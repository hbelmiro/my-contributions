# My Contributions

This repo tracks my open-source contributions, organized by project.

## Structure

Each top-level directory corresponds to a project (e.g., `kubeflow-pipelines/`). Inside each directory, contribution reports are named by year: `contributions-YYYY.md`.

## Generating a Contribution Report

When asked to generate or update a contribution report for a project, follow these steps.

### 1. Identify the GitHub repos

Ask the user which GitHub repos to include. Tracked orgs are `kubeflow`, `opendatahub-io`, and `red-hat-data-services`. Include all repos the user contributed to in those orgs. A single project may span multiple repos (e.g., `kubeflow/pipelines` and `kubeflow/pipelines-components`).

#### Fork deduplication

Several repos across these orgs are forks of each other (e.g., `red-hat-data-services/data-science-pipelines` is a fork of `opendatahub-io/data-science-pipelines`, which is a fork of `kubeflow/pipelines`; the same pattern exists for `pipelines-components`). Contributions must not be double-counted across a fork chain.

- Detect fork relationships with:

  ```bash
  gh api repos/<org>/<repo> --jq '{fork: .fork, parent: .parent.full_name, source: .source.full_name}'
  ```

  `parent` is the immediate fork target; `source` is the ultimate upstream root.

- **Attribution rule:** a contribution (PR, review, or issue) that exists in multiple repos of a fork chain counts once, in the most upstream repo where it exists. Precedence always goes to the most upstream contribution.
- **Exception:** a downstream backport PR that substantially changes the original upstream PR (non-mechanical conflict resolution, added fixes, changed behavior) also counts, attributed to the fork repo. Pure syncs or automated backports that mirror the upstream PR do not count.
- In practice: match PRs across the chain by title and code content, and compare the downstream diff against the upstream diff to decide whether a backport substantially changes the original. Gather per-repo data as usual, then dedupe while assembling the report.

### 2. Gather data with `gh`

**Never rely on local checkouts for any data.** Their remotes may point at forks and their branches may be stale. Always gather data from the live upstream source: the GitHub API (`gh`) for PRs, reviews, and issues, and a fresh fetch from the upstream remote for file contents (OWNERS, etc.).

For each repo, collect:

- **Merged PRs authored** in the target year:

  ```bash
  gh pr list --repo <org>/<repo> --author <username> --state merged \
    --search "merged:<year>-01-01..<year>-12-31" --limit 200 \
    --json number,title,mergedAt,url,labels,additions,deletions
  ```

- **PRs reviewed** (excluding self-reviews) in the target year:

  ```bash
  gh api --paginate \
    'search/issues?q=repo:<org>/<repo>+type:pr+reviewed-by:<username>+-author:<username>+merged:<year>-01-01..<year>-12-31&per_page=100' \
    --jq '.items[] | {number, title, html_url, user: .user.login, closed_at}'
  ```

- **Issues filed** in the target year:

  ```bash
  gh api --paginate \
    'search/issues?q=repo:<org>/<repo>+type:issue+author:<username>+created:<year>-01-01..<year>-12-31&per_page=100' \
    --jq '.items[] | {number, title, html_url, created_at, state}'
  ```

- **Open PRs** (to show ongoing work):

  ```bash
  gh pr list --repo <org>/<repo> --author <username> --state open \
    --json number,title,url,createdAt
  ```

- **Total lines changed** for authored PRs:

  ```bash
  gh pr list --repo <org>/<repo> --author <username> --state merged \
    --search "merged:<year>-01-01..<year>-12-31" --limit 200 \
    --json additions,deletions \
    --jq '[.[] | {a: .additions, d: .deletions}] | {total_additions: (map(.a) | add), total_deletions: (map(.d) | add), pr_count: length}'
  ```

- **OWNERS roles** (approver/reviewer) across repos in all tracked orgs (`kubeflow`, `opendatahub-io`, `red-hat-data-services`). Preferred: a sparse, blob-filtered clone of the real repo:

  ```bash
  git clone --depth 1 --filter=blob:none --sparse https://github.com/<org>/<repo>.git /tmp/<repo>-owners-check
  cd /tmp/<repo>-owners-check
  git sparse-checkout set --no-cone '/**/OWNERS'
  find . -name OWNERS | xargs grep -l <username>
  ```

  Alternative for single files: `gh api repos/<org>/<repo>/contents/<path>/OWNERS --jq '.content' | base64 -d`.
  Then read each matching file to classify the role (approver, reviewer, or both) and the directory scope. Clean up the temporary clone afterwards.

Run independent queries in parallel for efficiency.

### 3. Organize the report

Frame the report around **leadership impact**, not just a raw list. The report should tell the story of what the contributor drove, not merely enumerate commits.

#### Report structure

1. **Summary table** at the top with aggregate counts (PRs merged, PRs reviewed, issues filed, lines changed, open PRs) per repo.

2. **Merged PRs by area** for the primary repo. Categorize PRs into thematic groups that show breadth and depth of ownership. Good categories include:
   - Backend bug fixes and features
   - API and protobuf changes
   - CI/CD and infrastructure
   - Test reliability
   - Maintenance and governance
   - SDK changes
   - Frontend changes

   Only include categories that have PRs. Each category is a table with PR link, title, and merge date.

3. **Issues filed** as a table showing proactive identification of problems.

4. **Code reviews** — full table of PRs reviewed from other contributors, showing the author. This demonstrates mentoring and quality gate ownership. Separate automated dependency bumps (PRs authored by `dependabot[bot]` or `renovate[bot]` — classify by PR author, not title) into their own subsection; count them separately from human reviews in the summary and highlights.

5. **Open PRs** to show ongoing work and forward-looking initiatives.

6. **Governance — OWNERS roles** across repos in all tracked orgs (`kubeflow`, `opendatahub-io`, `red-hat-data-services`), showing where the contributor holds approver and/or reviewer roles. Organize by repo, with a table per repo listing path, approver (Yes/—), and reviewer (Yes/—).

7. **Merged PRs in secondary repos** as separate sections with their own tables. After fork deduplication, attribute each contribution to the most upstream repo where it exists; list substantial-change backports under the fork repo's section.

8. **Contribution highlights** at the end — a curated narrative section that calls out the most impactful work, grouped by theme:
   - Security improvements
   - Architecture and design contributions (KEPs, major refactors, migrations)
   - CI/CD ownership
   - Community and mentoring (review breadth, OWNERS file management, issue filing)

#### Formatting rules

- Use markdown tables with linked PR numbers (e.g., `[#1234](url)`)
- Sort PRs within each category by merge date, most recent first
- Use the PR title as-is (don't rewrite)
- Include the merge date in `YYYY-MM-DD` format
- For reviews, include the PR author's GitHub username
- All markdown files must pass `markdownlint-cli2` (config in `.markdownlint-cli2.jsonc`): run `npx -y markdownlint-cli2 --fix "**/*.md"` after writing the report

### 4. Write the file

Save as `<project-dir>/contributions-<year>.md` (e.g., `kubeflow-pipelines/contributions-2026.md`).

If a file for that year already exists, regenerate it from scratch with fresh data rather than patching it.

When a project directory has reports for more than one year, maintain a `README.md` in that directory summarizing all years: a yearly-reports link list, a short "At a Glance" table (one row per year: merged PRs, human reviews, brief highlights — not an exhaustive list), governance state, and any project-specific notes (e.g., fork-deduplication rules). Update it whenever a yearly report is generated or regenerated.
