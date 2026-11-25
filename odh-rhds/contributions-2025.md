# Open Data Hub / Red Hat Data Services Contributions — 2025

Contributions by [Helber Belmiro](https://github.com/hbelmiro) (`hbelmiro`) across the `opendatahub-io` and `red-hat-data-services` (RHDS) GitHub organizations, for calendar year 2025.

Fork-chain deduplication was applied: contributions that exist in upstream roots outside these two orgs (`kubeflow/pipelines`, `argoproj/argo-workflows`, `google/ml-metadata`) are excluded entirely, and contributions existing in both an ODH repo and its RHDS fork are attributed to the ODH repo.

## Summary

| Repo | PRs merged | PRs reviewed | Issues filed | Lines changed (+/−) |
| --- | ---: | ---: | ---: | ---: |
| [opendatahub-io/data-science-pipelines](https://github.com/opendatahub-io/data-science-pipelines) | 9 | 17 | 0 | 70,337 / 166,910 |
| [opendatahub-io/data-science-pipelines-operator](https://github.com/opendatahub-io/data-science-pipelines-operator) | 7 | 19 | 0 | 50 / 11 |
| [red-hat-data-services/data-science-pipelines](https://github.com/red-hat-data-services/data-science-pipelines) | 1 | 2 | 0 | 172 / 28 |
| [red-hat-data-services/data-science-pipelines-operator](https://github.com/red-hat-data-services/data-science-pipelines-operator) | 0 | 8 | 0 | — |
| [opendatahub-io/argo-workflows](https://github.com/opendatahub-io/argo-workflows) | 0 | 1 | 0 | — |
| [red-hat-data-services/argo-workflows](https://github.com/red-hat-data-services/argo-workflows) | 0 | 1 | 0 | — |
| **Total** | **17** | **48** | **0** | **70,559 / 166,949** |

No open PRs and no issues filed in these orgs in 2025. All reviews were of human-authored PRs (no dependabot/renovate reviews).

## Merged PRs by area — opendatahub-io/data-science-pipelines (primary repo)

### Upstream synchronization and rebases

Owning the fork's tracking of upstream Kubeflow Pipelines, including the major 2.5.0 rebase.

| PR | Title | Merged |
| --- | --- | --- |
| [#176](https://github.com/opendatahub-io/data-science-pipelines/pull/176) | Rebase over kubeflow@4c966f7 | 2025-06-05 |
| [#170](https://github.com/opendatahub-io/data-science-pipelines/pull/170) | Rebase 2.5.0 | 2025-05-28 |
| [#142](https://github.com/opendatahub-io/data-science-pipelines/pull/142) | UPSTREAM &lt;carry&gt;: Rebase code to kfp master branch - commit: 65d1d79fb7c77db076de0e9799516269c49e01a1 | 2025-02-25 |
| [#134](https://github.com/opendatahub-io/data-science-pipelines/pull/134) | UPSTREAM &lt;carry&gt;: Rebase code to kfp master branch - commit: 65d1d79fb7c77db076de0e9799516269c49e01a1 | 2025-02-12 |
| [#137](https://github.com/opendatahub-io/data-science-pipelines/pull/137) | UPSTREAM &lt;carry&gt;: Updated REBASE.opendatahub.md | 2025-02-20 |

### Backend bug fixes

| PR | Title | Merged |
| --- | --- | --- |
| [#132](https://github.com/opendatahub-io/data-science-pipelines/pull/132) | Fixed Pipeline Schedules failing after upgrading | 2025-02-06 |
| [#131](https://github.com/opendatahub-io/data-science-pipelines/pull/131) | Revert swf fixes | 2025-01-23 |
| [#130](https://github.com/opendatahub-io/data-science-pipelines/pull/130) | Revert swf fixes | 2025-01-23 |

### Build and container images

| PR | Title | Merged |
| --- | --- | --- |
| [#184](https://github.com/opendatahub-io/data-science-pipelines/pull/184) | UPSTREAM&lt;carry&gt;: Fixed warnings in Dockerfiles | 2025-06-24 |

## Code reviews — opendatahub-io/data-science-pipelines

17 reviews of PRs from other contributors, acting as a quality gate for the fork: rebases, upstream cherry-picks, CVE remediation, CI fixes, and OWNERS governance.

| PR | Title | Author |
| --- | --- | --- |
| [#244](https://github.com/opendatahub-io/data-science-pipelines/pull/244) | chore: [ODH stable-2.x] Remove DharmitD and rimolive from OWNERS files | mprahl |
| [#243](https://github.com/opendatahub-io/data-science-pipelines/pull/243) | chore: [ODH Stable] Remove DharmitD and rimolive from OWNERS files | mprahl |
| [#242](https://github.com/opendatahub-io/data-science-pipelines/pull/242) | chore: [ODH] Remove DharmitD and rimolive from OWNERS files | mprahl |
| [#239](https://github.com/opendatahub-io/data-science-pipelines/pull/239) | ci: fixing test image docker file path in the git workflow | nsingla |
| [#237](https://github.com/opendatahub-io/data-science-pipelines/pull/237) | cherry-pick 'configure ml-pipeline service address within driver.go' from upstream KFP | alyssacgoins |
| [#227](https://github.com/opendatahub-io/data-science-pipelines/pull/227) | ci: checking out before running action | nsingla |
| [#189](https://github.com/opendatahub-io/data-science-pipelines/pull/189) | (feat): Update dockerfile to support multi-arch builds | AjayJagan |
| [#188](https://github.com/opendatahub-io/data-science-pipelines/pull/188) | Merge master into stable | mprahl |
| [#158](https://github.com/opendatahub-io/data-science-pipelines/pull/158) | Cherry-pick: Allow the launcher command to be configurable (#11888) | mprahl |
| [#146](https://github.com/opendatahub-io/data-science-pipelines/pull/146) | Cherry-pick of (#11714): Ignore empty PULL_NUMBER environment variables in SDK tests | mprahl |
| [#145](https://github.com/opendatahub-io/data-science-pipelines/pull/145) | Rebase on KFP commit 78380095385be25e69b891ccb312b2857a200fdd | mprahl |
| [#143](https://github.com/opendatahub-io/data-science-pipelines/pull/143) | fix(backend): upgrading go to fix CVE-2024-45336 | dandawg |
| [#135](https://github.com/opendatahub-io/data-science-pipelines/pull/135) | fix(backend): glog upgrade fix for CVE GO-2025-3372 | dandawg |
| [#127](https://github.com/opendatahub-io/data-science-pipelines/pull/127) | merge v2.9.0 to stable | HumairAK |
| [#125](https://github.com/opendatahub-io/data-science-pipelines/pull/125) | Address CVEs | mprahl |
| [#120](https://github.com/opendatahub-io/data-science-pipelines/pull/120) | UPSTREAM: &lt;carry&gt;: Add ilab kfp pipeline to the DSPO repo | VaniHaripriya |
| [#118](https://github.com/opendatahub-io/data-science-pipelines/pull/118) | UPSTREAM: &lt;carry&gt;: Update ArtifactView enum to allow pipelines artifacts api to have optional content disposition | VaniHaripriya |

## Merged PRs — opendatahub-io/data-science-pipelines-operator

| PR | Title | Merged |
| --- | --- | --- |
| [#895](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/895) | Clarified DSP API server caching behavior in `dspipeline_types.go`. | 2025-07-18 |
| [#885](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/885) | Fixed warning in Dockerfile | 2025-06-25 |
| [#867](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/867) | Added `kubectl get pods` to log collection in the CI | 2025-06-18 |
| [#852](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/852) | Add hbelmiro as approver | 2025-06-06 |
| [#834](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/834) | Upgrade to KFP 2.5.0 | 2025-05-28 |
| [#794](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/794) | Upgraded actions/cache to v4 | 2025-02-20 |
| [#779](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/779) | Added support for TLS to scheduled-workflow | 2025-02-25 |

## Code reviews — opendatahub-io/data-science-pipelines-operator

19 reviews of PRs from other contributors, spanning controller features, CI/toolchain upgrades, CVE remediation, FIPS support, release documentation, and test infrastructure.

| PR | Title | Author |
| --- | --- | --- |
| [#953](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/953) | [ODH stable 2.x] Clean up the OWNERS file | mprahl |
| [#952](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/952) | Clean up the OWNERS file | mprahl |
| [#951](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/951) | Clean up the OWNERS file | mprahl |
| [#949](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/949) | removing hardcoded secrets | dchourasia |
| [#936](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/936) | chore: Update builder image to go 1.24 | gmfrasca |
| [#902](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/902) | chore: Use go.mod to get go version for CI setup | gmfrasca |
| [#888](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/888) | Bump Go version used in nightly tests | gmfrasca |
| [#887](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/887) | feat(controller): Add global configuration and functionality to manage or remove all Argo WCs | gmfrasca |
| [#848](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/848) | chore: parameterize container cli for test.sh | HumairAK |
| [#842](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/842) | Update the release documentation to use the GitHub workflow | mprahl |
| [#838](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/838) | Add CacheEnabled field to APIServer for configurable caching in DSPA | VaniHaripriya |
| [#836](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/836) | use a tag image instead of latest for proxy | HumairAK |
| [#835](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/835) | generalize standard tests | HumairAK |
| [#819](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/819) | Use the FIPS binaries when the cluster is in FIPS mode | mprahl |
| [#812](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/812) | replace iris data set with working link | HumairAK |
| [#788](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/788) | update params to match latest configs | HumairAK |
| [#777](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/777) | add runtime image | HumairAK |
| [#773](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/773) | update compatibility doc for 2.9 | HumairAK |
| [#770](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/770) | Address CVE-2024-45338 | mprahl |

## Merged PRs — red-hat-data-services/data-science-pipelines

| PR | Title | Merged |
| --- | --- | --- |
| [#183](https://github.com/red-hat-data-services/data-science-pipelines/pull/183) | Cherry pick RHOAIENG-14265 | 2025-01-17 |

(The identically-sized ODH counterpart, [opendatahub-io/data-science-pipelines#126](https://github.com/opendatahub-io/data-science-pipelines/pull/126), was closed unmerged, so this contribution is counted in the RHDS repo where it actually merged.)

## Code reviews — red-hat-data-services/data-science-pipelines-operator

Reviews of branch-specific maintenance PRs (RHOAI release branches, Konflux builder images) that exist only in the RHDS fork.

| PR | Title | Author |
| --- | --- | --- |
| [#561](https://github.com/red-hat-data-services/data-science-pipelines-operator/pull/561) | chore: Bump konflux builder images to go1.24 - main | gmfrasca |
| [#560](https://github.com/red-hat-data-services/data-science-pipelines-operator/pull/560) | chore: Bump builder images to go1.24 - rhoai 2.16 | gmfrasca |
| [#559](https://github.com/red-hat-data-services/data-science-pipelines-operator/pull/559) | chore: Bump builder images to go1.24 - rhoai 2.19 | gmfrasca |
| [#558](https://github.com/red-hat-data-services/data-science-pipelines-operator/pull/558) | chore: Bump builder images to go1.24 - rhoai 2.21 | gmfrasca |
| [#557](https://github.com/red-hat-data-services/data-science-pipelines-operator/pull/557) | chore: Bump builder images to go1.24 - rhoai 2.22 | gmfrasca |
| [#556](https://github.com/red-hat-data-services/data-science-pipelines-operator/pull/556) | chore: Bump builder images to go1.24 - rhoai 3.0 | gmfrasca |
| [#555](https://github.com/red-hat-data-services/data-science-pipelines-operator/pull/555) | chore: Bump builder images to go1.24 - rhoai 2.25 | gmfrasca |
| [#206](https://github.com/red-hat-data-services/data-science-pipelines-operator/pull/206) | CVE Resolution: update glog to 1.2.4 | ckhordiasma |

## Code reviews — other repos

| Repo | PR | Title | Author |
| --- | --- | --- | --- |
| opendatahub-io/argo-workflows | [#36](https://github.com/opendatahub-io/argo-workflows/pull/36) | DRAFT: Upgrade ODH Argo fork to upstream v3.5.14 | gmfrasca |
| red-hat-data-services/argo-workflows | [#397](https://github.com/red-hat-data-services/argo-workflows/pull/397) | fix(cve): CVE-2025-47913 for rhoai-2.22 | nsingla |
| red-hat-data-services/data-science-pipelines | [#666](https://github.com/red-hat-data-services/data-science-pipelines/pull/666) | cherry-pick: ignore unknown fields for pb json unmarshaling | HumairAK |
| red-hat-data-services/data-science-pipelines | [#248](https://github.com/red-hat-data-services/data-science-pipelines/pull/248) | CVE Resolution: update glog to 1.2.4 | ckhordiasma |

## Governance — OWNERS roles

OWNERS roles held in ODH/RHDS repos, verified against the live upstream repositories (RHDS mirrors of ODH files are not repeated; the ODH repo is listed where the file is shared). Roles in `opendatahub-io/pipelines-components` mirror the upstream `kubeflow/pipelines-components` OWNERS files and are therefore excluded from this report.

### opendatahub-io/data-science-pipelines

| Path | Approver | Reviewer |
| --- | --- | --- |
| `/` | Yes | Yes |
| `/kubernetes_platform` | Yes | Yes |

### opendatahub-io/data-science-pipelines-operator

| Path | Approver | Reviewer |
| --- | --- | --- |
| `/` | Yes | Yes |

### opendatahub-io/model-registry-operator

| Path | Approver | Reviewer |
| --- | --- | --- |
| `/` | Yes | Yes |

### opendatahub-io/argo-workflows (file shared with red-hat-data-services/argo-workflows)

| Path | Approver | Reviewer |
| --- | --- | --- |
| `/` | — | Yes |

## Contribution highlights

### Upstream fork stewardship

- Drove the ODH Kubeflow Pipelines fork's upstream tracking for 2025: executed the rebase onto KFP 2.5.0 ([#170](https://github.com/opendatahub-io/data-science-pipelines/pull/170)), the follow-up rebase over kubeflow@4c966f7 ([#176](https://github.com/opendatahub-io/data-science-pipelines/pull/176)), and two full rebases of the fork onto the KFP master branch at commit 65d1d79 ([#142](https://github.com/opendatahub-io/data-science-pipelines/pull/142), [#134](https://github.com/opendatahub-io/data-science-pipelines/pull/134)) — together touching roughly 100k lines across additions and deletions.
- Coordinated the matching operator-side upgrade to KFP 2.5.0 ([data-science-pipelines-operator#834](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/834)), keeping the DSPA operator and the backend fork in sync.

### Backend reliability

- Fixed Pipeline Schedules failing after upgrades ([#132](https://github.com/opendatahub-io/data-science-pipelines/pull/132)) and cleanly reverted problematic scheduled-workflow fixes with two targeted revert PRs ([#131](https://github.com/opendatahub-io/data-science-pipelines/pull/131), [#130](https://github.com/opendatahub-io/data-science-pipelines/pull/130)).
- Added TLS support for scheduled-workflows in the operator ([data-science-pipelines-operator#779](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/779)) and clarified DSP API server caching semantics in the CRD types ([data-science-pipelines-operator#895](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/895)).

### CI/CD and infrastructure

- Improved operator CI: added pod state collection to CI log gathering ([data-science-pipelines-operator#867](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/867)), upgraded actions/cache to v4 ([#794](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/794)), and fixed Dockerfile warnings in both repos.
- Reviewed the operator toolchain modernization (Go 1.24 builder images, go.mod-driven CI Go versioning, nightly-test Go bumps) across the ODH repo and seven RHOAI release branches in the RHDS fork.

### Community and quality-gate ownership

- 48 code reviews of other contributors' PRs across six repos in the two orgs — the busiest review areas being the DSP backend fork (17) and the DSPA operator (19) — covering rebases, upstream cherry-picks, CVE remediation (CVE-2024-45336, CVE-2024-45338, GO-2025-3372, glog CVEs), FIPS support, and test infrastructure.
- OWNERS approver in three ODH repos (data-science-pipelines incl. `kubernetes_platform`, data-science-pipelines-operator, model-registry-operator) and reviewer in the ODH/RHDS argo-workflows fork, added via open governance PRs ([data-science-pipelines-operator#852](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/852)); also reviewed the 2025 OWNERS cleanups and maintainer removals in both DSP repos.

## Deduplication notes

Excluded because the same contribution exists in an upstream root outside the two orgs (all by `hbelmiro` in `kubeflow/pipelines`):

- odh#122 (UPSTREAM: 11480), odh#123 (UPSTREAM: 11481), odh#124 (UPSTREAM: 11469), odh#171 (UPSTREAM: 11891, 11911) — cherry-picks of kubeflow/pipelines PRs #11480, #11481, #11469, #11911.
- odh#182 and its RHDS mirror rhds#703 ("Fix boolean flag syntax for `--cache_disabled`") — exists upstream as kubeflow/pipelines#12001.
- Review of odh-dsp#245 (CVE-2025-68156) — the same change by the same author exists upstream as kubeflow/pipelines#12571.

Excluded as mechanical RHDS mirrors of ODH PRs (attributed to ODH where counted):

- rhds-dsp#199/#200 ("Revert swf fixes") — mirrors of odh-dsp#130/#131.
- rhds OWNERS files identical to the ODH repo's — governance attributed to the ODH repo.

Counted in RHDS only (no merged ODH counterpart):

- rhds-dsp#183 ("Cherry pick RHOAIENG-14265") — the identical ODH PR #126 was closed unmerged.
- rhds-dspo branch-specific PRs (go1.24 builder bumps per RHOAI branch, glog CVE) and rhds-argo#397 — exist only in the RHDS fork.
