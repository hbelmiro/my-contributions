# Open Data Hub / Red Hat Data Services Contributions — 2026

Contributions by [hbelmiro](https://github.com/hbelmiro) across the `opendatahub-io` and `red-hat-data-services` (RHDS) GitHub organizations, January 1 – November 24, 2026.

**Deduplication note:** Contributions existing in multiple repos of a fork chain count once. PRs that mirror hbelmiro's own merged PRs in out-of-scope upstream roots (`kubeflow/pipelines`, `kubeflow/pipelines-components`) are excluded entirely (12 such PRs in `opendatahub-io/data-science-pipelines` and 1 in `opendatahub-io/pipelines-components`). RHDS PRs that are pure backports/syncs of PRs already counted in the ODH repo are excluded; RHDS-only work (Konflux Dockerfiles, release-branch engineering, Konflux central) is counted in RHDS.

## Summary

| Repo | PRs merged | PRs reviewed (human) | PRs reviewed (automated) | Issues filed | Lines changed (authored PRs) |
| --- | ---: | ---: | ---: | ---: | --- |
| opendatahub-io/data-science-pipelines-operator | 42 | 32 | 0 | 0 | +11,025 / −800 |
| opendatahub-io/data-science-pipelines | 37 | 34 | 1 | 0 | +31,846 / −5,124 |
| opendatahub-io/pipelines-components | 17 | 14 | 1 | 0 | +49,375 / −13,421 |
| opendatahub-io/argo-workflows | 4 | 3 | 0 | 0 | +236 / −195 |
| opendatahub-io/operator-chaos | 2 | 0 | 0 | 0 | +2,501 / −327 |
| opendatahub-io/mlflow-operator | 2 | 0 | 1 | 0 | +94 / −186 |
| opendatahub-io/model-registry-operator | 1 | 0 | 2 | 0 | +832 / −99 |
| opendatahub-io/opendatahub-tests | 1 | 0 | 0 | 0 | +4 / −1 |
| red-hat-data-services/data-science-pipelines | 16 | 8 | 0 | 0 | +1,385,883 / −254,967 |
| red-hat-data-services/argo-workflows | 5 | 7 | 0 | 0 | +165 / −23 |
| red-hat-data-services/konflux-central | 6 | 3 | 0 | 0 | +14 / −18 |
| red-hat-data-services/data-science-pipelines-operator | 4 | 5 | 0 | 0 | +2,358 / −126 |
| red-hat-data-services/ml-metadata | 3 | 4 | 0 | 0 | +6,573 / −6,555 |
| red-hat-data-services/pipelines-components | 2 | 4 | 0 | 0 | +164 / −402 |
| red-hat-data-services/rhods-devops-infra | 2 | 1 | 0 | 0 | +12 / −3 |
| **Total** | **144** | **117** | **5** | **0** | **+1,491,082 / −282,247** |

No open PRs and no issues filed in the period. The RHDS data-science-pipelines line count is dominated by [#1363](https://github.com/red-hat-data-services/data-science-pipelines/pull/1363), a merge of `upstream/stable` touching ~1.64M vendored lines.

## Merged PRs by area — opendatahub-io/data-science-pipelines-operator (primary repo)

### Backend features — managed pipelines and DRA

| PR | Title | Merged |
| --- | --- | --- |
| [#1144](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1144) | Added new config for default StorageClass for pipeline CreatePVC task volumes | 2026-11-23 |
| [#1128](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1128) | Set Managed Pipelines as enabled by default | 2026-10-08 |
| [#1090](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1090) | feat: add DRA resourceClaims support to all DSPA components | 2026-09-10 |
| [#1070](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1070) | Update managed pipeline `versionName` logic to use platform version | 2026-06-29 |
| [#1069](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1069) | Add versionName field to PipelineVersion CRD | 2026-06-26 |
| [#1011](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1011) | Add `--managedPipelinesDir` arg for managed pipelines support and update tests | 2026-04-08 |
| [#1003](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1003) | Add support for managed-pipelines.json validation and caching in DSP API controller | 2026-04-06 |
| [#1001](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1001) | Include `PlatformVersion` in API Server config hash and add unit test | 2026-03-31 |
| [#995](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/995) | Accept MANAGEDPIPELINES_IMAGES JSON mapping and forward RELATED_IMAGE_* env vars to init container | 2026-04-03 |

### Security and hardening

| PR | Title | Merged |
| --- | --- | --- |
| [#1097](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1097) | Fixing RBAC permissions | 2026-09-09 |
| [#1096](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1096) | chore: Add `ALLOWEDSERVICEACCOUNTS` environment variable to apiserver deployment templates for all test cases | 2026-09-09 |
| [#998](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/998) | Set default non-root user in Dockerfile for enhanced security | 2026-03-25 |

### Bug fixes

| PR | Title | Merged |
| --- | --- | --- |
| [#1099](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1099) | fix: database configuration hardening and build workflow fixes | 2026-09-09 |
| [#1098](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1098) | fix: database configuration hardening and build workflow fixes | 2026-09-09 |
| [#1102](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1102) | chore: fix kustomization to use openshift base for make-deploy | 2026-09-10 |

### CI/CD and test infrastructure

| PR | Title | Merged |
| --- | --- | --- |
| [#1149](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1149) | fix(ci): pin kubeflow/pipelines disk-cleanup action to main | 2026-11-17 |
| [#1148](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1148) | fix(ci): correct Kind webhook TLS and readiness checks | 2026-11-12 |
| [#1147](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1147) | Pin actions/checkout to v3.6.0 in build composite action | 2026-11-09 |
| [#1095](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1095) | fix(ci): always fall through on clone fallback when fork/branch not found | 2026-09-04 |
| [#1093](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1093) | fix(ci): detect fork repos when building DSP and Argo images in KinD tests | 2026-09-03 |
| [#1088](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1088) | chore(ci): build DSP and Argo images from source during KinD integration tests | 2026-09-01 |
| [#1084](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1084) | fix: exclude .tekton/ from yamllint pre-commit check | 2026-08-12 |
| [#1047](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1047) | ci: Add odh- prefix to ODH image tags for DSPO/DSP image alignment | 2026-05-26 |
| [#1016](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1016) | Add workflow to enforce consistency between Go versions in `go.mod` and Dockerfiles | 2026-05-06 |
| [#966](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/966) | Enable CI workflows triggered on push to main and stable branches | 2026-01-16 |
| [#965](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/965) | Enable CI workflows triggered on push to versioned branches (`v*.*.*`) | 2026-01-16 |
| [#962](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/962) | Enable CI workflows triggered on push to `main` and `stable` branches | 2026-01-15 |

### Build and packaging

| PR | Title | Merged |
| --- | --- | --- |
| [#1066](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1066) | Move `GODEBUG=fips140=on` configuration from Dockerfile to `go.mod` | 2026-06-18 |
| [#1062](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1062) | Used native FIPS from Go 1.26.3 | 2026-06-18 |
| [#1053](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1053) | fix: support arm64 builder for Dockerfile and add CI validation | 2026-06-30 |
| [#994](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/994) | Set `--platform=$BUILDPLATFORM` in Dockerfile builder stage | 2026-04-07 |
| [#970](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/970) | Added support for non-FIPS local builds on Apple Silicon | 2026-02-06 |

### Branch maintenance (main → stable merges)

| PR | Title | Merged |
| --- | --- | --- |
| [#1142](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1142) | Merge `main` into `stable` | 2026-11-03 |
| [#1076](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1076) | Merge main into stable | 2026-07-07 |
| [#1067](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1067) | Merge main into stable | 2026-06-22 |
| [#1057](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1057) | Merge from main | 2026-05-29 |
| [#1014](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1014) | Merge main to stable | 2026-04-10 |

### Governance and documentation

| PR | Title | Merged |
| --- | --- | --- |
| [#1150](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1150) | Remove mprahl from OWNERS | 2026-11-17 |
| [#1127](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1127) | Remove VaniHaripriya from OWNERS | 2026-09-30 |
| [#1085](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1085) | Remove nsingla from OWNERS | 2026-08-17 |
| [#1054](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1054) | Update `OWNERS` file: adjust approvers and reviewers, move `gmfrasca` to emeritus_approvers | 2026-05-19 |
| [#1133](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1133) | Document managed pipelines rollback behavior | 2026-10-12 |

## Merged PRs — opendatahub-io/data-science-pipelines

Fork-chain carries, branch maintenance, fork-specific fixes, and OWNERS governance. Excluded (mirrored in `kubeflow/pipelines`, out of scope): #533, #464, #442, #441, #440, #395, #391, #363, #358, #342, #339, #318.

### Upstream carries (fork-only patches)

| PR | Title | Merged |
| --- | --- | --- |
| [#531](https://github.com/opendatahub-io/data-science-pipelines/pull/531) | UPSTREAM: carry: Remove mprahl from OWNERS | 2026-11-17 |
| [#465](https://github.com/opendatahub-io/data-science-pipelines/pull/465) | UPSTREAM: carry: test: pin Ubuntu runners and repair Kind CI setup | 2026-10-29 |
| [#454](https://github.com/opendatahub-io/data-science-pipelines/pull/454) | UPSTREAM: carry: Added upgrade tests for modular architecture | 2026-10-08 |
| [#401](https://github.com/opendatahub-io/data-science-pipelines/pull/401) | UPSTREAM: carry: fix: re-establish port-forwarding after upgrade deploy in upgrade test | 2026-07-08 |
| [#386](https://github.com/opendatahub-io/data-science-pipelines/pull/386) | UPSTREAM carry: chore: remove `GODEBUG=fips140=on` from backend Dockerfiles and move configuration to go.mod | 2026-06-18 |
| [#360](https://github.com/opendatahub-io/data-science-pipelines/pull/360) | UPSTREAM carry: chore: remove FIPS-related build logic from Dockerfiles and Makefile | 2026-06-18 |
| [#355](https://github.com/opendatahub-io/data-science-pipelines/pull/355) | UPSTREAM carry: ci: Update DSP CI for odh- prefixed DSPO image tags and unified registry | 2026-05-26 |
| [#352](https://github.com/opendatahub-io/data-science-pipelines/pull/352) | UPSTREAM carry: Fixed cross-platform image builds | 2026-07-20 |
| [#348](https://github.com/opendatahub-io/data-science-pipelines/pull/348) | UPSTREAM carry: ci: enforce Go version consistency in workflows and Dockerfiles | 2026-05-06 |
| [#337](https://github.com/opendatahub-io/data-science-pipelines/pull/337) | UPSTREAM carry: fix(ci): Update service account name to 'pipeline-runner' in deployment script | 2026-04-24 |
| [#326](https://github.com/opendatahub-io/data-science-pipelines/pull/326) | UPSTREAM carry: fix(ci): Conditionalize operator deployment in workflows | 2026-04-15 |
| [#324](https://github.com/opendatahub-io/data-science-pipelines/pull/324) | UPSTREAM carry: fix(ci): Enable pod-to-pod TLS configuration in upgrade test workflow | 2026-04-14 |
| [#320](https://github.com/opendatahub-io/data-science-pipelines/pull/320) | UPSTREAM carry: fix(ci): Replace unavailable kube-rbac-proxy image registry | 2026-04-13 |
| [#315](https://github.com/opendatahub-io/data-science-pipelines/pull/315) | UPSTREAM carry: feat(backend): Add support for managed pipeline manifests in LoadSamples | 2026-04-10 |
| [#301](https://github.com/opendatahub-io/data-science-pipelines/pull/301) | UPSTREAM carry: chore(config): Rename `ARGO_POD_NAME` to `KFP_POD_NAME` in pod name fetch logic | 2026-03-25 |
| [#267](https://github.com/opendatahub-io/data-science-pipelines/pull/267) | UPSTREAM carry: Add FIPS and architecture build options to Dockerfiles and Makefile for compatibility with Apple Silicon | 2026-02-06 |
| [#266](https://github.com/opendatahub-io/data-science-pipelines/pull/266) | UPSTREAM carry: Update `actions/github-script` to v8.0.0 in commit-check-pr workflow | 2026-01-30 |

### CI/CD, build, and fork-specific fixes

| PR | Title | Merged |
| --- | --- | --- |
| [#523](https://github.com/opendatahub-io/data-science-pipelines/pull/523) | fix(test-images): support non-root UIDs in ds-pipelines-tests image | 2026-11-12 |
| [#522](https://github.com/opendatahub-io/data-science-pipelines/pull/522) | fix(ci): correct deployment namespaces and readiness | 2026-11-12 |
| [#470](https://github.com/opendatahub-io/data-science-pipelines/pull/470) | Pin actions/checkout to v3.6.0 in build composite action | 2026-11-09 |
| [#443](https://github.com/opendatahub-io/data-science-pipelines/pull/443) | ci: build DSPO image from selected source | 2026-09-10 |
| [#433](https://github.com/opendatahub-io/data-science-pipelines/pull/433) | test: temporarily skip MLflow e2e tests | 2026-08-27 |
| [#416](https://github.com/opendatahub-io/data-science-pipelines/pull/416) | Fix cross-architecture wget binary in apiserver Dockerfile | 2026-07-21 |
| [#413](https://github.com/opendatahub-io/data-science-pipelines/pull/413) | Use rhoai-version tag as managed pipeline version name | 2026-07-16 |

### Branch maintenance (master/main → stable merges)

| PR | Title | Merged |
| --- | --- | --- |
| [#466](https://github.com/opendatahub-io/data-science-pipelines/pull/466) | Merge `master` into `stable` | 2026-10-30 |
| [#419](https://github.com/opendatahub-io/data-science-pipelines/pull/419) | Merge master into stable | 2026-07-23 |
| [#415](https://github.com/opendatahub-io/data-science-pipelines/pull/415) | Sync master into stable | 2026-07-17 |
| [#400](https://github.com/opendatahub-io/data-science-pipelines/pull/400) | Main to stable | 2026-07-08 |
| [#389](https://github.com/opendatahub-io/data-science-pipelines/pull/389) | Merge main into stable | 2026-06-19 |
| [#340](https://github.com/opendatahub-io/data-science-pipelines/pull/340) | Merge master into stable | 2026-04-24 |
| [#327](https://github.com/opendatahub-io/data-science-pipelines/pull/327) | Merge master to stable | 2026-04-15 |
| [#325](https://github.com/opendatahub-io/data-science-pipelines/pull/325) | Merge master to stable | 2026-04-14 |
| [#319](https://github.com/opendatahub-io/data-science-pipelines/pull/319) | Merge main to stable | 2026-04-11 |

### Governance — OWNERS

| PR | Title | Merged |
| --- | --- | --- |
| [#455](https://github.com/opendatahub-io/data-science-pipelines/pull/455) | Remove VaniHaripriya from OWNERS | 2026-09-30 |
| [#431](https://github.com/opendatahub-io/data-science-pipelines/pull/431) | Remove nsingla from OWNERS | 2026-08-17 |
| [#414](https://github.com/opendatahub-io/data-science-pipelines/pull/414) | Update OWNERS: adjust reviewer/approver roles and consolidate | 2026-07-21 |
| [#265](https://github.com/opendatahub-io/data-science-pipelines/pull/265) | chore: Add hbelmiro and nsingla to OWNERS file as approvers | 2026-01-30 |

## Issues filed

None in the period.

## Code reviews

### opendatahub-io/data-science-pipelines-operator (32)

| PR | Title | Author |
| --- | --- | --- |
| [#1145](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1145) | feat(tls): project cluster TLS policy into DSP API and webhook operands | ugiordan |
| [#1143](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1143) | fix(tls): validate cluster TLS profiles and honor adherence policy | ugiordan |
| [#1140](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1140) | fix(aipipelines): report Kubeflow Pipelines release in status | mprahl |
| [#1139](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1139) | feat: apply OpenShift TLS profile to kube-rbac-proxy sidecars | sduvvuri1603 |
| [#1138](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1138) | fix(aipipelines): adopt legacy-owned core ServiceMonitor | mprahl |
| [#1101](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1101) | feat(tls): enable secure metrics serving | ugiordan |
| [#1094](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1094) | feat(api): add AIPipelines module API | lugi0 |
| [#1091](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1091) | fix: set SSL_CERT_DIR on workflow pods so the driver trusts the mounted CA | VaniHaripriya |
| [#1083](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1083) | feat(rbac,tls): move config.openshift.io RBAC to overlay and tighten adherence error handling (RHOAIENG-79001, RHOAIENG-78981) | ugiordan |
| [#1079](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1079) | fix: handle IsServerTimeout in TLS profile resolution | ugiordan |
| [#1078](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1078) | fix: simplify TLS adherence policy error handling | ugiordan |
| [#1074](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1074) | fix: TLS profile resilience (transient errors, adherence policy, watcher self-healing) | ugiordan |
| [#1068](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1068) | (chore): address disconnected-readiness-scorer findings | alyssacgoins |
| [#1063](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1063) | feat: integrate with cluster TLS security profile | ugiordan |
| [#1058](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1058) | test: adding chaos integration tests | nsingla |
| [#1056](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1056) | feat: add AutoML and AutoRAG related images to manager | Wojciech-Rebisz |
| [#1048](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1048) | Add mlflow plugin support | VaniHaripriya |
| [#1015](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1015) | fix: surface all ExtractParams errors on APIServerReady status | sduvvuri1603 |
| [#1013](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1013) | Updated to source managed pipeline related images from RELATED_IMAGE_* | VaniHaripriya |
| [#1007](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1007) | chore: updating kfp version to 2.16.0 | nsingla |
| [#1006](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1006) | fix(test): reset global Prometheus gauges before metrics unit tests | sduvvuri1603 |
| [#1005](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1005) | feat: default managed pipelines image from operator config | sduvvuri1603 |
| [#1002](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1002) | Add sduvvuri to OWNERS and reviewers list | sduvvuri1603 |
| [#999](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/999) | Add NetworkPolicy watcher to DSPA controller | sduvvuri1603 |
| [#997](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/997) | adding tags to pipeline and pipeline version CRDs | nsingla |
| [#993](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/993) | feat: Inject init container into API server deployment for pipeline compilation and upload | sduvvuri1603 |
| [#991](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/991) | adding back managed pipeline spec to dspa | nsingla |
| [#990](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/990) | fix(metrics): delete metrics during DSPA finalization | nsingla |
| [#985](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/985) | upgrade to go 1.25.7 to address CVE-2025-61729 | alyssacgoins |
| [#963](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/963) | removing hardcoded secrets | dchourasia |
| [#961](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/961) | removing hardoded secrets | dchourasia |
| [#955](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/955) | chore: Bump Kustomize version in Makefile | gmfrasca |

### opendatahub-io/data-science-pipelines (34 human, 1 automated)

| PR | Title | Author |
| --- | --- | --- |
| [#527](https://github.com/opendatahub-io/data-science-pipelines/pull/527) | test(backend): open pipeline fixtures read-only | dbasunag |
| [#526](https://github.com/opendatahub-io/data-science-pipelines/pull/526) | test(backend): harden upgrade harness detection and lifecycle | dbasunag |
| [#471](https://github.com/opendatahub-io/data-science-pipelines/pull/471) | UPSTREAM: carry: fix product smoke filters and multi-user E2E configure | sduvvuri1603 |
| [#468](https://github.com/opendatahub-io/data-science-pipelines/pull/468) | UPSTREAM: carry: feat: add TLS MinVersion and cipher suite CLI flags to apiserver (#13609) | ugiordan |
| [#467](https://github.com/opendatahub-io/data-science-pipelines/pull/467) | UPSTREAM: carry: Phase 2 quality gates for AI Pipelines (retire Sanity) | sduvvuri1603 |
| [#438](https://github.com/opendatahub-io/data-science-pipelines/pull/438) | test: Enable MLflow e2e tests | VaniHaripriya |
| [#430](https://github.com/opendatahub-io/data-science-pipelines/pull/430) | fix: exclude TLS security scans from CI gate | ugiordan |
| [#412](https://github.com/opendatahub-io/data-science-pipelines/pull/412) | Main to stable merge | VaniHaripriya |
| [#392](https://github.com/opendatahub-io/data-science-pipelines/pull/392) | chore(test): fix and cleanup gpu tests | nsingla |
| [#381](https://github.com/opendatahub-io/data-science-pipelines/pull/381) | test: fixing reports for upgrade tests | nsingla |
| [#374](https://github.com/opendatahub-io/data-science-pipelines/pull/374) | test: adding a custom reporter to skip adding filtered out tests to the jun… | nsingla |
| [#365](https://github.com/opendatahub-io/data-science-pipelines/pull/365) | Sync master into stable | mprahl |
| [#362](https://github.com/opendatahub-io/data-science-pipelines/pull/362) | chore: sync upstream kubeflow/pipelines | dsp-developers |
| [#359](https://github.com/opendatahub-io/data-science-pipelines/pull/359) | test: adding support for disconnected tests to run during release validation | nsingla |
| [#353](https://github.com/opendatahub-io/data-science-pipelines/pull/353) | ci(fix): add repo to fix pr creation | nsingla |
| [#347](https://github.com/opendatahub-io/data-science-pipelines/pull/347) | chore: Merge upstream2 | nsingla |
| [#346](https://github.com/opendatahub-io/data-science-pipelines/pull/346) | ci(fix): always prioritize upstream frontend if there are conflicts | nsingla |
| [#345](https://github.com/opendatahub-io/data-science-pipelines/pull/345) | ci: adding workflow to sync dsp with upstream | nsingla |
| [#335](https://github.com/opendatahub-io/data-science-pipelines/pull/335) | chore: Merge master to stable | nsingla |
| [#334](https://github.com/opendatahub-io/data-science-pipelines/pull/334) | fix(ci): properly skip jobs in rhds when cachecEnabled=true with tld Enabled | nsingla |
| [#333](https://github.com/opendatahub-io/data-science-pipelines/pull/333) | Merge pull request #332 from nsingla/fix_v2_integration_tests | nsingla |
| [#332](https://github.com/opendatahub-io/data-science-pipelines/pull/332) | fix(ci): fixing pod to pod tls config in legacy v2 tests | nsingla |
| [#331](https://github.com/opendatahub-io/data-science-pipelines/pull/331) | chore: merge main into stable | nsingla |
| [#330](https://github.com/opendatahub-io/data-science-pipelines/pull/330) | fix (ci): using default tls cert when not deploying operator | nsingla |
| [#321](https://github.com/opendatahub-io/data-science-pipelines/pull/321) | fix(ci): fix deployment rhods | nsingla |
| [#317](https://github.com/opendatahub-io/data-science-pipelines/pull/317) | fix(ci): fixing frontend image build issue | nsingla |
| [#316](https://github.com/opendatahub-io/data-science-pipelines/pull/316) | fix dspo image tag for stable branch | nsingla |
| [#312](https://github.com/opendatahub-io/data-science-pipelines/pull/312) | chore: Merge master 20260407 | nsingla |
| [#311](https://github.com/opendatahub-io/data-science-pipelines/pull/311) | chore: Rebase upstream3 | nsingla |
| [#302](https://github.com/opendatahub-io/data-science-pipelines/pull/302) | chore: Rebase upstream | nsingla |
| [#286](https://github.com/opendatahub-io/data-science-pipelines/pull/286) | chore(ci): adding option to deploy using dsp operator and dspa cr | nsingla |
| [#271](https://github.com/opendatahub-io/data-science-pipelines/pull/271) | chore: Rebase KFP upstream to ODH | nsingla |
| [#270](https://github.com/opendatahub-io/data-science-pipelines/pull/270) | chore: upgrading go | nsingla |
| [#264](https://github.com/opendatahub-io/data-science-pipelines/pull/264) | UPSTREAM drop: Update ML Pipeline server address to facilitate TLS-enabled gRPC connection | alyssacgoins |

Automated/bot-authored PRs reviewed: [#525](https://github.com/opendatahub-io/data-science-pipelines/pull/525) (red-hat-konflux[bot]).

### opendatahub-io/pipelines-components (14 human, 1 automated)

| PR | Title | Author |
| --- | --- | --- |
| [#203](https://github.com/opendatahub-io/pipelines-components/pull/203) | Cherry pick latest upstream changes related to repo level tests | filip-komarzyniec |
| [#202](https://github.com/opendatahub-io/pipelines-components/pull/202) | chore: cherry pick Introduce jsonschema for metadata files validation | filip-komarzyniec |
| [#201](https://github.com/opendatahub-io/pipelines-components/pull/201) | fix(automl, autorag): remove redundant component Containerfile symlinks | DorotaDR |
| [#185](https://github.com/opendatahub-io/pipelines-components/pull/185) | chore(automl, autorag): switch AIPCC PyPI index from cpu-ubi9-test to cpu-ubi9 | DorotaDR |
| [#89](https://github.com/opendatahub-io/pipelines-components/pull/89) | fix: overriding RELATED_IMAGE in the init-managed-pipelines container | Wojciech-Rebisz |
| [#82](https://github.com/opendatahub-io/pipelines-components/pull/82) | docs: Update DSPO changes in managed pipelines | Wojciech-Rebisz |
| [#68](https://github.com/opendatahub-io/pipelines-components/pull/68) | ci: Adding support for Hermetic Builds | nsingla |
| [#62](https://github.com/opendatahub-io/pipelines-components/pull/62) | chore(deps): Use kfp v2.16.1 | Wojciech-Rebisz |
| [#53](https://github.com/opendatahub-io/pipelines-components/pull/53) | feat: add RAG pipeline components and multi-step pipeline | szaher |
| [#38](https://github.com/opendatahub-io/pipelines-components/pull/38) | Merge upstream to odh | VaniHaripriya |
| [#37](https://github.com/opendatahub-io/pipelines-components/pull/37) | ci: support stable branch in container-build | VaniHaripriya |
| [#33](https://github.com/opendatahub-io/pipelines-components/pull/33) | chore: Merge main into stable | nsingla |
| [#20](https://github.com/opendatahub-io/pipelines-components/pull/20) | Ignore .tekton/ for YAML linting | mprahl |
| [#2](https://github.com/opendatahub-io/pipelines-components/pull/2) | feat: Initial managed-pipeline.json generation | dryszka |

Automated/bot-authored PRs reviewed: [#14](https://github.com/opendatahub-io/pipelines-components/pull/14) (odh-devops-app[bot]).

### Other opendatahub-io repos

| Repo | PR | Title | Author |
| --- | --- | --- | --- |
| argo-workflows | [#81](https://github.com/opendatahub-io/argo-workflows/pull/81) | chore: Merge main into stable | jonburdo |
| argo-workflows | [#72](https://github.com/opendatahub-io/argo-workflows/pull/72) | chore(deps): upgrade golang.org/x/crypto to 0.52.0 | alyssacgoins |
| argo-workflows | [#71](https://github.com/opendatahub-io/argo-workflows/pull/71) | chore(deps): upgrade google.golang.org/grpc and associated dependencies | alyssacgoins |
| ml-metadata | [#26](https://github.com/opendatahub-io/ml-metadata/pull/26) | Backport CVE-2026-18618 fix: upgrade bundled gRPC/protobuf and fix upb builds on arm64/ppc64le | VaniHaripriya |
| mlflow | [#84](https://github.com/opendatahub-io/mlflow/pull/84) | Cherry-pick SQLAlchemy 2.1 support | mprahl |

Automated/bot-authored PRs reviewed: mlflow-operator [#59](https://github.com/opendatahub-io/mlflow-operator/pull/59) (dependabot[bot]), model-registry-operator [#774](https://github.com/opendatahub-io/model-registry-operator/pull/774) and [#745](https://github.com/opendatahub-io/model-registry-operator/pull/745) (dependabot[bot]).

### red-hat-data-services (32, RHDS-only — backport reviews of PRs already reviewed in ODH excluded)

| Repo | PR | Title | Author |
| --- | --- | --- | --- |
| argo-workflows | [#775](https://github.com/red-hat-data-services/argo-workflows/pull/775) | fix(executor): address CVE-2025-66626 path traversal in untar[rhoai-3.4] | VaniHaripriya |
| argo-workflows | [#774](https://github.com/red-hat-data-services/argo-workflows/pull/774) | fix(executor): address CVE-2025-66626 path traversal in untar[rhoai-3.3] | VaniHaripriya |
| argo-workflows | [#759](https://github.com/red-hat-data-services/argo-workflows/pull/759) | fix(deps): bump Go to 1.26.3 for CVE-2026-33811 [rhoai-3.3] | VaniHaripriya |
| argo-workflows | [#758](https://github.com/red-hat-data-services/argo-workflows/pull/758) | fix(deps): bump Go to 1.26.3 for CVE-2026-33811 [rhoai-3.4] | VaniHaripriya |
| argo-workflows | [#757](https://github.com/red-hat-data-services/argo-workflows/pull/757) | fix(deps): bump Go to 1.26.3 for CVE-2026-33811 [rhoai-2.25] | VaniHaripriya |
| argo-workflows | [#720](https://github.com/red-hat-data-services/argo-workflows/pull/720) | chore(fix): CVE fixes | nsingla |
| argo-workflows | [#581](https://github.com/red-hat-data-services/argo-workflows/pull/581) | chore: bump Go builders to 1.25.7 | nsingla |
| data-science-pipelines | [#2057](https://github.com/red-hat-data-services/data-science-pipelines/pull/2057) | chore: fix CI [rhoai-3.4] | alyssacgoins |
| data-science-pipelines | [#1676](https://github.com/red-hat-data-services/data-science-pipelines/pull/1676) | fix(konflux): keep openssl-libs in RPM lockfile on rhoai-2.25 | VaniHaripriya |
| data-science-pipelines | [#1650](https://github.com/red-hat-data-services/data-science-pipelines/pull/1650) | fix(deps): bump Go to 1.26.3 for CVE-2026-33814 on rhoai-3.3 | sduvvuri1603 |
| data-science-pipelines | [#1649](https://github.com/red-hat-data-services/data-science-pipelines/pull/1649) | fix(deps): bump Go to 1.26.3 for CVE-2026-33814 on rhoai-2.25 | sduvvuri1603 |
| data-science-pipelines | [#1634](https://github.com/red-hat-data-services/data-science-pipelines/pull/1634) | fix(ci): use Python 3.9 get-pip URL in apiserver Dockerfile [rhoai-2.25] | VaniHaripriya |
| data-science-pipelines | [#1584](https://github.com/red-hat-data-services/data-science-pipelines/pull/1584) | Backport mlflow tls fix to rhoai 3.5 ea.2 | VaniHaripriya |
| data-science-pipelines | [#1570](https://github.com/red-hat-data-services/data-science-pipelines/pull/1570) | fix(deps): bump Go dependencies to resolve critical CVEs [rhoai-3.3] | nsingla |
| data-science-pipelines | [#1271](https://github.com/red-hat-data-services/data-science-pipelines/pull/1271) | chore(deps): update minio image ref from to Quay from GCR (rhoai-2.25) | alyssacgoins |
| data-science-pipelines-operator | [#1093](https://github.com/red-hat-data-services/data-science-pipelines-operator/pull/1093) | fix(deps): bump Go to 1.26.3 for CVE-2026-33811 [rhoai-3.4] | VaniHaripriya |
| data-science-pipelines-operator | [#1065](https://github.com/red-hat-data-services/data-science-pipelines-operator/pull/1065) | fix: restore FIPS build flags in Dockerfile.konflux | pablofelix |
| data-science-pipelines-operator | [#1054](https://github.com/red-hat-data-services/data-science-pipelines-operator/pull/1054) | chore(fix): fixing cves | nsingla |
| data-science-pipelines-operator | [#893](https://github.com/red-hat-data-services/data-science-pipelines-operator/pull/893) | chore: upgrading go | nsingla |
| data-science-pipelines-operator | [#809](https://github.com/red-hat-data-services/data-science-pipelines-operator/pull/809) | chore(deps): update Go to 1.25.5 to address CVE-2025-61729 [rhoai-2.25] | alyssacgoins |
| konflux-central | [#4148](https://github.com/red-hat-data-services/konflux-central/pull/4148) | fix(konflux): restore non-hermetic ml-metadata builds (rhoai-3.7-ea.1) | syelluma123 |
| konflux-central | [#1920](https://github.com/red-hat-data-services/konflux-central/pull/1920) | disable s390x for odh-pipelines-components in RHOAI 3.4 | dryszka |
| konflux-central | [#1919](https://github.com/red-hat-data-services/konflux-central/pull/1919) | disable s390x for odh-pipelines-components | dryszka |
| ml-metadata | [#1280](https://github.com/red-hat-data-services/ml-metadata/pull/1280) | fix(konflux): add generic prefetch to on-push pipelinerun | KorneAlex |
| ml-metadata | [#1119](https://github.com/red-hat-data-services/ml-metadata/pull/1119) | Backport CVE-2026-18618 fix for odh-mlmd-grpc-server-rhel9[rhoai 2.25] | VaniHaripriya |
| ml-metadata | [#1118](https://github.com/red-hat-data-services/ml-metadata/pull/1118) | Backport CVE-2026-18618 fix for odh-mlmd-grpc-server-rhel9[rhoai 3.3] | VaniHaripriya |
| ml-metadata | [#1117](https://github.com/red-hat-data-services/ml-metadata/pull/1117) | Backport CVE-2026-18618 fix for odh-mlmd-grpc-server-rhel9[rhoai 3.4] | VaniHaripriya |
| pipelines-components | [#323](https://github.com/red-hat-data-services/pipelines-components/pull/323) | upgrade-pip | adysenrothman |
| pipelines-components | [#311](https://github.com/red-hat-data-services/pipelines-components/pull/311) | fix(build): bump certifi to 2026.10.23 to distrust eMudhra CAs | dryszka |
| pipelines-components | [#94](https://github.com/red-hat-data-services/pipelines-components/pull/94) | chore: remove tekton files that belong to midstream | Mateusz-Switala |
| pipelines-components | [#21](https://github.com/red-hat-data-services/pipelines-components/pull/21) | ci: Add support for hermetics | nsingla |
| rhods-devops-infra | [#536](https://github.com/red-hat-data-services/rhods-devops-infra/pull/536) | add pipelines-components and kserve-autogluon-server repos to automerger | mchamsed-rh |

## Open PRs

None — no open PRs authored by hbelmiro in any of these repos.

## Governance — OWNERS roles

### opendatahub-io/data-science-pipelines-operator

| Path | Approver | Reviewer |
| --- | --- | --- |
| / | Yes | Yes |

### opendatahub-io/data-science-pipelines

| Path | Approver | Reviewer |
| --- | --- | --- |
| / | Yes | Yes |
| kubernetes_platform/ | Yes | Yes |

### opendatahub-io/pipelines-components

| Path | Approver | Reviewer |
| --- | --- | --- |
| / | Yes | — |
| .github/ | Yes | Yes |
| docs/ | Yes | Yes |
| scripts/ | Yes | Yes |
| scripts/validate_metadata/tests/resources/directories_metadata/* (test fixtures) | Yes | partial |
| test_data/ | Yes | Yes |
| test_data/components/grouped/ml_models/linear_model/ | Yes | Yes |
| test_data/pipelines/grouped/etl_flows/daily_ingest/ | Yes | Yes |
| components/data_processing/yoda_data_processor/ | Yes | — |

### opendatahub-io/argo-workflows

| Path | Approver | Reviewer |
| --- | --- | --- |
| / | — | Yes |

### opendatahub-io/model-registry-operator

| Path | Approver | Reviewer |
| --- | --- | --- |
| / | Yes | Yes |

### red-hat-data-services mirrors

The RHDS repos `argo-workflows`, `data-science-pipelines`, `data-science-pipelines-operator`, and `pipelines-components` carry the same OWNERS entries as their opendatahub-io counterparts (forks kept in sync): approver+reviewer at the root of RHDS data-science-pipelines, data-science-pipelines-operator, and pipelines-components (plus the same subdirectory scopes), and reviewer-only in RHDS argo-workflows.

No OWNERS roles in: ilab-on-ocp, ml-metadata, mlflow, mlflow-operator, opendatahub-tests, operator-chaos, org-management, konflux-central, rhods-devops-infra.

## Merged PRs in secondary repos

### opendatahub-io/pipelines-components (17)

Excluded #32 (mirrors kubeflow/pipelines-components #139/#140).

| PR | Title | Merged |
| --- | --- | --- |
| [#376](https://github.com/opendatahub-io/pipelines-components/pull/376) | UPSTREAM: carry: Remove mprahl from OWNERS | 2026-11-17 |
| [#282](https://github.com/opendatahub-io/pipelines-components/pull/282) | Remove VaniHaripriya from OWNERS | 2026-09-30 |
| [#208](https://github.com/opendatahub-io/pipelines-components/pull/208) | Remove nsingla from OWNERS files | 2026-08-17 |
| [#207](https://github.com/opendatahub-io/pipelines-components/pull/207) | Update approvers list in OWNERS file | 2026-08-14 |
| [#144](https://github.com/opendatahub-io/pipelines-components/pull/144) | Merge main into stable | 2026-06-22 |
| [#110](https://github.com/opendatahub-io/pipelines-components/pull/110) | Merge KFP into main | 2026-05-28 |
| [#102](https://github.com/opendatahub-io/pipelines-components/pull/102) | Merge from KFP | 2026-05-27 |
| [#99](https://github.com/opendatahub-io/pipelines-components/pull/99) | UPSTREAM carry: chore: Add `no_parent_owners: true` to all component and pipeline OWNERS files | 2026-06-02 |
| [#85](https://github.com/opendatahub-io/pipelines-components/pull/85) | Merge kubeflow to odh | 2026-05-21 |
| [#78](https://github.com/opendatahub-io/pipelines-components/pull/78) | docs: Add guidelines for requesting managed pipeline runtime images | 2026-05-19 |
| [#75](https://github.com/opendatahub-io/pipelines-components/pull/75) | UPSTREAM carry: chore: Add platform-specific flag for Python in requirements generation | 2026-07-02 |
| [#40](https://github.com/opendatahub-io/pipelines-components/pull/40) | fix: Remove `--extra test` flag in Dockerfile's `uv sync` command | 2026-04-16 |
| [#27](https://github.com/opendatahub-io/pipelines-components/pull/27) | Merge main to stable | 2026-04-13 |
| [#26](https://github.com/opendatahub-io/pipelines-components/pull/26) | feat: compile managed pipeline YAMLs at build time | 2026-04-10 |
| [#23](https://github.com/opendatahub-io/pipelines-components/pull/23) | feat: Add initialization scripts and pipeline definitions for managed pipelines | 2026-04-08 |
| [#3](https://github.com/opendatahub-io/pipelines-components/pull/3) | fix: Align with red-hat-data-services/main to resolve sync merge conflicts | 2026-03-19 |
| [#1](https://github.com/opendatahub-io/pipelines-components/pull/1) | Cherry pick from RHDS | 2026-03-18 |

### opendatahub-io/argo-workflows (4)

| PR | Title | Merged |
| --- | --- | --- |
| [#77](https://github.com/opendatahub-io/argo-workflows/pull/77) | Remove VaniHaripriya from OWNERS | 2026-09-30 |
| [#69](https://github.com/opendatahub-io/argo-workflows/pull/69) | chore: Merge main into stable | 2026-06-19 |
| [#68](https://github.com/opendatahub-io/argo-workflows/pull/68) | chore: Move FIPS 140 configuration from Dockerfiles to go.mod | 2026-06-18 |
| [#67](https://github.com/opendatahub-io/argo-workflows/pull/67) | chore: Switch from OpenSSL FIPS to native Go FIPS 140-3 module | 2026-06-18 |

### opendatahub-io/operator-chaos (2)

| PR | Title | Merged |
| --- | --- | --- |
| [#7](https://github.com/opendatahub-io/operator-chaos/pull/7) | fix: make chaos experiment recovery measurement reflect real operator recovery | 2026-10-30 |
| [#8](https://github.com/opendatahub-io/operator-chaos/pull/8) | chore(deps): align nested SDK modules with root module (go 1.26, controller-runtime v0.24.1) | 2026-10-15 |

### opendatahub-io/mlflow-operator (2)

| PR | Title | Merged |
| --- | --- | --- |
| [#42](https://github.com/opendatahub-io/mlflow-operator/pull/42) | Refactor `mlflowToHelmValues` to use `runtime.DefaultUnstructuredConverter` | 2026-02-03 |
| [#37](https://github.com/opendatahub-io/mlflow-operator/pull/37) | Add CGO_ENABLED override for Apple Silicon container builds | 2026-01-29 |

### opendatahub-io/model-registry-operator (1)

| PR | Title | Merged |
| --- | --- | --- |
| [#734](https://github.com/opendatahub-io/model-registry-operator/pull/734) | fix: serve health probes from process start and release leader lease on shutdown | 2026-10-30 |

### opendatahub-io/opendatahub-tests (1)

| PR | Title | Merged |
| --- | --- | --- |
| [#2737](https://github.com/opendatahub-io/opendatahub-tests/pull/2737) | fix(image): pin odh user uid to 1001 for Jenkins runs | 2026-11-24 |

### red-hat-data-services/data-science-pipelines (16)

RHDS-only work: Konflux Dockerfile/toolchain management, release-branch backports with substantial adaptation, and branch merges. Pure backports of ODH PRs excluded.

| PR | Title | Merged |
| --- | --- | --- |
| [#1635](https://github.com/red-hat-data-services/data-science-pipelines/pull/1635) | fix(ci): cherry-pick init containers + CI fixes for rhoai-3.3 | 2026-08-18 |
| [#1633](https://github.com/red-hat-data-services/data-science-pipelines/pull/1633) | fix(ci): cherry-pick init containers (#12970) + CI deploy fixes | 2026-08-14 |
| [#1557](https://github.com/red-hat-data-services/data-science-pipelines/pull/1557) | chore: Remove stale cmake/clang/openssl from api Konflux Dockerfile | 2026-06-24 |
| [#1551](https://github.com/red-hat-data-services/data-science-pipelines/pull/1551) | chore: Update Konflux Dockerfiles to use Go toolset 1.26.3 and native Go FIPS 140 configuration | 2026-06-24 |
| [#1544](https://github.com/red-hat-data-services/data-science-pipelines/pull/1544) | chore: Update Konflux Dockerfiles to use Go toolset 1.26.3 and native Go FIPS 140 configuration | 2026-06-24 |
| [#1543](https://github.com/red-hat-data-services/data-science-pipelines/pull/1543) | chore: Update Konflux Dockerfiles to use Go toolset 1.26.3 and native Go FIPS 140 configuration | 2026-06-24 |
| [#1522](https://github.com/red-hat-data-services/data-science-pipelines/pull/1522) | chore: remove unused dnf install commands from Dockerfiles | 2026-06-02 |
| [#1521](https://github.com/red-hat-data-services/data-science-pipelines/pull/1521) | UPSTREAM carry: chore: update go-toolset to v1.26.2 in all Konflux Dockerfiles | 2026-06-01 |
| [#1520](https://github.com/red-hat-data-services/data-science-pipelines/pull/1520) | UPSTREAM carry: chore: update go-toolset to v1.26.2 in all Konflux Dockerfiles | 2026-06-01 |
| [#1459](https://github.com/red-hat-data-services/data-science-pipelines/pull/1459) | [rhoai-3.5-ea.1] fix: use multi-arch go-toolset 1.25.7 image digest in konflux Dockerfiles, downgrading from 1.25.9 to match go.mod | 2026-05-12 |
| [#1458](https://github.com/red-hat-data-services/data-science-pipelines/pull/1458) | fix: use multi-arch go-toolset 1.25.7 image digest in konflux Dockerfiles, downgrading from 1.25.9 to match go.mod | 2026-05-12 |
| [#1438](https://github.com/red-hat-data-services/data-science-pipelines/pull/1438) | fix(konflux): pin go-toolset digest to Go 1.25.7 to match go.mod | 2026-05-05 |
| [#1399](https://github.com/red-hat-data-services/data-science-pipelines/pull/1399) | chore(backend): update openssl version in Konflux API Dockerfile | 2026-04-22 |
| [#1398](https://github.com/red-hat-data-services/data-science-pipelines/pull/1398) | chore(backend): upgrade go-toolset in Konflux Dockerfiles from 1.24 to 1.25 | 2026-04-22 |
| [#1397](https://github.com/red-hat-data-services/data-science-pipelines/pull/1397) | chore(backend): upgrade go-toolset in Konflux Dockerfiles from 1.24 to 1.25 | 2026-04-22 |
| [#1363](https://github.com/red-hat-data-services/data-science-pipelines/pull/1363) | Merge remote-tracking branch 'upstream/stable' | 2026-04-15 |

### red-hat-data-services/data-science-pipelines-operator (4)

| PR | Title | Merged |
| --- | --- | --- |
| [#1121](https://github.com/red-hat-data-services/data-science-pipelines-operator/pull/1121) | Fix CI integration tests | 2026-08-20 |
| [#1039](https://github.com/red-hat-data-services/data-science-pipelines-operator/pull/1039) | chore: Update Konflux Dockerfile to use Go toolset 1.26.3 and native Go FIPS 140 configuration | 2026-06-24 |
| [#1031](https://github.com/red-hat-data-services/data-science-pipelines-operator/pull/1031) | chore: Merge main into rhoai-3.5-ea.2 | 2026-06-24 |
| [#1030](https://github.com/red-hat-data-services/data-science-pipelines-operator/pull/1030) | chore: Update Konflux Dockerfile to use Go toolset 1.26.3 and native Go FIPS 140 configuration | 2026-06-24 |

### red-hat-data-services/argo-workflows (5)

| PR | Title | Merged |
| --- | --- | --- |
| [#735](https://github.com/red-hat-data-services/argo-workflows/pull/735) | chore: Sync from main to rhoai-3.5 | 2026-07-16 |
| [#705](https://github.com/red-hat-data-services/argo-workflows/pull/705) | chore: Update Dockerfiles to use Go toolset 1.26.3 and native Go FIPS 140 configuration in Konflux Dockerfiles | 2026-06-24 |
| [#700](https://github.com/red-hat-data-services/argo-workflows/pull/700) | chore: Update Dockerfiles to use Go toolset 1.26.3 and native Go FIPS 140 configuration in Konflux Dockerfiles | 2026-06-24 |
| [#699](https://github.com/red-hat-data-services/argo-workflows/pull/699) | chore: Update Dockerfiles to use Go toolset 1.26.3 and native Go FIPS 140 configuration in Konflux Dockerfiles | 2026-06-24 |
| [#571](https://github.com/red-hat-data-services/argo-workflows/pull/571) | chore: Merge main and fix recurring auto-merge conflicts | 2026-04-02 |

### red-hat-data-services/konflux-central (6)

| PR | Title | Merged |
| --- | --- | --- |
| [#4038](https://github.com/red-hat-data-services/konflux-central/pull/4038) | fix(konflux): restore non-hermetic ml-metadata builds (3.6 EA2 behavior) | 2026-10-30 |
| [#4037](https://github.com/red-hat-data-services/konflux-central/pull/4037) | fix(konflux): restore non-hermetic ml-metadata builds (3.6 EA2 behavior) | 2026-10-30 |
| [#4007](https://github.com/red-hat-data-services/konflux-central/pull/4007) | Revert "Add generic prefetch to ml-metadata pull-request pipelinerun" (#3952) | 2026-10-29 |
| [#4006](https://github.com/red-hat-data-services/konflux-central/pull/4006) | Revert "Add generic prefetch to ml-metadata pipelinerun" (#3918) | 2026-10-29 |
| [#3952](https://github.com/red-hat-data-services/konflux-central/pull/3952) | Add generic prefetch to ml-metadata pull-request pipelinerun (main) | 2026-10-27 |
| [#3918](https://github.com/red-hat-data-services/konflux-central/pull/3918) | Add generic prefetch to ml-metadata pipelinerun (rhoai-3.6) | 2026-10-23 |

### red-hat-data-services/ml-metadata (3)

| PR | Title | Merged |
| --- | --- | --- |
| [#1312](https://github.com/red-hat-data-services/ml-metadata/pull/1312) | Fix Dockerfile.konflux for Bazel 6.3.2 and upb aarch64/ppc64le build | 2026-11-04 |
| [#1299](https://github.com/red-hat-data-services/ml-metadata/pull/1299) | Revert "fix(konflux): add rpm prefetch setup for hermetic build" (#1279, #1280) | 2026-10-29 |
| [#1279](https://github.com/red-hat-data-services/ml-metadata/pull/1279) | fix(konflux): add rpm prefetch setup for hermetic build | 2026-10-23 |

### red-hat-data-services/pipelines-components (2)

| PR | Title | Merged |
| --- | --- | --- |
| [#53](https://github.com/red-hat-data-services/pipelines-components/pull/53) | Cherry pick: ci: Adding support for Hermetic Builds | 2026-05-20 |
| [#52](https://github.com/red-hat-data-services/pipelines-components/pull/52) | chore: Bump `kfp` and `kfp-kubernetes` to version 2.16.1 in requirements.txt | 2026-05-15 |

### red-hat-data-services/rhods-devops-infra (2)

| PR | Title | Merged |
| --- | --- | --- |
| [#1101](https://github.com/red-hat-data-services/rhods-devops-infra/pull/1101) | feat(sync): sync AI Pipelines components from main/master instead of stable | 2026-11-24 |
| [#519](https://github.com/red-hat-data-services/rhods-devops-infra/pull/519) | Add pipelines-components to upstream auto-merge configuration | 2026-03-18 |

## Contribution highlights

### Architecture and design — Managed Pipelines

The defining initiative of the year: designed and landed the **Managed Pipelines** architecture end to end. In the operator this spans the `--managedPipelinesDir` flag ([#1011](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1011)), managed-pipelines.json validation and caching in the DSP API controller ([#1003](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1003)), image mapping via `MANAGEDPIPELINES_IMAGES` and `RELATED_IMAGE_*` ([#995](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/995)), `PipelineVersion` CRD `versionName` driven by platform version ([#1069](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1069), [#1070](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1070)), and enabling Managed Pipelines by default ([#1128](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1128)). The pipeline side adds managed manifest support in `LoadSamples` ([#315](https://github.com/opendatahub-io/data-science-pipelines/pull/315)) and rhoai-version tagging ([#413](https://github.com/opendatahub-io/data-science-pipelines/pull/413)); the components repo contributes the build-time compilation of managed pipeline YAMLs ([#26](https://github.com/opendatahub-io/pipelines-components/pull/26), [#23](https://github.com/opendatahub-io/pipelines-components/pull/23)) and contributor docs ([#78](https://github.com/opendatahub-io/pipelines-components/pull/78)). Also delivered DRA (Dynamic Resource Allocation) support across all DSPA components ([#1090](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1090)) and the default StorageClass config for CreatePVC tasks ([#1144](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1144)).

### Security improvements

- RBAC permission reduction for pipeline-runner and operator ClusterRoles ([#1097](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1097))
- Service-account allow-listing (`ALLOWEDSERVICEACCOUNTS`) in apiserver deployments ([#1096](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1096))
- Database configuration hardening incl. crypto/rand secret generation and DSN injection fixes ([#1098](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1098), [#1099](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1099))
- Non-root default user in images ([#998](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/998), [#523](https://github.com/opendatahub-io/data-science-pipelines/pull/523), [#2737](https://github.com/opendatahub-io/opendatahub-tests/pull/2737))
- Migrated the FIPS story from OpenSSL patches to the native Go FIPS 140-3 module across DSP, DSPO, and Argo ([#1062](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1062), [#67](https://github.com/opendatahub-io/argo-workflows/pull/67))

### CI/CD and release engineering ownership

Rebuilt the CI foundation of the ODH AI Pipelines stack: enabled push-triggered CI on main/stable/versioned branches, added KinD integration tests that build DSP and Argo images from source with fork detection ([#1088](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1088), [#1093](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1093)), Go version consistency enforcement ([#1016](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1016)), and webhook TLS/readiness fixes for Kind ([#1148](https://github.com/opendatahub-io/data-science-pipelines-operator/pull/1148)). On the RHDS side, owned Konflux build infrastructure: Go toolset/FIPS alignment across all Konflux Dockerfiles, hermetic build experiments with prefetch and their reverts (ml-metadata, konflux-central), and the sync tooling change moving AI Pipelines component syncs from stable to main ([rhods-devops-infra #1101](https://github.com/red-hat-data-services/rhods-devops-infra/pull/1101)). Also authored the new operator-chaos repository work measuring real operator recovery ([#7](https://github.com/opendatahub-io/operator-chaos/pull/7)).

### Community and mentoring

117 human PR reviews across 12 repos, acting as the effective quality gate for the AI Pipelines team — reviewing TLS hardening, the AIPipelines module API, chaos testing, CRD changes, and bot/automation work from teammates (ugiordan, mprahl, sduvvuri1603, nsingla, VaniHaripriya, alyssacgoins, dbasunag, and others). Maintains OWNERS files across five repos, performed the 2026 roster cleanup (adding self and nsingla as approvers, moving inactive members to emeritus), and holds approver+reviewer roles at the root of data-science-pipelines-operator, data-science-pipelines, pipelines-components, and model-registry-operator.
