# My Contributions

This repo tracks my open-source contributions, organized by project.

## Structure

Each top-level directory corresponds to a project (e.g., `kubeflow-pipelines/`). Inside each directory, contribution reports are named by year: `contributions-YYYY.md`.

## Generating a Contribution Report

When asked to generate or update a contribution report for a project, follow these steps.

### 1. Identify the GitHub repos

Ask the user which GitHub repos to include. A single project may span multiple repos (e.g., `kubeflow/pipelines` and `kubeflow/pipelines-components`).

### 2. Gather data with `gh`

**Never rely on local checkouts for any data.** Their remotes may point at forks and their branches may be stale. Always gather data from the live upstream source: the GitHub API (`gh`) for PRs, reviews, and issues, and a fresh fetch from the upstream remote for file contents (OWNERS, etc.).

For each repo, collect:

- **Merged PRs authored** in the target year:
  ```
  gh pr list --repo <org>/<repo> --author <username> --state merged \
    --search "merged:<year>-01-01..<year>-12-31" --limit 200 \
    --json number,title,mergedAt,url,labels,additions,deletions
  ```

- **PRs reviewed** (excluding self-reviews) in the target year:
  ```
  gh api --paginate \
    'search/issues?q=repo:<org>/<repo>+type:pr+reviewed-by:<username>+-author:<username>+merged:<year>-01-01..<year>-12-31&per_page=100' \
    --jq '.items[] | {number, title, html_url, user: .user.login, closed_at}'
  ```

- **Issues filed** in the target year:
  ```
  gh api --paginate \
    'search/issues?q=repo:<org>/<repo>+type:issue+author:<username>+created:<year>-01-01..<year>-12-31&per_page=100' \
    --jq '.items[] | {number, title, html_url, created_at, state}'
  ```

- **Open PRs** (to show ongoing work):
  ```
  gh pr list --repo <org>/<repo> --author <username> --state open \
    --json number,title,url,createdAt
  ```

- **Total lines changed** for authored PRs:
  ```
  gh pr list --repo <org>/<repo> --author <username> --state merged \
    --search "merged:<year>-01-01..<year>-12-31" --limit 200 \
    --json additions,deletions \
    --jq '[.[] | {a: .additions, d: .deletions}] | {total_additions: (map(.a) | add), total_deletions: (map(.d) | add), pr_count: length}'
  ```

- **OWNERS roles** (approver/reviewer) across kubeflow org repos. Preferred: a sparse, blob-filtered clone of the real repo:
  ```
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

6. **Governance — OWNERS roles** across kubeflow org repos, showing where the contributor holds approver and/or reviewer roles. Organize by repo, with a table per repo listing path, approver (Yes/—), and reviewer (Yes/—).

7. **Merged PRs in secondary repos** as separate sections with their own tables.

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

### 4. Write the file

Save as `<project-dir>/contributions-<year>.md` (e.g., `kubeflow-pipelines/contributions-2026.md`).

If a file for that year already exists, regenerate it from scratch with fresh data rather than patching it.
