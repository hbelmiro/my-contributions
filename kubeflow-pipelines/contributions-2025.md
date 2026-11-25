# Kubeflow Pipelines Contributions — 2025 (hbelmiro)

## Summary

| Repo | PRs Merged | PRs Reviewed (human) | PRs Reviewed (bots) | Issues Filed | Lines Added | Lines Deleted | Open PRs |
| --- | --- | --- | --- | --- | --- | --- | --- |
| [kubeflow/pipelines](https://github.com/kubeflow/pipelines) | 30 | 99 | 8 | 41 | 24,594 | 144,370 | 0 |
| [kubeflow/pipelines-components](https://github.com/kubeflow/pipelines-components) | 14 | 4 | 3 | 0 | 6,684 | 2,164 | 0 |
| **Total** | **44** | **103** | **11** | **41** | **31,278** | **146,534** | **0** |

## Merged PRs in kubeflow/pipelines

### Backend bug fixes and features

| PR | Title | Merged |
| --- | --- | --- |
| [#12467](https://github.com/kubeflow/pipelines/pull/12467) | fix(backend): Parse JSON and decode base64 in artifact client | 2025-11-21 |
| [#12394](https://github.com/kubeflow/pipelines/pull/12394) | Implemented HTTP Artifact Streaming to Prevent OOM Errors with Large Files | 2025-11-19 |
| [#12001](https://github.com/kubeflow/pipelines/pull/12001) | fix(backend): Fix boolean flag syntax for `--cache_disabled` and update test to cover pipelines with outputs | 2025-06-23 |
| [#11831](https://github.com/kubeflow/pipelines/pull/11831) | feat(backend): add the option to enable/disable cache globally | 2025-05-08 |
| [#11771](https://github.com/kubeflow/pipelines/pull/11771) | feat(backend): Add the ability to set a proxy for accessing external resources | 2025-04-10 |
| [#11578](https://github.com/kubeflow/pipelines/pull/11578) | fix(backend): Replaced hardcoded ServiceAccount with default config | 2025-02-05 |
| [#11469](https://github.com/kubeflow/pipelines/pull/11469) | fix(backend): Synced ScheduledWorkflow CRs on apiserver startup | 2025-01-08 |
| [#11481](https://github.com/kubeflow/pipelines/pull/11481) | chore(backend): Fixed ServiceAccount in job creation | 2025-01-08 |
| [#11480](https://github.com/kubeflow/pipelines/pull/11480) | chore(backend): Fixed namespace in job creation | 2025-01-08 |

### CI/CD and infrastructure

| PR | Title | Merged |
| --- | --- | --- |
| [#12543](https://github.com/kubeflow/pipelines/pull/12543) | fix(manifests): Allow same-namespace access to SeaweedFS for standalone deployments | 2025-12-12 |
| [#12121](https://github.com/kubeflow/pipelines/pull/12121) | chore(CI): Fix invalid references in workflow conditions and update GitHub Actions to use `actions/checkout@v5` consistently | 2025-08-13 |
| [#12074](https://github.com/kubeflow/pipelines/pull/12074) | chore: Switch Argo Workflows manifests to remote Git references | 2025-07-29 |
| [#12072](https://github.com/kubeflow/pipelines/pull/12072) | chore: Upgrade Argo Workflows to v3.6.7, bump golang version to v.1.24 | 2025-07-25 |
| [#11806](https://github.com/kubeflow/pipelines/pull/11806) | chore(test): Improved path filtering in the CI | 2025-04-15 |
| [#11796](https://github.com/kubeflow/pipelines/pull/11796) | chore(test): Removed the no longer needed rerun-pr-jobs.yml | 2025-04-09 |
| [#11786](https://github.com/kubeflow/pipelines/pull/11786) | chore(test): Bumped ubuntu runner to 24.04 in rerun-pr-jobs.yml | 2025-04-01 |
| [#11784](https://github.com/kubeflow/pipelines/pull/11784) | chore(test): Replaced the unmaintained rerun action | 2025-04-01 |

### Test reliability

| PR | Title | Merged |
| --- | --- | --- |
| [#11916](https://github.com/kubeflow/pipelines/pull/11916) | chore(test): Update cache test timeout and polling intervals | 2025-05-15 |
| [#11910](https://github.com/kubeflow/pipelines/pull/11910) | chore(test): fixed log collection in tests | 2025-05-21 |
| [#11911](https://github.com/kubeflow/pipelines/pull/11911) | chore(tests): fix KFP SDK tests | 2025-05-14 |
| [#11779](https://github.com/kubeflow/pipelines/pull/11779) | test: Added the result of `kubectl get pods` to logs when waiting for pods to get ready | 2025-03-31 |
| [#11775](https://github.com/kubeflow/pipelines/pull/11775) | test: Fixed `collect-logs.sh` path | 2025-03-28 |
| [#11773](https://github.com/kubeflow/pipelines/pull/11773) | test: Fixed and improved log collection | 2025-03-27 |
| [#11658](https://github.com/kubeflow/pipelines/pull/11658) | chore(test): Increased timeout in test | 2025-02-20 |
| [#11545](https://github.com/kubeflow/pipelines/pull/11545) | chore(test): Fixed namespace in tests | 2025-01-27 |

### Maintenance and governance

| PR | Title | Merged |
| --- | --- | --- |
| [#12065](https://github.com/kubeflow/pipelines/pull/12065) | chore(docs): Added new AI/ML lifecycle blog post link to README.md | 2025-07-22 |
| [#12003](https://github.com/kubeflow/pipelines/pull/12003) | chore(backend): Fixed warnings in Dockerfiles | 2025-06-23 |
| [#11844](https://github.com/kubeflow/pipelines/pull/11844) | chore(backend): fixed support for Podman in Makefile | 2025-04-23 |
| [#11834](https://github.com/kubeflow/pipelines/pull/11834) | chore(backend): Optimized Dockerfiles | 2025-04-17 |
| [#11841](https://github.com/kubeflow/pipelines/pull/11841) | fix(backend): fixed Dockerfile | 2025-04-21 |

## Issues filed in kubeflow/pipelines

| Issue | Title | Filed | State |
| --- | --- | --- | --- |
| [#12513](https://github.com/kubeflow/pipelines/issues/12513) | KEP-12513: Filesystem-Based Artifact Storage for Kubeflow Pipelines | 2025-12-03 | open |
| [#12439](https://github.com/kubeflow/pipelines/issues/12439) | chore(<backend>): Encapsulate `v2/objectstore` package to prevent usage outside v2 execution engine | 2025-11-12 | closed |
| [#12018](https://github.com/kubeflow/pipelines/issues/12018) | chore(<test>): Run tests on post-merge with different global configurations | 2025-06-26 | closed |
| [#12017](https://github.com/kubeflow/pipelines/issues/12017) | chore(<test>): Increase integration test coverage by not relying only on pipelines based on container components | 2025-06-26 | closed |
| [#11990](https://github.com/kubeflow/pipelines/issues/11990) | [backend] Pipelines with outputs fail when `CACHEENABLED = false` | 2025-06-18 | closed |
| [#11923](https://github.com/kubeflow/pipelines/issues/11923) | chore(<tests>): Clean up unnecessary parentheses and fix the formatting of the CI files | 2025-05-21 | closed |
| [#11922](https://github.com/kubeflow/pipelines/issues/11922) | chore(sdk): Drop support for Python 3.9, discuss 3.10 | 2025-05-21 | closed |
| [#11840](https://github.com/kubeflow/pipelines/issues/11840) | [feature] Add the option to enable/disable cache globally | 2025-04-21 | closed |
| [#11764](https://github.com/kubeflow/pipelines/issues/11764) | chore: Fix CVEs | 2025-03-21 | closed |
| [#11744](https://github.com/kubeflow/pipelines/issues/11744) | [feature] Add the ability to set a proxy for accessing external resources | 2025-03-12 | closed |
| [#11727](https://github.com/kubeflow/pipelines/issues/11727) | chore(<test>): Separate infrastructure commands from actual test commands in CI and scripts | 2025-03-05 | closed |
| [#11706](https://github.com/kubeflow/pipelines/issues/11706) | chore(<test>): Update test/README.md#running-tests-locally-with-kind to reflect the changes from #11494 | 2025-02-28 | closed |
| [#11705](https://github.com/kubeflow/pipelines/issues/11705) | chore(<test>): Use `make` commands in .github/workflows/validate-generated-files.yml | 2025-02-28 | closed |
| [#11704](https://github.com/kubeflow/pipelines/issues/11704) | chore(<test>): Use `make` commands in .github/workflows/upgrade-test.yml | 2025-02-28 | closed |
| [#11703](https://github.com/kubeflow/pipelines/issues/11703) | chore(<test>): Use `make` commands in .github/workflows/sdk-yapf.yml | 2025-02-28 | closed |
| [#11702](https://github.com/kubeflow/pipelines/issues/11702) | chore(<test>): Use `make` commands in .github/workflows/sdk-upgrade.yml | 2025-02-28 | closed |
| [#11701](https://github.com/kubeflow/pipelines/issues/11701) | chore(<test>): Use `make` commands in .github/workflows/sdk-isort.yml | 2025-02-28 | closed |
| [#11700](https://github.com/kubeflow/pipelines/issues/11700) | chore(<test>): Use `make` commands in .github/workflows/sdk-execution.yml | 2025-02-28 | closed |
| [#11699](https://github.com/kubeflow/pipelines/issues/11699) | chore(<test>): Use `make` commands in .github/workflows/sdk-docformatter.yml | 2025-02-28 | closed |
| [#11698](https://github.com/kubeflow/pipelines/issues/11698) | chore(<test>): https://github.com/kubeflow/pipelines/blob/master/.github/workflows/sdk-component-yaml.yml | 2025-02-28 | closed |
| [#11697](https://github.com/kubeflow/pipelines/issues/11697) | chore(<test>): Use `make` commands in .github/workflows/presubmit-backend.yml | 2025-02-28 | closed |
| [#11696](https://github.com/kubeflow/pipelines/issues/11696) | chore(<test>): Use `make` commands in .github/workflows/periodic.yml | 2025-02-28 | closed |
| [#11695](https://github.com/kubeflow/pipelines/issues/11695) | chore(<test>): Use `make` commands in .github/workflows/kubeflow-pipelines-manifests.yml | 2025-02-28 | closed |
| [#11694](https://github.com/kubeflow/pipelines/issues/11694) | chore(<test>): Use `make` commands in .github/workflows/kfp-sdk-tests.yml | 2025-02-28 | closed |
| [#11693](https://github.com/kubeflow/pipelines/issues/11693) | chore(<test>): Use `make` commands in .github/workflows/kfp-sdk-runtime-tests.yml | 2025-02-28 | closed |
| [#11692](https://github.com/kubeflow/pipelines/issues/11692) | chore(<test>): Use `make` commands in .github/workflows/kfp-samples.yml | 2025-02-28 | closed |
| [#11691](https://github.com/kubeflow/pipelines/issues/11691) | chore(<test>): Use `make` commands in .github/workflows/kfp-kubernetes-library-test.yml | 2025-02-28 | closed |
| [#11690](https://github.com/kubeflow/pipelines/issues/11690) | chore(<test>): Use `make` commands in .github/workflows/kfp-kubernetes-execution-tests.yml | 2025-02-28 | closed |
| [#11689](https://github.com/kubeflow/pipelines/issues/11689) | chore(<test>): Use `make` commands in .github/workflows/gcpc-modules-tests.yml | 2025-02-28 | closed |
| [#11688](https://github.com/kubeflow/pipelines/issues/11688) | chore(<test>): Use `make` commands in .github/workflows/frontend.yml | 2025-02-28 | closed |
| [#11687](https://github.com/kubeflow/pipelines/issues/11687) | chore(<test>): Use `make` commands in .github/workflows/e2e-test.yml | 2025-02-28 | closed |
| [#11686](https://github.com/kubeflow/pipelines/issues/11686) | chore(<test>): Use `make` commands in .github/workflows/backend-visualization.yml | 2025-02-28 | closed |
| [#11665](https://github.com/kubeflow/pipelines/issues/11665) | [feature] Delete a pipeline and all its pipeline versions in one single step | 2025-02-24 | closed |
| [#11649](https://github.com/kubeflow/pipelines/issues/11649) | chore(<test>): `KFP Samples` test is flaky | 2025-02-18 | closed |
| [#11612](https://github.com/kubeflow/pipelines/issues/11612) | Test | 2025-02-11 | closed |
| [#11611](https://github.com/kubeflow/pipelines/issues/11611) | chore(<test>): Create an integration test for Scheduled/Recurring runs | 2025-02-11 | closed |
| [#11574](https://github.com/kubeflow/pipelines/issues/11574) | [backend] `ServiceAccountName` is hardcoded in the Argo compiler. It should use the `DefaultPipelineRunnerServiceAccount` config | 2025-01-31 | closed |
| [#11568](https://github.com/kubeflow/pipelines/issues/11568) | chore(<frontend>): Frontend tests are failing in the `master` branch. | 2025-01-29 | closed |
| [#11558](https://github.com/kubeflow/pipelines/issues/11558) | chore(<test>): kfp-sdk-tests has an error in the python version variable | 2025-01-27 | closed |
| [#11495](https://github.com/kubeflow/pipelines/issues/11495) | chore(tests): Create a test to check whether `requirements.txt` was generated with `pip-compile` | 2025-01-02 | closed |
| [#11494](https://github.com/kubeflow/pipelines/issues/11494) | chore(tests): Create `make` commands for running tests locally | 2025-01-02 | open |

## Code reviews in kubeflow/pipelines

99 reviews of PRs from other human contributors:

| PR | Title | Author | Merged |
| --- | --- | --- | --- |
| [#12570](https://github.com/kubeflow/pipelines/pull/12570) | chore: [2.14] Remove DharmitD and rimolive due to inactivity | mprahl | 2025-12-22 |
| [#12568](https://github.com/kubeflow/pipelines/pull/12568) | chore: [2.15] Remove DharmitD and rimolive due to inactivity | mprahl | 2025-12-22 |
| [#12567](https://github.com/kubeflow/pipelines/pull/12567) | chore: Remove DharmitD and rimolive due to inactivity | mprahl | 2025-12-22 |
| [#12549](https://github.com/kubeflow/pipelines/pull/12549) | Cleanup kind workflows and Harden release downloads(incl. artifact paging) | sduvvuri1603 | 2025-12-12 |
| [#12527](https://github.com/kubeflow/pipelines/pull/12527) | chore: add GitHub welcome workflow for new contributors | aniketpati1121 | 2025-12-24 |
| [#12492](https://github.com/kubeflow/pipelines/pull/12492) | chore: remove duplicate default-allow-same-namespace network policy | akagami-harsh | 2025-12-01 |
| [#12481](https://github.com/kubeflow/pipelines/pull/12481) | configure ml-pipeline service address within driver.go | alyssacgoins | 2025-11-25 |
| [#12475](https://github.com/kubeflow/pipelines/pull/12475) | ci: fixing and reenabling upgrade tests | nsingla | 2025-11-24 |
| [#12447](https://github.com/kubeflow/pipelines/pull/12447) | add free disk space job to api server tests | HumairAK | 2025-11-14 |
| [#12433](https://github.com/kubeflow/pipelines/pull/12433) | chore(release): bumped version to 2.14.4 | HumairAK | 2025-11-11 |
| [#12432](https://github.com/kubeflow/pipelines/pull/12432) | chore: update google-cloud-components-image | HumairAK | 2025-11-11 |
| [#12429](https://github.com/kubeflow/pipelines/pull/12429) | fix visualization docker build failures by bumping python | HumairAK | 2025-11-11 |
| [#12421](https://github.com/kubeflow/pipelines/pull/12421) | test: fixing http client creation and renaming e2e pipeline name prefix | nsingla | 2025-11-07 |
| [#12408](https://github.com/kubeflow/pipelines/pull/12408) | chore: Extend and update the stalebot | juliusvonkohout | 2025-11-13 |
| [#12377](https://github.com/kubeflow/pipelines/pull/12377) | Optional Runtime Parameters Fix | sduvvuri1603 | 2025-10-28 |
| [#12248](https://github.com/kubeflow/pipelines/pull/12248) | feat(backend, sdk): Add custom_path field to RuntimeArtifact | alyssacgoins | 2025-10-29 |
| [#12149](https://github.com/kubeflow/pipelines/pull/12149) | Fix failing backend test | akagami-harsh | 2025-08-15 |
| [#12147](https://github.com/kubeflow/pipelines/pull/12147) | propose removing mlmd from kfp | HumairAK | 2025-08-20 |
| [#12145](https://github.com/kubeflow/pipelines/pull/12145) | fix(manifests): Include WC Deployment patch when updating Argo manifests. Fixes #12144 | gmfrasca | 2025-08-15 |
| [#12132](https://github.com/kubeflow/pipelines/pull/12132) | fix(sdk): Set spec.description when compiling to Kubernetes manifests | mprahl | 2025-08-13 |
| [#12108](https://github.com/kubeflow/pipelines/pull/12108) | test generating backend proto go code | HumairAK | 2025-08-05 |
| [#12107](https://github.com/kubeflow/pipelines/pull/12107) | Fix samples-test workflow | akagami-harsh | 2025-08-06 |
| [#12099](https://github.com/kubeflow/pipelines/pull/12099) | fix(deps): revert metadata_writer k8s version | zazulam | 2025-08-01 |
| [#12093](https://github.com/kubeflow/pipelines/pull/12093) | fix(CI): Reduces CI time. Fixes #11768 | nsingla | 2025-08-07 |
| [#12083](https://github.com/kubeflow/pipelines/pull/12083) | chore(backend): resolve linting errors | HumairAK | 2025-07-29 |
| [#12028](https://github.com/kubeflow/pipelines/pull/12028) | feat(sdk) Add Input Parameter support for node affinity | VaniHaripriya | 2025-07-30 |
| [#12019](https://github.com/kubeflow/pipelines/pull/12019) | fix: Delete the pipeline along with its all versions. Fixes #11665 | milinddethe15 | 2025-07-16 |
| [#11998](https://github.com/kubeflow/pipelines/pull/11998) | fix(apiserver): fix typos in resource_manager.go: | milosjava | 2025-06-23 |
| [#11982](https://github.com/kubeflow/pipelines/pull/11982) | feat(backend): update Argo Workflow Compiler to create workspace PVCs | VaniHaripriya | 2025-07-17 |
| [#11980](https://github.com/kubeflow/pipelines/pull/11980) | feat(backend): support for optional input parameters in nested pipelines | alyssacgoins | 2025-07-14 |
| [#11955](https://github.com/kubeflow/pipelines/pull/11955) | feat(frontend) Use native k8s probes for pipeline-ui | LaurentGoderre | 2025-06-06 |
| [#11952](https://github.com/kubeflow/pipelines/pull/11952) | feat(backend/frontend): Add the name field for pipelines and pipeline versions | mprahl | 2025-06-06 |
| [#11948](https://github.com/kubeflow/pipelines/pull/11948) | chore: Adding Devin's DeepWiki to README | franciscojavierarceo | 2025-06-02 |
| [#11926](https://github.com/kubeflow/pipelines/pull/11926) | chore(ci): clean up unnecessary parentheses and fix the formatting of the CI files | lekaf974 | 2025-05-27 |
| [#11924](https://github.com/kubeflow/pipelines/pull/11924) | test: Update the Kubernetes and Python version ranges in the CI | mprahl | 2025-05-28 |
| [#11917](https://github.com/kubeflow/pipelines/pull/11917) | chore(backend): upgrade mysql to 8.4 | HumairAK | 2025-05-16 |
| [#11903](https://github.com/kubeflow/pipelines/pull/11903) | fix(sdk): Resolves issue when using ParallelFor with param and depending tasks | mai-nakagawa | 2025-05-09 |
| [#11896](https://github.com/kubeflow/pipelines/pull/11896) | chore: correct broken links in README.md | Shekharrajak | 2025-05-09 |
| [#11888](https://github.com/kubeflow/pipelines/pull/11888) | feat(backend): Allow the launcher command to be configurable | mprahl | 2025-05-02 |
| [#11886](https://github.com/kubeflow/pipelines/pull/11886) | chore: update all owners files | HumairAK | 2025-05-02 |
| [#11875](https://github.com/kubeflow/pipelines/pull/11875) | docs(KEP): Propose a new pipeline run workspace feature | mprahl | 2025-05-16 |
| [#11866](https://github.com/kubeflow/pipelines/pull/11866) | fix(sdk): resolve issue when creating pipeline version from pipeline name using the cli. Fixes #11810 | chjdev | 2025-04-30 |
| [#11845](https://github.com/kubeflow/pipelines/pull/11845) | chore(sdk): update go toolchain patch | HumairAK | 2025-04-21 |
| [#11842](https://github.com/kubeflow/pipelines/pull/11842) | add missing release note updates to sdk main branch | HumairAK | 2025-04-21 |
| [#11824](https://github.com/kubeflow/pipelines/pull/11824) | fix(docs): Remove Podman as backend README pre-req | alyssacgoins | 2025-04-15 |
| [#11820](https://github.com/kubeflow/pipelines/pull/11820) | fix(docs): Use the latest driver and launcher images in the dev environment | mprahl | 2025-04-11 |
| [#11819](https://github.com/kubeflow/pipelines/pull/11819) | fix(deps): widen urllib3 upper bound to <3.0.0 | dolfim-ibm | 2025-04-14 |
| [#11818](https://github.com/kubeflow/pipelines/pull/11818) | fix(tests): free up space in some test runners | droctothorpe | 2025-04-11 |
| [#11809](https://github.com/kubeflow/pipelines/pull/11809) | feat(backend): implement logs as artifacts + CI updates | droctothorpe | 2025-04-11 |
| [#11800](https://github.com/kubeflow/pipelines/pull/11800) | (chore): add image builds for default branch | HumairAK | 2025-04-09 |
| [#11798](https://github.com/kubeflow/pipelines/pull/11798) | fix setup env for kfp k8s lib tests | HumairAK | 2025-04-09 |
| [#11792](https://github.com/kubeflow/pipelines/pull/11792) | increase stale action timers | HumairAK | 2025-04-07 |
| [#11780](https://github.com/kubeflow/pipelines/pull/11780) | chore(backend): upgade go and deps | HumairAK | 2025-03-31 |
| [#11777](https://github.com/kubeflow/pipelines/pull/11777) | chore(backend): refactor driver tests | HumairAK | 2025-03-31 |
| [#11776](https://github.com/kubeflow/pipelines/pull/11776) | fix(backend): Include missing go.mod for cacheserver/viewercontroller images | gmfrasca | 2025-03-28 |
| [#11772](https://github.com/kubeflow/pipelines/pull/11772) | fix(CI) Github action is vulnerable to code execution via `comment body` | lociko | 2025-03-26 |
| [#11770](https://github.com/kubeflow/pipelines/pull/11770) | feat(backend/sdk): Add input parameterization for various k8s resources | HumairAK | 2025-03-28 |
| [#11751](https://github.com/kubeflow/pipelines/pull/11751) | Fix PSS restricted warnings | akagami-harsh | 2025-03-26 |
| [#11750](https://github.com/kubeflow/pipelines/pull/11750) | Fix Istio sidecar injection by moving from annotations to labels | madmecodes | 2025-03-17 |
| [#11735](https://github.com/kubeflow/pipelines/pull/11735) | fix(sdk): allow google-cloud-storage < 4 | parthea | 2025-04-08 |
| [#11734](https://github.com/kubeflow/pipelines/pull/11734) | fix: minio fsgroup for popular clusters | juliusvonkohout | 2025-03-12 |
| [#11719](https://github.com/kubeflow/pipelines/pull/11719) | remove unused function | HumairAK | 2025-03-01 |
| [#11678](https://github.com/kubeflow/pipelines/pull/11678) | chore: improved securitycontext for mysql | juliusvonkohout | 2025-02-28 |
| [#11676](https://github.com/kubeflow/pipelines/pull/11676) | docs: Add documentation for set_image_pull_secrets | george-kuanli-peng | 2025-02-27 |
| [#11675](https://github.com/kubeflow/pipelines/pull/11675) | chore: nominate sdk/backend reviewers | HumairAK | 2025-02-26 |
| [#11669](https://github.com/kubeflow/pipelines/pull/11669) | Chore: fix the PPC image for the dockerhub ratelimit and add the securitycontext | juliusvonkohout | 2025-03-05 |
| [#11668](https://github.com/kubeflow/pipelines/pull/11668) | chore: Fix typos | co63oc | 2025-04-09 |
| [#11662](https://github.com/kubeflow/pipelines/pull/11662) | fix(backend): ignore unknown fields for pb json unmarshaling | HumairAK | 2025-02-24 |
| [#11618](https://github.com/kubeflow/pipelines/pull/11618) | (test) : Collect and upload logs when test fails for k8s | chahatsagarmain | 2025-02-18 |
| [#11610](https://github.com/kubeflow/pipelines/pull/11610) | docs(backend): fixed docker cmd in docs for non-amd64 | dandawg | 2025-02-12 |
| [#11609](https://github.com/kubeflow/pipelines/pull/11609) | chore: Remove License checker | HumairAK | 2025-02-10 |
| [#11608](https://github.com/kubeflow/pipelines/pull/11608) | fix(backend): the metacontroller is broken since #11474 | juliusvonkohout | 2025-02-10 |
| [#11604](https://github.com/kubeflow/pipelines/pull/11604) | chore(backend): fixed imports on metadata_helpers.py | dandawg | 2025-02-10 |
| [#11603](https://github.com/kubeflow/pipelines/pull/11603) | chore(backend): updated deprecated grpc func | dandawg | 2025-02-11 |
| [#11585](https://github.com/kubeflow/pipelines/pull/11585) | fix(backend) fix run retry for argo | ntny | 2025-02-17 |
| [#11577](https://github.com/kubeflow/pipelines/pull/11577) | chore(deps): replace deprecated ioutil with os and io in tests | dandawg | 2025-01-31 |
| [#11575](https://github.com/kubeflow/pipelines/pull/11575) | chore(frontend) : Fix frontend failing ci test | chahatsagarmain | 2025-02-02 |
| [#11570](https://github.com/kubeflow/pipelines/pull/11570) | docs(backend): small formatting improvements | dandawg | 2025-02-12 |
| [#11559](https://github.com/kubeflow/pipelines/pull/11559) | chor(test) : Fix kfp-sdk-test for different python versions | chahatsagarmain | 2025-02-10 |
| [#11553](https://github.com/kubeflow/pipelines/pull/11553) | feat(backend): add support for uploading new sample pipeline vers | HumairAK | 2025-01-25 |
| [#11551](https://github.com/kubeflow/pipelines/pull/11551) | docs: Add a KEP for a Kubernetes native API for pipelines | mprahl | 2025-02-26 |
| [#11547](https://github.com/kubeflow/pipelines/pull/11547) | fix(sdk): dsl.component docstring typo | dandawg | 2025-01-24 |
| [#11539](https://github.com/kubeflow/pipelines/pull/11539) | `[chore][backend]` Add workflow to validate affected generated files | chahatsagarmain | 2025-02-12 |
| [#11537](https://github.com/kubeflow/pipelines/pull/11537) | Fix typo in documentation for contribution and developer guide | assu-2000 | 2025-01-26 |
| [#11533](https://github.com/kubeflow/pipelines/pull/11533) | update driver & launcher image handling | HumairAK | 2025-04-10 |
| [#11531](https://github.com/kubeflow/pipelines/pull/11531) | chore(release): bumped version to 2.4.0 | HumairAK | 2025-01-16 |
| [#11530](https://github.com/kubeflow/pipelines/pull/11530) | switch release/api generator images to ghcr (#11528) | HumairAK | 2025-01-16 |
| [#11528](https://github.com/kubeflow/pipelines/pull/11528) | chore: switch release/api generator images to ghcr | HumairAK | 2025-01-16 |
| [#11522](https://github.com/kubeflow/pipelines/pull/11522) | add remaining dockerfiles to build workflow | HumairAK | 2025-01-15 |
| [#11521](https://github.com/kubeflow/pipelines/pull/11521) | fix: Update broken api-connect link | dandawg | 2025-01-26 |
| [#11511](https://github.com/kubeflow/pipelines/pull/11511) | docs(backend): improved backend README | dandawg | 2025-01-29 |
| [#11499](https://github.com/kubeflow/pipelines/pull/11499) | chore: Add instructions to remote debug the Driver pods | mprahl | 2025-01-09 |
| [#11496](https://github.com/kubeflow/pipelines/pull/11496) | chore(test): Fix SDK tests | rimolive | 2025-01-02 |
| [#11490](https://github.com/kubeflow/pipelines/pull/11490) | feat(docs): Add architecture diagram | anishasthana | 2025-01-17 |
| [#11473](https://github.com/kubeflow/pipelines/pull/11473) | chore(deps): Update client-go and controller-runtime | mprahl | 2025-01-09 |
| [#11470](https://github.com/kubeflow/pipelines/pull/11470) | fix(backend): Use an Argo Workflow exit lifecycle hook for exit handlers | mprahl | 2025-01-10 |
| [#11411](https://github.com/kubeflow/pipelines/pull/11411) | fix(backend): Fix enable_caching issues when handling PVC creation/deletion | rimolive | 2025-01-16 |
| [#11278](https://github.com/kubeflow/pipelines/pull/11278) | feat(backend): configurable log level for driver / launcher images | CarterFendley | 2025-02-21 |
| [#10762](https://github.com/kubeflow/pipelines/pull/10762) | chore: bump requests-toolbelt to 1.0.0 | SimonDR-Boltzmann | 2025-01-24 |

### Automated dependency bumps (kubeflow/pipelines)

8 reviews of PRs authored by `dependabot[bot]`:

| PR | Title | Author | Merged |
| --- | --- | --- | --- |
| [#12531](https://github.com/kubeflow/pipelines/pull/12531) | chore(deps): bump urllib3 from 2.5.0 to 2.6.0 in /backend/metadata_writer | dependabot[bot] | 2025-12-08 |
| [#12066](https://github.com/kubeflow/pipelines/pull/12066) | chore(deps): bump golang.org/x/oauth2 from 0.0.0-20210628180205-a41e5a781914 to 0.27.0 in /test/tools/project-cleaner | dependabot[bot] | 2025-07-19 |
| [#11815](https://github.com/kubeflow/pipelines/pull/11815) | chore(deps): bump @babel/runtime-corejs3 from 7.12.5 to 7.27.0 in /frontend | dependabot[bot] | 2025-04-12 |
| [#11756](https://github.com/kubeflow/pipelines/pull/11756) | chore(deps): bump github.com/expr-lang/expr from 1.16.0 to 1.17.0 | dependabot[bot] | 2025-03-18 |
| [#11748](https://github.com/kubeflow/pipelines/pull/11748) | chore(deps): bump golang.org/x/net from 0.33.0 to 0.36.0 in /test/tools/project-cleaner | dependabot[bot] | 2025-03-17 |
| [#11747](https://github.com/kubeflow/pipelines/pull/11747) | chore(deps): bump @babel/helpers from 7.24.0 to 7.26.10 in /frontend | dependabot[bot] | 2025-03-31 |
| [#11732](https://github.com/kubeflow/pipelines/pull/11732) | chore(deps): bump axios from 1.6.0 to 1.8.2 in /frontend/server | dependabot[bot] | 2025-04-02 |
| [#11454](https://github.com/kubeflow/pipelines/pull/11454) | chore(deps): bump nanoid and mocha in /test/frontend-integration-test | dependabot[bot] | 2025-01-12 |

## Code reviews in kubeflow/pipelines-components

4 reviews of PRs from other human contributors:

| PR | Title | Author | Merged |
| --- | --- | --- | --- |
| [#49](https://github.com/kubeflow/pipelines-components/pull/49) | feat: Add automated component/pipeline skeleton generator with comprehensive tooling | nsingla | 2025-12-28 |
| [#14](https://github.com/kubeflow/pipelines-components/pull/14) | chore: Add basic Pull Request Template | gmfrasca | 2025-12-09 |
| [#7](https://github.com/kubeflow/pipelines-components/pull/7) | feat(scripts): Add README Generator script and accompanying README Sync Check | gmfrasca | 2025-12-06 |
| [#2](https://github.com/kubeflow/pipelines-components/pull/2) | Create initial documentation | gmfrasca | 2025-11-27 |

### Automated dependency bumps (kubeflow/pipelines-components)

3 reviews of PRs authored by `dependabot[bot]`:

| PR | Title | Author | Merged |
| --- | --- | --- | --- |
| [#44](https://github.com/kubeflow/pipelines-components/pull/44) | chore(deps): Bump actions/checkout from 4 to 6 | dependabot[bot] | 2025-12-22 |
| [#43](https://github.com/kubeflow/pipelines-components/pull/43) | chore(deps): Bump actions/upload-artifact from 5 to 6 | dependabot[bot] | 2025-12-22 |
| [#42](https://github.com/kubeflow/pipelines-components/pull/42) | chore(deps): Bump actions/setup-node from 4 to 6 | dependabot[bot] | 2025-12-22 |

## Open PRs

No open PRs in either repo.

## Governance — OWNERS roles

### kubeflow/pipelines

| Path | Approver | Reviewer |
| --- | --- | --- |
| `backend/` | Yes | Yes |
| `docs/` | Yes | — |
| `manifests/` | — | Yes |
| `test/` | Yes | — |
| `test_data/` | Yes | — |
| `.github/` | Yes | — |
| `kubernetes_platform/` | Yes | Yes |
| `sdk/python/kfp/kubernetes/` | Yes | Yes |
| `tools/` | — | Yes |

### kubeflow/pipelines-components

| Path | Approver | Reviewer |
| --- | --- | --- |
| `/` (root) | Yes | — |
| `docs/` | Yes | Yes |
| `scripts/` | Yes | Yes |
| `.github/` | Yes | Yes |
| `test_data/` | Yes | Yes |
| `test_data/pipelines/grouped/etl_flows/daily_ingest/` | Yes | — |
| `test_data/components/grouped/ml_models/linear_model/` | Yes | — |

## Merged PRs in kubeflow/pipelines-components

| PR | Title | Merged |
| --- | --- | --- |
| [#28](https://github.com/kubeflow/pipelines-components/pull/28) | ci: Removed validation of missing Containerfile for custom Kubeflow images | 2025-12-22 |
| [#40](https://github.com/kubeflow/pipelines-components/pull/40) | chore(ci): add Dependabot (uv + github-actions) | 2025-12-19 |
| [#34](https://github.com/kubeflow/pipelines-components/pull/34) | ci: Added path filters for config and dependency files | 2025-12-19 |
| [#32](https://github.com/kubeflow/pipelines-components/pull/32) | chore: Added semver to ci dependencies and clean up dev dependencies | 2025-12-19 |
| [#23](https://github.com/kubeflow/pipelines-components/pull/23) | chore: Bump `kfp` to 2.15.0 | 2025-12-11 |
| [#31](https://github.com/kubeflow/pipelines-components/pull/31) | chore: Fixed all linting errors and added comprehensive docstrings | 2025-12-17 |
| [#30](https://github.com/kubeflow/pipelines-components/pull/30) | chore: Added --fix flags to pre-commit hooks for auto-fixing | 2025-12-17 |
| [#10](https://github.com/kubeflow/pipelines-components/pull/10) | Added `validate_base_images` script, tests, and GitHub workflow | 2025-12-15 |
| [#9](https://github.com/kubeflow/pipelines-components/pull/9) | Added unit test infrastructure for CI scripts | 2025-12-03 |
| [#3](https://github.com/kubeflow/pipelines-components/pull/3) | Added `pyproject.toml` files for core and third-party packages, implemented CI for building and testing Python packages | 2025-11-27 |
| [#19](https://github.com/kubeflow/pipelines-components/pull/19) | Fixed typos in CONTRIBUTING.md | 2025-12-05 |
| [#18](https://github.com/kubeflow/pipelines-components/pull/18) | Consolidated Python and actions versions | 2025-12-05 |
| [#4](https://github.com/kubeflow/pipelines-components/pull/4) | Add initial GitHub Actions workflow placeholder | 2025-11-06 |
| [#1](https://github.com/kubeflow/pipelines-components/pull/1) | Add initialization files for core and third-party Kubeflow Pipelines components and pipelines, restructure repository, update `.gitignore`, and enhance `README.md` | 2025-11-06 |

## Contribution highlights

### Architecture and design contributions

- Authored [KEP-12513: Filesystem-Based Artifact Storage for Kubeflow Pipelines](https://github.com/kubeflow/pipelines/issues/12513) — a major architectural proposal to move artifact storage to a filesystem-based approach.
- Implemented HTTP artifact streaming to prevent OOM errors with large files ([#12394](https://github.com/kubeflow/pipelines/pull/12394)) and fixed the artifact client's JSON/base64 handling ([#12467](https://github.com/kubeflow/pipelines/pull/12467)).
- Filed [#12439](https://github.com/kubeflow/pipelines/issues/12439) to encapsulate the `v2/objectstore` package and prevent usage outside the v2 execution engine — protecting architectural boundaries.
- Added a global cache enable/disable option to the backend ([#11831](https://github.com/kubeflow/pipelines/pull/11831)) and proxy support for accessing external resources ([#11771](https://github.com/kubeflow/pipelines/pull/11771)).

### CI/CD ownership

- Drove the modernization of CI: replaced unmaintained rerun actions, upgraded runners, and improved path filtering ([#11784](https://github.com/kubeflow/pipelines/pull/11784), [#11786](https://github.com/kubeflow/pipelines/pull/11786), [#11796](https://github.com/kubeflow/pipelines/pull/11796), [#11806](https://github.com/kubeflow/pipelines/pull/11806)).
- Upgraded Argo Workflows to v3.6.7 and Golang to 1.24 ([#12072](https://github.com/kubeflow/pipelines/pull/12072)), then switched Argo manifests to remote Git references ([#12074](https://github.com/kubeflow/pipelines/pull/12074)).
- Fixed log collection and test reliability across the CI suite ([#11773](https://github.com/kubeflow/pipelines/pull/11773), [#11775](https://github.com/kubeflow/pipelines/pull/11775), [#11779](https://github.com/kubeflow/pipelines/pull/11779), [#11910](https://github.com/kubeflow/pipelines/pull/11910), [#11911](https://github.com/kubeflow/pipelines/pull/11911), [#11916](https://github.com/kubeflow/pipelines/pull/11916)).
- Built the entire CI/CD foundation of the new `kubeflow/pipelines-components` repo: initial repo structure, Python package builds, unit test infrastructure, Dependabot, linting, and image validation ([#1](https://github.com/kubeflow/pipelines-components/pull/1), [#3](https://github.com/kubeflow/pipelines-components/pull/3), [#9](https://github.com/kubeflow/pipelines-components/pull/9), [#10](https://github.com/kubeflow/pipelines-components/pull/10), [#30](https://github.com/kubeflow/pipelines-components/pull/30), [#31](https://github.com/kubeflow/pipelines-components/pull/31), [#40](https://github.com/kubeflow/pipelines-components/pull/40)).

### Community and mentoring

- 103 human code reviews across both repos, from 35+ distinct contributors — acting as a primary quality gate for the project.
- Extensive OWNERS footprint: approver on 9 paths in `kubeflow/pipelines` (including `backend/`, `test/`, `kubernetes_platform/`, `docs/`) and root approver of `kubeflow/pipelines-components`.
- 41 issues filed, including a 20-issue campaign to standardize CI workflows on `make` commands ([#11686](https://github.com/kubeflow/pipelines/issues/11686)–[#11706](https://github.com/kubeflow/pipelines/issues/11706)), plus feature requests that drove shipped work (global cache, proxy support, pipeline deletion with versions).
