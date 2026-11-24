# Kubeflow Pipelines Contribution Report — Helber Belmiro (@hbelmiro)

**Period:** January 2026 – November 2026

## Summary

| Area                                              | Count             |
|---------------------------------------------------|-------------------|
| PRs merged in kubeflow/pipelines                  | 48                |
| PRs reviewed in kubeflow/pipelines (others' PRs)  | 71 (+2 Dependabot) |
| Issues filed in kubeflow/pipelines                | 19                |
| PRs merged in kubeflow/pipelines-components       | 22                |
| PRs reviewed in kubeflow/pipelines-components (others' PRs) | 15 (+38 Dependabot) |
| Lines changed in kubeflow/pipelines               | +20,268 / -8,536 |
| Lines changed in kubeflow/pipelines-components    | +5,471 / -1,050  |
| Open PRs                                          | 0                 |

---

## kubeflow/pipelines — Merged PRs by Area

### Backend — Bug Fixes and Features

| PR | Title | Merged |
|----|-------|--------|
| [#15168](https://github.com/kubeflow/pipelines/pull/15168) | feat(backend): configurable default StorageClass for CreatePVC tasks | 2026-10-27 |
| [#15024](https://github.com/kubeflow/pipelines/pull/15024) | fix(backend): stop defaulting CreatePVC storage class to "standard" | 2026-10-23 |
| [#14181](https://github.com/kubeflow/pipelines/pull/14181) | fix(backend): add service account authorization for runs and recurring runs | 2026-08-27 |
| [#13931](https://github.com/kubeflow/pipelines/pull/13931) | fix(backend): break infinite loop in isV2Spec on malformed YAML | 2026-08-05 |
| [#13885](https://github.com/kubeflow/pipelines/pull/13885) | fix(backend): reject runAsUser=0 at API level instead of deferring to kubelet | 2026-08-07 |
| [#13740](https://github.com/kubeflow/pipelines/pull/13740) | fix: Key processedPipelines by pipeline UUID instead of version name | 2026-07-16 |
| [#13552](https://github.com/kubeflow/pipelines/pull/13552) | fix: allow same-named pipeline versions under different pipelines (#13534, #13535, #13556) | 2026-06-26 |
| [#13315](https://github.com/kubeflow/pipelines/pull/13315) | fix(backend): fixes AWS SDK v2 checksum validation | 2026-04-24 |
| [#13158](https://github.com/kubeflow/pipelines/pull/13158) | fix(backend): Wire `MANAGED_PIPELINES_UPLOAD_TAGS` into `LoadSamples` | 2026-04-01 |
| [#13124](https://github.com/kubeflow/pipelines/pull/13124) | feat(backend): Improve pod name resolution for pipelines with long names and enhance test coverage | 2026-03-25 |
| [#12928](https://github.com/kubeflow/pipelines/pull/12928) | fix(backend): Added path traversal mitigation to DownloadBlob and improve unit test coverage | 2026-03-03 |
| [#12665](https://github.com/kubeflow/pipelines/pull/12665) | fix(backend): Refactor S3 bucket management by replacing MinIO client code with AWS SDK v2 and improving configuration validation | 2026-01-19 |
| [#12512](https://github.com/kubeflow/pipelines/pull/12512) | fix(backend): Refactor S3 bucket management by replacing MinIO client code with AWS SDK v2 and improving configuration validation | 2026-01-16 |

### Backend — API, Protobuf, and Architecture

| PR | Title | Merged |
|----|-------|--------|
| [#14243](https://github.com/kubeflow/pipelines/pull/14243) | feat(dra): add Dynamic Resource Allocation support to KFP | 2026-09-10 |
| [#14037](https://github.com/kubeflow/pipelines/pull/14037) | doc: add KEP for Dynamic Resource Allocation (DRA) support | 2026-08-31 |
| [#13722](https://github.com/kubeflow/pipelines/pull/13722) | refactor(backend): centralize V1 pipeline blocking into IsV1PipelinesBlocked | 2026-07-27 |
| [#13563](https://github.com/kubeflow/pipelines/pull/13563) | fix(ci): regenerate API files for grpc-gateway v2.28.0 and harden CI workflows | 2026-06-19 |
| [#12919](https://github.com/kubeflow/pipelines/pull/12919) | feat(backend): Add plugin input/output fields to RecurringRun and Run protobufs | 2026-03-09 |

### CI/CD and Infrastructure

| PR | Title | Merged |
|----|-------|--------|
| [#15914](https://github.com/kubeflow/pipelines/pull/15914) | chore(deps): update transitive dependencies via Dependabot | 2026-11-24 |
| [#15695](https://github.com/kubeflow/pipelines/pull/15695) | fix(ci): close cert-manager install race in TLS-enabled lanes | 2026-11-20 |
| [#15768](https://github.com/kubeflow/pipelines/pull/15768) | fix(ci): format ci_pass_eligibility_test.py with ruff | 2026-11-18 |
| [#15169](https://github.com/kubeflow/pipelines/pull/15169) | fix(ci): pin pre-commit lint hooks to Python 3.11 | 2026-10-26 |
| [#14351](https://github.com/kubeflow/pipelines/pull/14351) | ci: align isort version | 2026-09-30 |
| [#13771](https://github.com/kubeflow/pipelines/pull/13771) | ci: build API generator from source in CI to prevent stale files | 2026-07-27 |
| [#13685](https://github.com/kubeflow/pipelines/pull/13685) | fix(ci): make image rebuild step actually run after build failure | 2026-07-08 |
| [#13629](https://github.com/kubeflow/pipelines/pull/13629) | fix(ci): prevent ci-passed label when workflows await approval | 2026-07-02 |
| [#13470](https://github.com/kubeflow/pipelines/pull/13470) | chore: Removed non-needed package installation steps from backend Dockerfiles | 2026-06-08 |
| [#13431](https://github.com/kubeflow/pipelines/pull/13431) | chore: refactor Go setup into reusable composite action | 2026-05-26 |
| [#13421](https://github.com/kubeflow/pipelines/pull/13421) | chore: bump Go version to 1.26.2 | 2026-05-20 |
| [#13295](https://github.com/kubeflow/pipelines/pull/13295) | fix(ci): Add `proxy` parameter to e2e-test workflow deployment and test steps - Fixes #13294 | 2026-04-21 |
| [#13247](https://github.com/kubeflow/pipelines/pull/13247) | fix(ci): Update Profile Controller manifest URL in deploy script | 2026-04-10 |
| [#12810](https://github.com/kubeflow/pipelines/pull/12810) | chore(ci): Reverted changes in the CI check workflow from PR #12793 | 2026-02-16 |
| [#12773](https://github.com/kubeflow/pipelines/pull/12773) | chore(ci): Update image-build workflow to use `github.run_id` for artifact path | 2026-02-06 |
| [#12772](https://github.com/kubeflow/pipelines/pull/12772) | chore(ci): Refine SeaweedFS S3 auth setup and enhance wait logic in deployment scripts | 2026-02-10 |
| [#12769](https://github.com/kubeflow/pipelines/pull/12769) | chore(ci): Simplify image-build workflow by removing caching logic | 2026-02-05 |
| [#12712](https://github.com/kubeflow/pipelines/pull/12712) | chore(ci): Replace GitHub REST API calls with event payload and cache lookups | 2026-01-27 |
| [#12698](https://github.com/kubeflow/pipelines/pull/12698) | chore(ci): use author_association to avoid API rate limits in approve workflow | 2026-01-27 |
| [#12658](https://github.com/kubeflow/pipelines/pull/12658) | chore(tests): Optimize workflows with caching and action upgrades | 2026-01-21 |
| [#12540](https://github.com/kubeflow/pipelines/pull/12540) | chore(CI): Embed Argo Workflow logs into HTML test reports | 2026-01-12 |

### Test Reliability

| PR | Title | Merged |
|----|-------|--------|
| [#13593](https://github.com/kubeflow/pipelines/pull/13593) | fix(test): replace single-shot MLflow status checks with polling | 2026-06-25 |
| [#13312](https://github.com/kubeflow/pipelines/pull/13312) | fix(test): simplify and stabilize pipeline test cleanup | 2026-04-30 |
| [#13253](https://github.com/kubeflow/pipelines/pull/13253) | fix(test): Add `Eventually` for informer cache sync in pipeline version tests (#13312) | 2026-04-10 |
| [#12979](https://github.com/kubeflow/pipelines/pull/12979) | Revert "chore: migrate build system from pip/setup.py to uv workspace…" | 2026-03-06 |

### SDK

| PR | Title | Merged |
|----|-------|--------|
| [#14726](https://github.com/kubeflow/pipelines/pull/14726) | chore(deps): relax `requests` dependency to `>=2.33.0,<3` in Python SDK | 2026-10-07 |
| [#12741](https://github.com/kubeflow/pipelines/pull/12741) | chore(sdk): Add deprecation notice to `add_node_selector_constraint` docstring | 2026-01-30 |

### Maintenance and Governance

| PR | Title | Merged |
|----|-------|--------|
| [#13932](https://github.com/kubeflow/pipelines/pull/13932) | docs(AGENTS.md): add comment and documentation policy | 2026-08-06 |
| [#13389](https://github.com/kubeflow/pipelines/pull/13389) | chore: update OWNERS files to remove inactive reviewers and approvers | 2026-05-12 |
| [#12809](https://github.com/kubeflow/pipelines/pull/12809) | chore(test): Align test/ and test_data/ OWNERS with .github/OWNERS | 2026-02-16 |

## kubeflow/pipelines — Issues Filed (19)

| Issue | Title | State | Filed |
|-------|-------|-------|-------|
| [#15086](https://github.com/kubeflow/pipelines/issues/15086) | feat(backend): configurable default StorageClass for CreatePVC | closed | 2026-10-23 |
| [#14036](https://github.com/kubeflow/pipelines/issues/14036) | feat(sdk): KEP - Dynamic Resource Allocation (DRA) Support | closed | 2026-08-13 |
| [#13926](https://github.com/kubeflow/pipelines/issues/13926) | Malformed YAML upload causes infinite loop in isV2Spec and permanent goroutine leak | closed | 2026-07-29 |
| [#13592](https://github.com/kubeflow/pipelines/issues/13592) | Flaky MLflow E2E tests: single-shot status checks race with async MLflow updates | closed | 2026-06-25 |
| [#13566](https://github.com/kubeflow/pipelines/issues/13566) | Add concurrency groups to PR-triggered workflows to cancel stale runs | closed | 2026-06-19 |
| [#13565](https://github.com/kubeflow/pipelines/issues/13565) | Add timeout-minutes to image-builds and e2e-test-frontend workflows | closed | 2026-06-19 |
| [#13564](https://github.com/kubeflow/pipelines/issues/13564) | MLflow E2E tests failing: deploy action pinned to stale commit | closed | 2026-06-19 |
| [#13561](https://github.com/kubeflow/pipelines/issues/13561) | validate-generated-files CI broken on master since grpc-gateway v2.28.0 bump | closed | 2026-06-19 |
| [#13556](https://github.com/kubeflow/pipelines/issues/13556) | LoadSamples skips pipeline version creation when pipeline exists with empty namespace | closed | 2026-06-18 |
| [#13535](https://github.com/kubeflow/pipelines/issues/13535) | GetPipelineVersionByName returns wrong version when multiple pipelines have same-named versions | closed | 2026-06-16 |
| [#13534](https://github.com/kubeflow/pipelines/issues/13534) | Kubernetes store cannot create same-named pipeline versions under different pipelines | closed | 2026-06-16 |
| [#13314](https://github.com/kubeflow/pipelines/issues/13314) | [backend] S3 operations fail with non-AWS object stores after AWS SDK v2 checksum defaults change | closed | 2026-04-24 |
| [#13294](https://github.com/kubeflow/pipelines/issues/13294) | chore(test): HTTP proxy must match between deploy and E2E Ginkgo (`-useProxy`) | closed | 2026-04-21 |
| [#13252](https://github.com/kubeflow/pipelines/issues/13252) | fix(test): Flaky pipeline version sorting tests due to K8s store informer cache lag | closed | 2026-04-10 |
| [#12949](https://github.com/kubeflow/pipelines/issues/12949) | chore(backend): Consolidate v2 placeholder resolution into shared utility | open | 2026-03-02 |
| [#12913](https://github.com/kubeflow/pipelines/issues/12913) | chore(<backend>): Flaky test: TestCacheSingleRunWithPVC_SameName_Caches times out on Kind clusters | closed | 2026-02-25 |
| [#12771](https://github.com/kubeflow/pipelines/issues/12771) | [bug] SeaweedFS S3 Authentication Race Condition in CI | closed | 2026-02-05 |
| [#12725](https://github.com/kubeflow/pipelines/issues/12725) | chore(<backend>): Refactor Driver and Launcher: Make All Parameters Required | closed | 2026-01-29 |
| [#12686](https://github.com/kubeflow/pipelines/issues/12686) | chore(sdk): Migrate Python dependency management to uv workspaces | closed | 2026-01-21 |

## kubeflow/pipelines — Code Reviews (71 PRs from other contributors)

| PR | Title | Author | Merged |
|----|-------|--------|--------|
| [#15771](https://github.com/kubeflow/pipelines/pull/15771) | fix(ci): read queue conversation policy with workflow permissions | @jeffspahr | 2026-11-18 |
| [#12987](https://github.com/kubeflow/pipelines/pull/12987) | feat: fail pipeline runs on image pull failures | @jsonmp-k8 | 2026-10-27 |
| [#14713](https://github.com/kubeflow/pipelines/pull/14713) | fix(deps): align Dependabot ownership and remove tracked workspace exports | @jeffspahr | 2026-10-13 |
| [#12379](https://github.com/kubeflow/pipelines/pull/12379) | feat(backend): postgres integration | @kaikaila | 2026-09-08 |
| [#13891](https://github.com/kubeflow/pipelines/pull/13891) | fix(backend): make remaining kind-cluster wait timeouts configurable | @Sharkyii | 2026-08-26 |
| [#13711](https://github.com/kubeflow/pipelines/pull/13711) | chore(backend): validate required driver and launcher flags | @Priyanshu-u07 | 2026-08-11 |
| [#13836](https://github.com/kubeflow/pipelines/pull/13836) | fix(backend): propagate request context to archived log reads | @Sharkyii | 2026-08-10 |
| [#13935](https://github.com/kubeflow/pipelines/pull/13935) | fix(backend): close SQL rows on all early return paths in storage layer | @shivv23 | 2026-08-05 |
| [#13913](https://github.com/kubeflow/pipelines/pull/13913) | fix(backend): propagate ctx instead of using context.TODO/Background in PVC operations | @shivv23 | 2026-08-05 |
| [#13930](https://github.com/kubeflow/pipelines/pull/13930) | test(e2e): add Kind GPU scheduling check with Fake GPU Operator | @sduvvuri1603 | 2026-08-03 |
| [#13918](https://github.com/kubeflow/pipelines/pull/13918) | fix(backend): propagate error when scanRowsToRuns fails | @Sharkyii | 2026-07-29 |
| [#13773](https://github.com/kubeflow/pipelines/pull/13773) | fix(backend):Make kind-cluster-agnostic timeouts configurable | @Daniel-1600 | 2026-07-27 |
| [#13838](https://github.com/kubeflow/pipelines/pull/13838) | fix(backend): log the actual bucket close error, not the outer fetch error | @Sharkyii | 2026-07-27 |
| [#13839](https://github.com/kubeflow/pipelines/pull/13839) | fix(backend): return permanent error when token refresh fails in ReportRunMetrics | @Sharkyii | 2026-07-27 |
| [#13609](https://github.com/kubeflow/pipelines/pull/13609) | feat: add TLS MinVersion and cipher suite CLI flags to apiserver | @ugiordan | 2026-07-24 |
| [#13799](https://github.com/kubeflow/pipelines/pull/13799) | chore: apply gofmt formatting corrections in backend Go files | @kaikaila | 2026-07-24 |
| [#12417](https://github.com/kubeflow/pipelines/pull/12417) | feat: Support driver pod labels and annotations configuration at API server startup | @thc1006 | 2026-07-23 |
| [#13735](https://github.com/kubeflow/pipelines/pull/13735) | CI: Add execute permissions to .github/scripts/ai_triage.sh | @mprahl | 2026-07-15 |
| [#13695](https://github.com/kubeflow/pipelines/pull/13695) | test: authenticate and retry raw.githubusercontent.com URL verification | @jeffspahr | 2026-07-15 |
| [#13697](https://github.com/kubeflow/pipelines/pull/13697) | ci: authenticate googleapis proto fetches to avoid 429 rate limits | @jeffspahr | 2026-07-11 |
| [#13656](https://github.com/kubeflow/pipelines/pull/13656) | fix(backend): fall back to direct module fetch on Go proxy errors | @jeffspahr | 2026-07-10 |
| [#13693](https://github.com/kubeflow/pipelines/pull/13693) | ci: give legacy v2 integration tests an intentional time budget | @jeffspahr | 2026-07-10 |
| [#13655](https://github.com/kubeflow/pipelines/pull/13655) | ci: stop fail-fast from cancelling image builds and their retries | @jeffspahr | 2026-07-09 |
| [#12491](https://github.com/kubeflow/pipelines/pull/12491) | documentation: Update installation options | @gorkem | 2026-07-03 |
| [#13345](https://github.com/kubeflow/pipelines/pull/13345) | fix(backend): prevent premature workflow GC due to DB write race condition (#13342) | @shreeharshshinde | 2026-07-01 |
| [#13577](https://github.com/kubeflow/pipelines/pull/13577) | fix(backend): stream bounded object store reads | @jeffspahr | 2026-06-30 |
| [#13464](https://github.com/kubeflow/pipelines/pull/13464) | chore(deps): bump remaining backend Go builder images to golang:1.26.3 | @tolgatuncoglu | 2026-06-01 |
| [#13009](https://github.com/kubeflow/pipelines/pull/13009) | feat(frontend,backend): show actual retry start time for pipeline runs. Fixes #12845 | @Sridhar1030 | 2026-05-29 |
| [#13437](https://github.com/kubeflow/pipelines/pull/13437) | fix(backend): resolve artifact OneOf outputs at runtime (#13436) | @mprahl | 2026-05-28 |
| [#13325](https://github.com/kubeflow/pipelines/pull/13325) | fix(backend): apply recurring run service account unconditionally | @neo99zhang | 2026-05-20 |
| [#13307](https://github.com/kubeflow/pipelines/pull/13307) | chore(backend): Fix MLflow tags,nested run status update | @VaniHaripriya | 2026-05-12 |
| [#13359](https://github.com/kubeflow/pipelines/pull/13359) | Add alyssacgoins as a backend approver. | @alyssacgoins | 2026-05-07 |
| [#13298](https://github.com/kubeflow/pipelines/pull/13298) | chore(backend):Add RetryRun support to RunClient | @VaniHaripriya | 2026-05-07 |
| [#13352](https://github.com/kubeflow/pipelines/pull/13352) | chore: adding myself as backend approver | @nsingla | 2026-05-05 |
| [#13137](https://github.com/kubeflow/pipelines/pull/13137) | fix(backend): validate pipeline names in K8s store before API call | @Priyanshu-u07 | 2026-05-04 |
| [#12970](https://github.com/kubeflow/pipelines/pull/12970) | feat(manifests): add init containers for startup ordering to all critical deployments | @jsonmp-k8 | 2026-04-29 |
| [#13227](https://github.com/kubeflow/pipelines/pull/13227) | ci: preload Kind images instead of pushing via local registry | @jeffspahr | 2026-04-17 |
| [#12696](https://github.com/kubeflow/pipelines/pull/12696) | feat(kubernetes_platform): add data_source parameter to CreatePVC. Fixes #11420 | @khushiiagrawal | 2026-04-16 |
| [#12836](https://github.com/kubeflow/pipelines/pull/12836) | chore: Use make commands in https://github.com/kubeflow/pipelines/blo… | @matheusandre1 | 2026-04-10 |
| [#12776](https://github.com/kubeflow/pipelines/pull/12776) | fix(cli): remove unused namespace in `run.py` | @puwun | 2026-04-10 |
| [#12860](https://github.com/kubeflow/pipelines/pull/12860) | fix(frontend): Prevent Unauthorized Cross-Namespace Artifact Access (rebased, security-hardened) | @Raakshass | 2026-04-08 |
| [#13201](https://github.com/kubeflow/pipelines/pull/13201) | test(backend): increase apiserver/client test coverage to 62.3% | @jsonmp-k8 | 2026-04-07 |
| [#13203](https://github.com/kubeflow/pipelines/pull/13203) | test(backend): increase apiserver/template test coverage to 64.5% | @jsonmp-k8 | 2026-04-07 |
| [#13223](https://github.com/kubeflow/pipelines/pull/13223) | chore(ci): increase the number of parallel threads for e2e tests | @nsingla | 2026-04-06 |
| [#12755](https://github.com/kubeflow/pipelines/pull/12755) | chore(test): use make commands in `sdk-component-yaml` | @puwun | 2026-03-31 |
| [#12999](https://github.com/kubeflow/pipelines/pull/12999) | feat(backend): Add option to apply tags to create, upload pipelines and create pipeline version. Also allow filtering on the tag when fetching resources | @nsingla | 2026-03-20 |
| [#12823](https://github.com/kubeflow/pipelines/pull/12823) | chore(ci): upgrade GitHub Actions to latest major versions | @jsonmp-k8 | 2026-03-19 |
| [#13046](https://github.com/kubeflow/pipelines/pull/13046) | ci: workflow fixes | @nsingla | 2026-03-17 |
| [#12598](https://github.com/kubeflow/pipelines/pull/12598) | fix(backend): resolve IfPresent conditions in component.yaml. Fixes #11009 | @khushiiagrawal | 2026-03-12 |
| [#12833](https://github.com/kubeflow/pipelines/pull/12833) | fix: correct typo pipline_func_args -> pipeline_func_args in pipeline… | @sduvvuri1603 | 2026-03-10 |
| [#12971](https://github.com/kubeflow/pipelines/pull/12971) | fix(test): re-enable and add all snapshot tests for kfp-kubernetes | @jsonmp-k8 | 2026-03-06 |
| [#12770](https://github.com/kubeflow/pipelines/pull/12770) | chore: migrate build system from pip/setup.py to uv workspaces (#12686) | @sh4shv4t | 2026-03-06 |
| [#12862](https://github.com/kubeflow/pipelines/pull/12862) | doc: Add a KEP for native MLflow integration in KFP | @mprahl | 2026-03-03 |
| [#12916](https://github.com/kubeflow/pipelines/pull/12916) | chore(backend): Increase timeout for PVC cache test to reduce flakiness | @aniketpati1121 | 2026-02-27 |
| [#12911](https://github.com/kubeflow/pipelines/pull/12911) | chore(test): add jeffspahr to test OWNERS approvers | @jeffspahr | 2026-02-25 |
| [#12905](https://github.com/kubeflow/pipelines/pull/12905) | chore: upgrading go to 1.25.7 as it has many security fixes | @nsingla | 2026-02-25 |
| [#12607](https://github.com/kubeflow/pipelines/pull/12607) | feat(backend): add Literal parameter validation in API Server and Driver. Fixes #12602 | @khushiiagrawal | 2026-02-18 |
| [#12793](https://github.com/kubeflow/pipelines/pull/12793) | chore(frontend): upgrade material-ui to v4 | @jeffspahr | 2026-02-15 |
| [#12766](https://github.com/kubeflow/pipelines/pull/12766) | test: fix ray pipeline and lower casing pipeline names in upgrade tests | @nsingla | 2026-02-13 |
| [#12792](https://github.com/kubeflow/pipelines/pull/12792) | Fix SeaweedFS IAM endpoint in profile controller | @sduvvuri1603 | 2026-02-13 |
| [#12613](https://github.com/kubeflow/pipelines/pull/12613) | chore: Remove minio | @akagami-harsh | 2026-02-11 |
| [#12781](https://github.com/kubeflow/pipelines/pull/12781) |  docs : replace broken project argo link with offical argo workflow d… | @aniketpati1121 | 2026-02-10 |
| [#12768](https://github.com/kubeflow/pipelines/pull/12768) | feat(ci): optimize copilot reviews | @droctothorpe | 2026-02-05 |
| [#12764](https://github.com/kubeflow/pipelines/pull/12764) | ci: add pr number to the cache key | @nsingla | 2026-02-04 |
| [#12753](https://github.com/kubeflow/pipelines/pull/12753) | docs: fix broken Kubeflow Pipelines installation link | @aniketpati1121 | 2026-02-02 |
| [#12735](https://github.com/kubeflow/pipelines/pull/12735) | fix(testing) retention for image-builds-with-cache artifacts | @alyssacgoins | 2026-01-29 |
| [#12710](https://github.com/kubeflow/pipelines/pull/12710) | ci: adding myself as reviewer and approver for github workflows & actions | @nsingla | 2026-01-27 |
| [#12694](https://github.com/kubeflow/pipelines/pull/12694) | Fix: pip upgrade in backend API Dockerfile | @sduvvuri1603 | 2026-01-23 |
| [#12657](https://github.com/kubeflow/pipelines/pull/12657) | fix(ci): port-forward minio-service instead of pod | @kaikaila | 2026-01-16 |
| [#12631](https://github.com/kubeflow/pipelines/pull/12631) | chore: remove disabled renovate.json5 config | @jeffspahr | 2026-01-09 |
| [#12572](https://github.com/kubeflow/pipelines/pull/12572) | Update CA Cert Conditional | @alyssacgoins | 2026-01-05 |

### Automated dependency bumps reviewed (Dependabot) (2)

| PR | Title | Author | Merged |
|----|-------|--------|--------|
| [#14634](https://github.com/kubeflow/pipelines/pull/14634) | chore(deps): bump golang in /backend | @dependabot[bot] | 2026-10-02 |
| [#12629](https://github.com/kubeflow/pipelines/pull/12629) | chore(deps): bump werkzeug from 3.1.3 to 3.1.5 in /backend/src/apiserver/visualization | @dependabot[bot] | 2026-01-09 |

## kubeflow/pipelines — Open PRs

No open PRs — all authored work has been merged or closed.

## kubeflow/pipelines-components — Merged PRs (22)

| PR | Title | Merged |
|----|-------|--------|
| [#218](https://github.com/kubeflow/pipelines-components/pull/218) | ci: install gh CLI in jobs that use it | 2026-11-04 |
| [#213](https://github.com/kubeflow/pipelines-components/pull/213) | fix: remove stale kfp_components root package entries | 2026-10-20 |
| [#193](https://github.com/kubeflow/pipelines-components/pull/193) | Add hbelmiro to approvers list in OWNERS file | 2026-08-05 |
| [#186](https://github.com/kubeflow/pipelines-components/pull/186) | fix(scripts): move tests into tests/ for CI discovery | 2026-07-23 |
| [#182](https://github.com/kubeflow/pipelines-components/pull/182) | fix(ci): regenerate stale golden READMEs and trigger tests on test_data changes | 2026-07-15 |
| [#178](https://github.com/kubeflow/pipelines-components/pull/178) | chore: Updated stale readme | 2026-07-02 |
| [#163](https://github.com/kubeflow/pipelines-components/pull/163) | ci: Remove `OWNERS` file exclusion from `readme-check.yml` paths-ignore | 2026-05-28 |
| [#161](https://github.com/kubeflow/pipelines-components/pull/161) | chore: Update OWNERS files with current team roster | 2026-05-27 |
| [#159](https://github.com/kubeflow/pipelines-components/pull/159) | ci: Ignore `OWNERS` file changes in workflow triggers | 2026-05-26 |
| [#140](https://github.com/kubeflow/pipelines-components/pull/140) | ci: Refactor environment variable usage in workflows | 2026-04-14 |
| [#139](https://github.com/kubeflow/pipelines-components/pull/139) | ci: Update actions to pinned versions in workflows | 2026-04-14 |
| [#122](https://github.com/kubeflow/pipelines-components/pull/122) | ci: Trust Dependabot for CI checks and improve bot handling | 2026-03-17 |
| [#115](https://github.com/kubeflow/pipelines-components/pull/115) | ci: Add workflows for CI label management and approvals | 2026-03-13 |
| [#70](https://github.com/kubeflow/pipelines-components/pull/70) | chore: Move `pyyaml` from core dependencies to optional test dependencies | 2026-01-14 |
| [#67](https://github.com/kubeflow/pipelines-components/pull/67) | chore: Added release branch support to CI workflows | 2026-02-03 |
| [#65](https://github.com/kubeflow/pipelines-components/pull/65) | Allow top-level kfp_components imports and clarify Import Guard guidance | 2026-01-09 |
| [#59](https://github.com/kubeflow/pipelines-components/pull/59) | chore: Unpinned test dependencies, add uv.lock sync check in pre-commit and CI | 2026-01-06 |
| [#57](https://github.com/kubeflow/pipelines-components/pull/57) | refactor: Consolidate reusable utility functions into `scripts/lib` | 2026-01-07 |
| [#53](https://github.com/kubeflow/pipelines-components/pull/53) | chore: replace 'uv run python' with 'uv run' across repo | 2026-01-02 |
| [#51](https://github.com/kubeflow/pipelines-components/pull/51) | docs: Added AI agent guidance | 2026-02-02 |
| [#50](https://github.com/kubeflow/pipelines-components/pull/50) | test: Standardize test imports to use relative imports | 2026-01-02 |
| [#8](https://github.com/kubeflow/pipelines-components/pull/8) | Added CI workflows for building, validating, and testing custom base images | 2026-01-23 |

## kubeflow/pipelines-components — Code Reviews (15 PRs from other contributors)

| PR | Title | Author | Merged |
|----|-------|--------|--------|
| [#201](https://github.com/kubeflow/pipelines-components/pull/201) | fix: allow pytest to run in git worktrees | @Ehtasham-Yasin | 2026-10-02 |
| [#200](https://github.com/kubeflow/pipelines-components/pull/200) | fix: reject future metadata verification dates | @Ehtasham-Yasin | 2026-10-02 |
| [#199](https://github.com/kubeflow/pipelines-components/pull/199) | fix(scripts): handle empty metadata.yaml in check_component_freshness. Fixes #198 | @rautaditya2606 | 2026-10-02 |
| [#180](https://github.com/kubeflow/pipelines-components/pull/180) | chore: Introduce jsonschema for metadata files validation | @filip-komarzyniec | 2026-08-10 |
| [#127](https://github.com/kubeflow/pipelines-components/pull/127) | feat(ci): add container build matrix check. Fixes #119 | @prachimaskar | 2026-05-27 |
| [#151](https://github.com/kubeflow/pipelines-components/pull/151) | ci(fix): fixing cyclic dependency in check ci status | @nsingla | 2026-05-07 |
| [#141](https://github.com/kubeflow/pipelines-components/pull/141) | ci: Remove workflow branch filters so CI runs on all target branches | @VaniHaripriya | 2026-04-15 |
| [#88](https://github.com/kubeflow/pipelines-components/pull/88) | feat: sdg component | @beatsmonster | 2026-04-07 |
| [#94](https://github.com/kubeflow/pipelines-components/pull/94) | feat: Add Components and Pipelines Subcategories Support | @VaniHaripriya | 2026-02-25 |
| [#83](https://github.com/kubeflow/pipelines-components/pull/83) | fix: Tighten compile-check metadata helpers and Workflow triggers | @sduvvuri1603 | 2026-01-23 |
| [#13](https://github.com/kubeflow/pipelines-components/pull/13) | Add compile check tooling and CI workflow | @sduvvuri1603 | 2026-01-22 |
| [#29](https://github.com/kubeflow/pipelines-components/pull/29) | Add a CI check to ensure packages entries in pyproject.toml are up to date | @VaniHaripriya | 2026-01-12 |
| [#35](https://github.com/kubeflow/pipelines-components/pull/35) | feat(scripts): Write script to check and report component/pipeline freshness | @gmfrasca | 2026-01-09 |
| [#56](https://github.com/kubeflow/pipelines-components/pull/56) | fix(CI): Add missing CI dependencies and pin them | @mprahl | 2026-01-05 |
| [#55](https://github.com/kubeflow/pipelines-components/pull/55) | chore: fixing yaml template linting issues | @nsingla | 2026-01-02 |

### Automated dependency bumps reviewed (Dependabot) (38)

| PR | Title | Author | Merged |
|----|-------|--------|--------|
| [#219](https://github.com/kubeflow/pipelines-components/pull/219) | chore(deps): Bump oauthlib from 4.0.0 to 4.0.1 | @dependabot[bot] | 2026-11-06 |
| [#217](https://github.com/kubeflow/pipelines-components/pull/217) | chore(deps): Bump pyasn1 from 0.6.3 to 0.6.5 | @dependabot[bot] | 2026-11-04 |
| [#215](https://github.com/kubeflow/pipelines-components/pull/215) | chore(deps): Bump filelock from 3.25.2 to 4.2.1 | @dependabot[bot] | 2026-11-03 |
| [#214](https://github.com/kubeflow/pipelines-components/pull/214) | chore(deps): Bump certifi from 2026.2.25 to 2026.10.19 | @dependabot[bot] | 2026-10-23 |
| [#207](https://github.com/kubeflow/pipelines-components/pull/207) | chore(deps): Bump oauthlib from 3.3.1 to 4.0.0 | @dependabot[bot] | 2026-10-02 |
| [#204](https://github.com/kubeflow/pipelines-components/pull/204) | chore(deps): Bump urllib3 from 2.6.3 to 2.8.0 | @dependabot[bot] | 2026-10-02 |
| [#203](https://github.com/kubeflow/pipelines-components/pull/203) | chore(deps): Bump pyjwt from 2.12.1 to 2.15.0 | @dependabot[bot] | 2026-10-02 |
| [#205](https://github.com/kubeflow/pipelines-components/pull/205) | chore(deps): Bump litellm from 1.82.5 to 1.88.6 | @dependabot[bot] | 2026-10-02 |
| [#197](https://github.com/kubeflow/pipelines-components/pull/197) | chore(deps): Bump anyio from 4.12.1 to 4.14.2 | @dependabot[bot] | 2026-09-30 |
| [#194](https://github.com/kubeflow/pipelines-components/pull/194) | chore(deps): Bump pip from 26.0.1 to 26.2 | @dependabot[bot] | 2026-09-01 |
| [#192](https://github.com/kubeflow/pipelines-components/pull/192) | chore(deps): Bump cryptography from 46.0.5 to 50.0.0 | @dependabot[bot] | 2026-08-05 |
| [#191](https://github.com/kubeflow/pipelines-components/pull/191) | chore(deps): Bump aiohttp from 3.13.3 to 3.14.3 | @dependabot[bot] | 2026-08-05 |
| [#160](https://github.com/kubeflow/pipelines-components/pull/160) | chore(deps): Bump docker/metadata-action from 6.0.0 to 6.1.0 | @dependabot[bot] | 2026-05-27 |
| [#158](https://github.com/kubeflow/pipelines-components/pull/158) | chore(deps): Bump docker/login-action from 3.7.0 to 4.2.0 | @dependabot[bot] | 2026-05-26 |
| [#157](https://github.com/kubeflow/pipelines-components/pull/157) | chore(deps): Bump docker/setup-buildx-action from 4.0.0 to 4.1.0 | @dependabot[bot] | 2026-05-26 |
| [#156](https://github.com/kubeflow/pipelines-components/pull/156) | chore(deps): Bump docker/build-push-action from 7.1.0 to 7.2.0 | @dependabot[bot] | 2026-05-21 |
| [#136](https://github.com/kubeflow/pipelines-components/pull/136) | chore(deps): Bump actions/github-script from 8 to 9 | @dependabot[bot] | 2026-04-15 |
| [#120](https://github.com/kubeflow/pipelines-components/pull/120) | chore(deps): Bump actions/upload-artifact from 4 to 7 | @dependabot[bot] | 2026-03-17 |
| [#113](https://github.com/kubeflow/pipelines-components/pull/113) | chore(deps): Bump docker/build-push-action from 6 to 7 | @dependabot[bot] | 2026-03-06 |
| [#112](https://github.com/kubeflow/pipelines-components/pull/112) | chore(deps): Bump docker/metadata-action from 5 to 6 | @dependabot[bot] | 2026-03-06 |
| [#108](https://github.com/kubeflow/pipelines-components/pull/108) | chore(deps): Bump docker/setup-qemu-action from 3 to 4 | @dependabot[bot] | 2026-03-05 |
| [#109](https://github.com/kubeflow/pipelines-components/pull/109) | chore(deps): Bump docker/setup-buildx-action from 3 to 4 | @dependabot[bot] | 2026-03-05 |
| [#105](https://github.com/kubeflow/pipelines-components/pull/105) | chore(deps): Bump actions/download-artifact from 7 to 8 | @dependabot[bot] | 2026-02-27 |
| [#104](https://github.com/kubeflow/pipelines-components/pull/104) | chore(deps): Bump actions/upload-artifact from 6 to 7 | @dependabot[bot] | 2026-02-27 |
| [#101](https://github.com/kubeflow/pipelines-components/pull/101) | chore(deps): Bump ruff from 0.15.1 to 0.15.2 | @dependabot[bot] | 2026-02-23 |
| [#98](https://github.com/kubeflow/pipelines-components/pull/98) | chore(deps): Bump ruff from 0.14.12 to 0.15.1 | @dependabot[bot] | 2026-02-13 |
| [#93](https://github.com/kubeflow/pipelines-components/pull/93) | chore(deps): Bump pip from 26.0 to 26.0.1 | @dependabot[bot] | 2026-02-13 |
| [#77](https://github.com/kubeflow/pipelines-components/pull/77) | chore(deps): Bump pyasn1 from 0.6.1 to 0.6.2 | @dependabot[bot] | 2026-02-13 |
| [#79](https://github.com/kubeflow/pipelines-components/pull/79) | chore(deps): Bump urllib3 from 2.6.2 to 2.6.3 | @dependabot[bot] | 2026-02-13 |
| [#89](https://github.com/kubeflow/pipelines-components/pull/89) | chore(deps): Bump pip from 25.3 to 26.0 | @dependabot[bot] | 2026-02-04 |
| [#85](https://github.com/kubeflow/pipelines-components/pull/85) | chore(deps): Bump packaging from 25.0 to 26.0 | @dependabot[bot] | 2026-02-04 |
| [#90](https://github.com/kubeflow/pipelines-components/pull/90) | chore(deps): Bump protobuf from 6.33.2 to 6.33.5 | @dependabot[bot] | 2026-02-04 |
| [#81](https://github.com/kubeflow/pipelines-components/pull/81) | chore(deps): Bump actions/checkout from 4 to 6 | @dependabot[bot] | 2026-01-23 |
| [#84](https://github.com/kubeflow/pipelines-components/pull/84) | chore(deps): Bump scikit-learn from 1.4.0 to 1.5.0 in /docs/examples | @dependabot[bot] | 2026-01-23 |
| [#69](https://github.com/kubeflow/pipelines-components/pull/69) | chore(deps): Bump yamllint from 1.35.1 to 1.38.0 | @dependabot[bot] | 2026-01-13 |
| [#66](https://github.com/kubeflow/pipelines-components/pull/66) | chore(deps): Bump ruff from 0.8.4 to 0.14.11 | @dependabot[bot] | 2026-01-13 |
| [#68](https://github.com/kubeflow/pipelines-components/pull/68) | chore(deps): Bump actions/checkout from 4 to 6 | @dependabot[bot] | 2026-01-13 |
| [#58](https://github.com/kubeflow/pipelines-components/pull/58) | chore(deps): Bump actions/checkout from 4 to 6 | @dependabot[bot] | 2026-01-06 |

## Governance — OWNERS Roles

### kubeflow/pipelines

| Path | Approver | Reviewer |
|------|----------|----------|
| .github/ | Yes | — |
| backend/ | Yes | Yes |
| docs/ | Yes | — |
| kubernetes_platform/ | Yes | Yes |
| manifests/ | — | Yes |
| sdk/python/kfp/kubernetes/ | Yes | Yes |
| test/ | Yes | — |
| test_data/ | Yes | — |
| tools/ | — | Yes |

### kubeflow/pipelines-components

| Path | Approver | Reviewer |
|------|----------|----------|
| .github/ | Yes | Yes |
| OWNERS (root) | Yes | — |
| docs/ | Yes | Yes |
| scripts/ | Yes | Yes |
| test_data/ | Yes | Yes |
| test_data/components/grouped/ml_models/linear_model/ | Yes | — |
| test_data/pipelines/grouped/etl_flows/daily_ingest/ | Yes | — |

### kubeflow/website

| Path | Approver | Reviewer |
|------|----------|----------|
| content/en/docs/components/pipelines/ | Yes | — |

## Contribution Highlights

### Security
- Path traversal mitigation in `DownloadBlob` ([#12928](https://github.com/kubeflow/pipelines/pull/12928)).
- Rejected `runAsUser=0` at the API level instead of deferring to kubelet ([#13885](https://github.com/kubeflow/pipelines/pull/13885)).
- Service account authorization for runs and recurring runs ([#14181](https://github.com/kubeflow/pipelines/pull/14181)).
- Reviewed and helped land the cross-namespace artifact access fix ([#12860](https://github.com/kubeflow/pipelines/pull/12860)).
- Go toolchain kept current through security releases (1.25.7 review, 1.26.2 bump).

### Architecture and Design
- Authored the KEP for Dynamic Resource Allocation (DRA) support ([#14037](https://github.com/kubeflow/pipelines/pull/14037)) and implemented it end-to-end ([#14243](https://github.com/kubeflow/pipelines/pull/14243), ~4,000 lines added) — the largest feature of the period.
- Added plugin input/output fields to Run and RecurringRun protobufs, enabling runtime extensions ([#12919](https://github.com/kubeflow/pipelines/pull/12919)).
- Migrated S3 bucket management from the MinIO client to AWS SDK v2 ([#12512](https://github.com/kubeflow/pipelines/pull/12512), [#12665](https://github.com/kubeflow/pipelines/pull/12665)) and fixed the resulting checksum validation breakage with non-AWS object stores.
- Centralized V1 pipeline blocking into `IsV1PipelinesBlocked` ([#13722](https://github.com/kubeflow/pipelines/pull/13722)).

### CI/CD Ownership
- Built pipelines-components CI essentially from scratch: build/validate/test workflows for custom base images ([#8](https://github.com/kubeflow/pipelines-components/pull/8)), label management and approval workflows ([#115](https://github.com/kubeflow/pipelines-components/pull/115)), Dependabot trust ([#122](https://github.com/kubeflow/pipelines-components/pull/122)), release-branch support ([#67](https://github.com/kubeflow/pipelines-components/pull/67)).
- In kubeflow/pipelines: hardened the ci-passed label gate, removed GitHub API rate-limit dependencies, stabilized image-build workflows, SeaweedFS S3 auth in CI, and embedded Argo logs into HTML test reports.
- Regenerated API files for grpc-gateway v2.28.0 and made the API generator build from source to prevent stale files.

### Test Reliability
- Fixed Kubernetes-store version bugs (same-named versions, `GetPipelineVersionByName`), MLflow E2E flakiness (polling instead of single-shot checks), informer cache sync races, and broke the `isV2Spec` infinite loop on malformed YAML.

### Community and Mentoring
- 86 code reviews from other contributors, including first-time and external contributors, plus 40 automated dependency bumps reviewed (Dependabot) (shivv23, Sharkyii, Daniel-1600, Ehtasham-Yasin, rautadadya2606 and others).
- 19 issues filed covering backend bugs, flaky tests, CI outages, and feature KEPs.
- OWNERS governance: approver across 15 paths spanning kubeflow/pipelines, kubeflow/pipelines-components, and kubeflow/website; pruned inactive reviewers/approvers ([#13389](https://github.com/kubeflow/pipelines/pull/13389), [#161](https://github.com/kubeflow/pipelines-components/pull/161)).
