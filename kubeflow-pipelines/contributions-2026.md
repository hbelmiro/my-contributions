# Kubeflow Pipelines Contribution Report — Helber Belmiro (@hbelmiro)

**Period:** January 2026 – August 2026

## Summary

| Area                                             | Count            |
|--------------------------------------------------|------------------|
| PRs merged in kubeflow/pipelines                 | 35               |
| PRs reviewed in kubeflow/pipelines (others' PRs) | 65               |
| Issues filed in kubeflow/pipelines               | 17               |
| PRs merged in kubeflow/pipelines-components      | 20               |
| Lines changed in kubeflow/pipelines              | +13,187 / -8,124 |
| Open PRs in kubeflow/pipelines                   | 4                |

---

## kubeflow/pipelines — Merged PRs by Area

### Backend — Bug Fixes and Features

| PR                                                         | Title                                                                        | Merged     |
|------------------------------------------------------------|------------------------------------------------------------------------------|------------|
| [#13931](https://github.com/kubeflow/pipelines/pull/13931) | fix(backend): break infinite loop in isV2Spec on malformed YAML              | 2026-08-05 |
| [#13740](https://github.com/kubeflow/pipelines/pull/13740) | fix: Key processedPipelines by pipeline UUID instead of version name         | 2026-07-16 |
| [#13722](https://github.com/kubeflow/pipelines/pull/13722) | refactor(backend): centralize V1 pipeline blocking into IsV1PipelinesBlocked | 2026-07-27 |
| [#13552](https://github.com/kubeflow/pipelines/pull/13552) | fix: allow same-named pipeline versions under different pipelines            | 2026-06-26 |
| [#13315](https://github.com/kubeflow/pipelines/pull/13315) | fix(backend): fixes AWS SDK v2 checksum validation                           | 2026-04-24 |
| [#13158](https://github.com/kubeflow/pipelines/pull/13158) | fix(backend): Wire `MANAGED_PIPELINES_UPLOAD_TAGS` into `LoadSamples`        | 2026-04-01 |
| [#13124](https://github.com/kubeflow/pipelines/pull/13124) | feat(backend): Improve pod name resolution for pipelines with long names     | 2026-03-25 |
| [#12928](https://github.com/kubeflow/pipelines/pull/12928) | fix(backend): Added path traversal mitigation to DownloadBlob                | 2026-03-03 |
| [#12665](https://github.com/kubeflow/pipelines/pull/12665) | fix(backend): Refactor S3 bucket management — replace MinIO with AWS SDK v2  | 2026-01-19 |
| [#12512](https://github.com/kubeflow/pipelines/pull/12512) | fix(backend): Refactor S3 bucket management (initial)                        | 2026-01-16 |

### Backend — API and Protobuf

| PR                                                         | Title                                                                           | Merged     |
|------------------------------------------------------------|---------------------------------------------------------------------------------|------------|
| [#12919](https://github.com/kubeflow/pipelines/pull/12919) | feat(backend): Add plugin input/output fields to RecurringRun and Run protobufs | 2026-03-09 |
| [#13563](https://github.com/kubeflow/pipelines/pull/13563) | fix(ci): regenerate API files for grpc-gateway v2.28.0 and harden CI workflows  | 2026-06-19 |
| [#13771](https://github.com/kubeflow/pipelines/pull/13771) | ci: build API generator from source in CI to prevent stale files                | 2026-07-27 |

### CI/CD and Infrastructure

| PR                                                         | Title                                                                           | Merged     |
|------------------------------------------------------------|---------------------------------------------------------------------------------|------------|
| [#13685](https://github.com/kubeflow/pipelines/pull/13685) | fix(ci): make image rebuild step actually run after build failure               | 2026-07-08 |
| [#13629](https://github.com/kubeflow/pipelines/pull/13629) | fix(ci): prevent ci-passed label when workflows await approval                  | 2026-07-02 |
| [#13431](https://github.com/kubeflow/pipelines/pull/13431) | chore: refactor Go setup into reusable composite action                         | 2026-05-26 |
| [#13421](https://github.com/kubeflow/pipelines/pull/13421) | chore: bump Go version to 1.26.2                                                | 2026-05-20 |
| [#12810](https://github.com/kubeflow/pipelines/pull/12810) | chore(ci): Reverted changes in the CI check workflow from PR #12793             | 2026-02-16 |
| [#12773](https://github.com/kubeflow/pipelines/pull/12773) | chore(ci): Update image-build workflow to use `github.run_id` for artifact path | 2026-02-06 |
| [#12772](https://github.com/kubeflow/pipelines/pull/12772) | chore(ci): Refine SeaweedFS S3 auth setup and enhance wait logic                | 2026-02-10 |
| [#12769](https://github.com/kubeflow/pipelines/pull/12769) | chore(ci): Simplify image-build workflow by removing caching logic              | 2026-02-05 |
| [#12712](https://github.com/kubeflow/pipelines/pull/12712) | chore(ci): Replace GitHub REST API calls with event payload and cache lookups   | 2026-01-27 |
| [#12698](https://github.com/kubeflow/pipelines/pull/12698) | chore(ci): use author_association to avoid API rate limits in approve workflow  | 2026-01-27 |
| [#12658](https://github.com/kubeflow/pipelines/pull/12658) | chore(tests): Optimize workflows with caching and action upgrades               | 2026-01-21 |
| [#12540](https://github.com/kubeflow/pipelines/pull/12540) | chore(CI): Embed Argo Workflow logs into HTML test reports                      | 2026-01-12 |
| [#13295](https://github.com/kubeflow/pipelines/pull/13295) | fix(ci): Add `proxy` parameter to e2e-test workflow                             | 2026-04-21 |
| [#13247](https://github.com/kubeflow/pipelines/pull/13247) | fix(ci): Update Profile Controller manifest URL in deploy script                | 2026-04-10 |

### Test Reliability

| PR                                                         | Title                                                                         | Merged     |
|------------------------------------------------------------|-------------------------------------------------------------------------------|------------|
| [#13593](https://github.com/kubeflow/pipelines/pull/13593) | fix(test): replace single-shot MLflow status checks with polling              | 2026-06-25 |
| [#13312](https://github.com/kubeflow/pipelines/pull/13312) | fix(test): simplify and stabilize pipeline test cleanup                       | 2026-04-30 |
| [#13253](https://github.com/kubeflow/pipelines/pull/13253) | fix(test): Add `Eventually` for informer cache sync in pipeline version tests | 2026-04-10 |

### Maintenance and Governance

| PR                                                         | Title                                                                          | Merged     |
|------------------------------------------------------------|--------------------------------------------------------------------------------|------------|
| [#13470](https://github.com/kubeflow/pipelines/pull/13470) | chore: Removed non-needed package installation steps from backend Dockerfiles  | 2026-06-08 |
| [#13389](https://github.com/kubeflow/pipelines/pull/13389) | chore: update OWNERS files to remove inactive reviewers and approvers          | 2026-05-12 |
| [#12979](https://github.com/kubeflow/pipelines/pull/12979) | Revert "chore: migrate build system from pip/setup.py to uv workspace"         | 2026-03-06 |
| [#12809](https://github.com/kubeflow/pipelines/pull/12809) | chore(test): Align test/ and test_data/ OWNERS with .github/OWNERS             | 2026-02-16 |
| [#12741](https://github.com/kubeflow/pipelines/pull/12741) | chore(sdk): Add deprecation notice to `add_node_selector_constraint` docstring | 2026-01-30 |

---

## kubeflow/pipelines — Issues Filed (17)

| Issue                                                        | Title                                                                                           | Status |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------|--------|
| [#13926](https://github.com/kubeflow/pipelines/issues/13926) | Malformed YAML upload causes infinite loop in isV2Spec and permanent goroutine leak             | Closed |
| [#13592](https://github.com/kubeflow/pipelines/issues/13592) | Flaky MLflow E2E tests: single-shot status checks race with async MLflow updates                | Closed |
| [#13566](https://github.com/kubeflow/pipelines/issues/13566) | Add concurrency groups to PR-triggered workflows to cancel stale runs                           | Closed |
| [#13565](https://github.com/kubeflow/pipelines/issues/13565) | Add timeout-minutes to image-builds and e2e-test-frontend workflows                             | Closed |
| [#13564](https://github.com/kubeflow/pipelines/issues/13564) | MLflow E2E tests failing: deploy action pinned to stale commit                                  | Closed |
| [#13561](https://github.com/kubeflow/pipelines/issues/13561) | validate-generated-files CI broken on master since grpc-gateway v2.28.0 bump                    | Closed |
| [#13556](https://github.com/kubeflow/pipelines/issues/13556) | LoadSamples skips pipeline version creation when pipeline exists with empty namespace           | Closed |
| [#13535](https://github.com/kubeflow/pipelines/issues/13535) | GetPipelineVersionByName returns wrong version when multiple pipelines have same-named versions | Closed |
| [#13534](https://github.com/kubeflow/pipelines/issues/13534) | Kubernetes store cannot create same-named pipeline versions under different pipelines           | Closed |
| [#13314](https://github.com/kubeflow/pipelines/issues/13314) | S3 operations fail with non-AWS object stores after AWS SDK v2 checksum defaults change         | Closed |
| [#13294](https://github.com/kubeflow/pipelines/issues/13294) | HTTP proxy must match between deploy and E2E Ginkgo (`-useProxy`)                               | Closed |
| [#13252](https://github.com/kubeflow/pipelines/issues/13252) | Flaky pipeline version sorting tests due to K8s store informer cache lag                        | Closed |
| [#12949](https://github.com/kubeflow/pipelines/issues/12949) | Consolidate v2 placeholder resolution into shared utility                                       | Open   |
| [#12913](https://github.com/kubeflow/pipelines/issues/12913) | Flaky test: TestCacheSingleRunWithPVC_SameName_Caches times out on Kind clusters                | Closed |
| [#12771](https://github.com/kubeflow/pipelines/issues/12771) | SeaweedFS S3 Authentication Race Condition in CI                                                | Closed |
| [#12725](https://github.com/kubeflow/pipelines/issues/12725) | Refactor Driver and Launcher: Make All Parameters Required                                      | Open   |
| [#12686](https://github.com/kubeflow/pipelines/issues/12686) | Migrate Python dependency management to uv workspaces                                           | Open   |

---

## kubeflow/pipelines — Code Reviews (65 PRs from other contributors)

Reviews span backend, CI, frontend, SDK, testing, and governance areas. Notable reviews include:

| PR                                                         | Title                                                                      | Author           |
|------------------------------------------------------------|----------------------------------------------------------------------------|------------------|
| [#13935](https://github.com/kubeflow/pipelines/pull/13935) | fix(backend): close SQL rows on all early return paths in storage layer    | shivv23          |
| [#13930](https://github.com/kubeflow/pipelines/pull/13930) | test(e2e): add Kind GPU scheduling check with Fake GPU Operator            | sduvvuri1603     |
| [#13918](https://github.com/kubeflow/pipelines/pull/13918) | fix(backend): propagate error when scanRowsToRuns fails                    | Sharkyii         |
| [#13913](https://github.com/kubeflow/pipelines/pull/13913) | fix(backend): propagate ctx instead of using context.TODO/Background       | shivv23          |
| [#13839](https://github.com/kubeflow/pipelines/pull/13839) | fix(backend): return permanent error when token refresh fails              | Sharkyii         |
| [#13838](https://github.com/kubeflow/pipelines/pull/13838) | fix(backend): log the actual bucket close error                            | Sharkyii         |
| [#13799](https://github.com/kubeflow/pipelines/pull/13799) | chore: apply gofmt formatting corrections                                  | kaikaila         |
| [#13773](https://github.com/kubeflow/pipelines/pull/13773) | fix(backend): Make kind-cluster-agnostic timeouts configurable             | Daniel-1600      |
| [#13735](https://github.com/kubeflow/pipelines/pull/13735) | CI: Add execute permissions to .github/scripts/ai_triage.sh                | mprahl           |
| [#13697](https://github.com/kubeflow/pipelines/pull/13697) | ci: authenticate googleapis proto fetches to avoid 429 rate limits         | jeffspahr        |
| [#13695](https://github.com/kubeflow/pipelines/pull/13695) | test: authenticate and retry raw.githubusercontent.com URL verification    | jeffspahr        |
| [#13693](https://github.com/kubeflow/pipelines/pull/13693) | ci: give legacy v2 integration tests an intentional time budget            | jeffspahr        |
| [#13656](https://github.com/kubeflow/pipelines/pull/13656) | fix(backend): fall back to direct module fetch on Go proxy errors          | jeffspahr        |
| [#13655](https://github.com/kubeflow/pipelines/pull/13655) | ci: stop fail-fast from cancelling image builds and their retries          | jeffspahr        |
| [#13609](https://github.com/kubeflow/pipelines/pull/13609) | feat: add TLS MinVersion and cipher suite CLI flags to apiserver           | ugiordan         |
| [#13577](https://github.com/kubeflow/pipelines/pull/13577) | fix(backend): stream bounded object store reads                            | jeffspahr        |
| [#13464](https://github.com/kubeflow/pipelines/pull/13464) | chore(deps): bump remaining backend Go builder images to golang:1.26.3     | tolgatuncoglu    |
| [#13437](https://github.com/kubeflow/pipelines/pull/13437) | fix(backend): resolve artifact OneOf outputs at runtime                    | mprahl           |
| [#13359](https://github.com/kubeflow/pipelines/pull/13359) | Add alyssacgoins as a backend approver                                     | alyssacgoins     |
| [#13352](https://github.com/kubeflow/pipelines/pull/13352) | chore: adding myself as backend approver                                   | nsingla          |
| [#13345](https://github.com/kubeflow/pipelines/pull/13345) | fix(backend): prevent premature workflow GC due to DB write race condition | shreeharshshinde |
| [#13325](https://github.com/kubeflow/pipelines/pull/13325) | fix(backend): apply recurring run service account unconditionally          | neo99zhang       |
| [#13307](https://github.com/kubeflow/pipelines/pull/13307) | chore(backend): Fix MLflow tags, nested run status update                  | VaniHaripriya    |
| [#13298](https://github.com/kubeflow/pipelines/pull/13298) | chore(backend): Add RetryRun support to RunClient                          | VaniHaripriya    |
| [#13227](https://github.com/kubeflow/pipelines/pull/13227) | ci: preload Kind images instead of pushing via local registry              | jeffspahr        |
| [#13223](https://github.com/kubeflow/pipelines/pull/13223) | chore(ci): increase the number of parallel threads for e2e tests           | nsingla          |
| [#13203](https://github.com/kubeflow/pipelines/pull/13203) | test(backend): increase apiserver/template test coverage to 64.5%          | jsonmp-k8        |
| [#13201](https://github.com/kubeflow/pipelines/pull/13201) | test(backend): increase apiserver/client test coverage to 62.3%            | jsonmp-k8        |
| [#13137](https://github.com/kubeflow/pipelines/pull/13137) | fix(backend): validate pipeline names in K8s store before API call         | Priyanshu-u07    |
| [#13046](https://github.com/kubeflow/pipelines/pull/13046) | ci: workflow fixes                                                         | nsingla          |
| [#13009](https://github.com/kubeflow/pipelines/pull/13009) | feat(frontend,backend): show actual retry start time for pipeline runs     | Sridhar1030      |
| [#12999](https://github.com/kubeflow/pipelines/pull/12999) | feat(backend): Add option to apply tags to create, upload pipelines        | nsingla          |
| [#12971](https://github.com/kubeflow/pipelines/pull/12971) | fix(test): re-enable and add all snapshot tests for kfp-kubernetes         | jsonmp-k8        |
| [#12970](https://github.com/kubeflow/pipelines/pull/12970) | feat(manifests): add init containers for startup ordering                  | jsonmp-k8        |
| [#12916](https://github.com/kubeflow/pipelines/pull/12916) | chore(backend): Increase timeout for PVC cache test to reduce flakiness    | aniketpati1121   |
| [#12911](https://github.com/kubeflow/pipelines/pull/12911) | chore(test): add jeffspahr to test OWNERS approvers                        | jeffspahr        |
| [#12905](https://github.com/kubeflow/pipelines/pull/12905) | chore: upgrading go to 1.25.7 as it has many security fixes                | nsingla          |
| [#12862](https://github.com/kubeflow/pipelines/pull/12862) | doc: Add a KEP for native MLflow integration in KFP                        | mprahl           |
| [#12860](https://github.com/kubeflow/pipelines/pull/12860) | fix(frontend): Prevent Unauthorized Cross-Namespace Artifact Access        | Raakshass        |
| [#12836](https://github.com/kubeflow/pipelines/pull/12836) | chore: Use make commands in documentation                                  | matheusandre1    |
| [#12833](https://github.com/kubeflow/pipelines/pull/12833) | fix: correct typo pipline_func_args -> pipeline_func_args                  | sduvvuri1603     |
| [#12823](https://github.com/kubeflow/pipelines/pull/12823) | chore(ci): upgrade GitHub Actions to latest major versions                 | jsonmp-k8        |
| [#12793](https://github.com/kubeflow/pipelines/pull/12793) | chore(frontend): upgrade material-ui to v4                                 | jeffspahr        |
| [#12792](https://github.com/kubeflow/pipelines/pull/12792) | Fix SeaweedFS IAM endpoint in profile controller                           | sduvvuri1603     |
| [#12781](https://github.com/kubeflow/pipelines/pull/12781) | docs: replace broken project argo link                                     | aniketpati1121   |
| [#12776](https://github.com/kubeflow/pipelines/pull/12776) | fix(cli): remove unused namespace in `run.py`                              | puwun            |
| [#12770](https://github.com/kubeflow/pipelines/pull/12770) | chore: migrate build system from pip/setup.py to uv workspaces             | sh4shv4t         |
| [#12768](https://github.com/kubeflow/pipelines/pull/12768) | feat(ci): optimize copilot reviews                                         | droctothorpe     |
| [#12766](https://github.com/kubeflow/pipelines/pull/12766) | test: fix ray pipeline and lower casing pipeline names in upgrade tests    | nsingla          |
| [#12764](https://github.com/kubeflow/pipelines/pull/12764) | ci: add pr number to the cache key                                         | nsingla          |
| [#12755](https://github.com/kubeflow/pipelines/pull/12755) | chore(test): use make commands in `sdk-component-yaml`                     | puwun            |
| [#12753](https://github.com/kubeflow/pipelines/pull/12753) | docs: fix broken Kubeflow Pipelines installation link                      | aniketpati1121   |
| [#12735](https://github.com/kubeflow/pipelines/pull/12735) | fix(testing) retention for image-builds-with-cache artifacts               | alyssacgoins     |
| [#12710](https://github.com/kubeflow/pipelines/pull/12710) | ci: adding myself as reviewer and approver for github workflows & actions  | nsingla          |
| [#12696](https://github.com/kubeflow/pipelines/pull/12696) | feat(kubernetes_platform): add data_source parameter to CreatePVC          | khushiiagrawal   |
| [#12694](https://github.com/kubeflow/pipelines/pull/12694) | Fix: pip upgrade in backend API Dockerfile                                 | sduvvuri1603     |
| [#12657](https://github.com/kubeflow/pipelines/pull/12657) | fix(ci): port-forward minio-service instead of pod                         | kaikaila         |
| [#12631](https://github.com/kubeflow/pipelines/pull/12631) | chore: remove disabled renovate.json5 config                               | jeffspahr        |
| [#12629](https://github.com/kubeflow/pipelines/pull/12629) | chore(deps): bump werkzeug from 3.1.3 to 3.1.5                             | dependabot       |
| [#12613](https://github.com/kubeflow/pipelines/pull/12613) | chore: Remove minio                                                        | akagami-harsh    |
| [#12607](https://github.com/kubeflow/pipelines/pull/12607) | feat(backend): add Literal parameter validation                            | khushiiagrawal   |
| [#12598](https://github.com/kubeflow/pipelines/pull/12598) | fix(backend): resolve IfPresent conditions in component.yaml               | khushiiagrawal   |
| [#12572](https://github.com/kubeflow/pipelines/pull/12572) | Update CA Cert Conditional                                                 | alyssacgoins     |
| [#12491](https://github.com/kubeflow/pipelines/pull/12491) | documentation: Update installation options                                 | gorkem           |
| [#12417](https://github.com/kubeflow/pipelines/pull/12417) | feat: Support driver pod labels and annotations configuration              | thc1006          |

---

## kubeflow/pipelines — Open PRs (in progress)

| PR                                                         | Title                                                                                   | Created    |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------|------------|
| [#13932](https://github.com/kubeflow/pipelines/pull/13932) | docs(AGENTS.md): add comment and documentation policy                                   | 2026-07-29 |
| [#13885](https://github.com/kubeflow/pipelines/pull/13885) | fix(backend): reject runAsUser=0 at API level instead of deferring to kubelet           | 2026-07-27 |
| [#13143](https://github.com/kubeflow/pipelines/pull/13143) | fix(backend, frontend): Infer FAILED state for pods stuck in CreateContainerConfigError | 2026-03-26 |
| [#12515](https://github.com/kubeflow/pipelines/pull/12515) | Add KEP-12513: Introduce PVC-based artifact storage for Kubeflow Pipelines              | 2025-12-03 |

---

## kubeflow/pipelines-components — Merged PRs (20)

| PR                                                                | Title                                                                           | Merged     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------|------------|
| [#193](https://github.com/kubeflow/pipelines-components/pull/193) | Add hbelmiro to approvers list in OWNERS file                                   | 2026-08-05 |
| [#186](https://github.com/kubeflow/pipelines-components/pull/186) | fix(scripts): move tests into tests/ for CI discovery                           | 2026-07-23 |
| [#182](https://github.com/kubeflow/pipelines-components/pull/182) | fix(ci): regenerate stale golden READMEs and trigger tests on test_data changes | 2026-07-15 |
| [#178](https://github.com/kubeflow/pipelines-components/pull/178) | chore: Updated stale readme                                                     | 2026-07-02 |
| [#163](https://github.com/kubeflow/pipelines-components/pull/163) | ci: Remove `OWNERS` file exclusion from readme-check.yml                        | 2026-05-28 |
| [#161](https://github.com/kubeflow/pipelines-components/pull/161) | chore: Update OWNERS files with current team roster                             | 2026-05-27 |
| [#159](https://github.com/kubeflow/pipelines-components/pull/159) | ci: Ignore `OWNERS` file changes in workflow triggers                           | 2026-05-26 |
| [#140](https://github.com/kubeflow/pipelines-components/pull/140) | ci: Refactor environment variable usage in workflows                            | 2026-04-14 |
| [#139](https://github.com/kubeflow/pipelines-components/pull/139) | ci: Update actions to pinned versions in workflows                              | 2026-04-14 |
| [#122](https://github.com/kubeflow/pipelines-components/pull/122) | ci: Trust Dependabot for CI checks and improve bot handling                     | 2026-03-17 |
| [#115](https://github.com/kubeflow/pipelines-components/pull/115) | ci: Add workflows for CI label management and approvals                         | 2026-03-13 |
| [#70](https://github.com/kubeflow/pipelines-components/pull/70)   | chore: Move `pyyaml` from core dependencies to optional test dependencies       | 2026-01-14 |
| [#67](https://github.com/kubeflow/pipelines-components/pull/67)   | chore: Added release branch support to CI workflows                             | 2026-02-03 |
| [#65](https://github.com/kubeflow/pipelines-components/pull/65)   | Allow top-level kfp_components imports and clarify Import Guard guidance        | 2026-01-09 |
| [#59](https://github.com/kubeflow/pipelines-components/pull/59)   | chore: Unpinned test dependencies, add uv.lock sync check in pre-commit and CI  | 2026-01-06 |
| [#57](https://github.com/kubeflow/pipelines-components/pull/57)   | refactor: Consolidate reusable utility functions into `scripts/lib`             | 2026-01-07 |
| [#53](https://github.com/kubeflow/pipelines-components/pull/53)   | chore: replace 'uv run python' with 'uv run' across repo                        | 2026-01-02 |
| [#51](https://github.com/kubeflow/pipelines-components/pull/51)   | docs: Added AI agent guidance                                                   | 2026-02-02 |
| [#50](https://github.com/kubeflow/pipelines-components/pull/50)   | test: Standardize test imports to use relative imports                          | 2026-01-02 |
| [#8](https://github.com/kubeflow/pipelines-components/pull/8)     | Added CI workflows for building, validating, and testing custom base images     | 2026-01-23 |

---

## Governance — OWNERS Roles

### kubeflow/pipelines

| Path                   | Approver | Reviewer |
|------------------------|----------|----------|
| `.github/`             | Yes      | —        |
| `backend/`             | Yes      | Yes      |
| `docs/`                | Yes      | —        |
| `kubernetes_platform/` | Yes      | Yes      |
| `manifests/kustomize/` | —        | Yes      |
| `tools/`               | —        | Yes      |

### kubeflow/pipelines-components

| Path         | Approver | Reviewer |
|--------------|----------|----------|
| `/` (root)   | Yes      | —        |
| `.github/`   | Yes      | Yes      |
| `docs/`      | Yes      | Yes      |
| `scripts/`   | Yes      | Yes      |
| `test_data/` | Yes      | Yes      |

### kubeflow/website

| Path                                    | Approver | Reviewer |
|-----------------------------------------|----------|----------|
| `content/en/docs/components/pipelines/` | Yes      | —        |

---

## Contribution Highlights

### Security
- **Path traversal mitigation** in object store blob downloads ([#12928](https://github.com/kubeflow/pipelines/pull/12928))
- **runAsUser=0 rejection** at API level (open — [#13885](https://github.com/kubeflow/pipelines/pull/13885))
- Reviewed cross-namespace artifact access fix ([#12860](https://github.com/kubeflow/pipelines/pull/12860))

### Architecture and Design
- **KEP for PVC-based artifact storage** (open — [#12515](https://github.com/kubeflow/pipelines/pull/12515))
- **Plugin input/output fields** added to RecurringRun and Run protobufs ([#12919](https://github.com/kubeflow/pipelines/pull/12919))
- **MinIO-to-AWS SDK v2 migration** for S3 bucket management ([#12665](https://github.com/kubeflow/pipelines/pull/12665), [#12512](https://github.com/kubeflow/pipelines/pull/12512))
- **Centralized V1 pipeline blocking** refactor ([#13722](https://github.com/kubeflow/pipelines/pull/13722))
- Reviewed MLflow KEP ([#12862](https://github.com/kubeflow/pipelines/pull/12862))

### CI/CD Ownership
- Overhauled CI approval workflows to eliminate API rate limits and race conditions
- Hardened image builds with retry logic and artifact path improvements
- Embedded Argo Workflow logs in HTML test reports for faster debugging
- Built CI infrastructure for kubeflow/pipelines-components from scratch (workflows, label management, approvals)
- Built API generator from source in CI to prevent stale generated files ([#13771](https://github.com/kubeflow/pipelines/pull/13771))

### Community and Mentoring
- Reviewed 65 PRs from 20+ distinct contributors across backend, CI, frontend, SDK, testing, and governance
- Updated OWNERS files across kubeflow/pipelines and kubeflow/pipelines-components
- Filed 17 issues with detailed root cause analysis and reproduction steps
