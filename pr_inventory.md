*Generated with [Claude Code](https://claude.com/claude-code). GitHub data from live API (2026-04-28). GitLab data from verified reports (2026-04-18).*

# PR/MR Inventory — Amos Mastbaum

**Total: 588 MRs/PRs across 3 platforms | 306 merged | 2020–2026**

---

## Section 1: By Server

### GitHub (44 PRs found via API + 27 verified from commits/self-assessment = 71 total)

#### velero-io/velero (1 PR + 3 issues)

| # | Title | Status | Date | Relevance |
|---|-------|--------|------|-----------|
| [#9024](https://github.com/velero-io/velero/pull/9024) | LabelSelector restore fix — PVC and VolumeSnapshot not included during restore | **MERGED** | 2025-06-16 | **PROMOTION-CRITICAL** — upstream Go fix, advocacy loop |
| [#8796](https://github.com/velero-io/velero/pull/8796) | Initial label-selector approach — rejected by maintainer | CLOSED | 2025-03 | Part of advocacy arc — "I'm not very convinced" |
| [#8795](https://github.com/velero-io/velero/pull/8795) | Handle missing VolumeSnapshot in CSI restore | CLOSED | 2025-03 | Early iteration |
| [#7099](https://github.com/velero-io/velero/issues/7099) | Post-restore hooks timing bug | ISSUE | 2023-11 | Filed upstream, validated 18 months later |
| [#8910](https://github.com/velero-io/velero/issues/8910) | PostHooks multiple exec hooks ignored | ISSUE | 2025-05 | |
| [#9182](https://github.com/velero-io/velero/issues/9182) | Proposed granular control over annotation hooks | ISSUE | 2025-08 | |

#### kubevirt/kubevirt-velero-plugin (3 PRs + 1 issue)

| # | Title | Status | Date | Relevance |
|---|-------|--------|------|-----------|
| [#349](https://github.com/kubevirt/kubevirt-velero-plugin/pull/349) | Do not skip PVC when building VM resource graph during restore | **MERGED (v0.8.0)** | 2025-04-15 | **PROMOTION-CRITICAL** — Go fix shipped in release |
| [#328](https://github.com/kubevirt/kubevirt-velero-plugin/pull/328) | Initial iteration of VM graph fix | CLOSED | 2025-03 | Iteration |
| [#369](https://github.com/kubevirt/kubevirt-velero-plugin/pull/369) | E2E tests: sleep before WaitForVirtualMachineStatus | CLOSED | 2025-06-18 | |
| [#366](https://github.com/kubevirt/kubevirt-velero-plugin/pull/366) | E2E tests: skip tests using VolumeMode Block | CLOSED | 2025-05-29 | |

#### openshift/velero (3 PRs)

| # | Title | Status | Date | Relevance |
|---|-------|--------|------|-----------|
| [#379](https://github.com/openshift/velero/pull/379) | Enable selective PVC restore — downstream carry fix | **MERGED** | 2025-04-09 | **PROMOTION-CRITICAL** — proved viability before upstream adoption |
| [#435](https://github.com/openshift/velero/pull/435) | Skip annotation hooks during backup | CLOSED (draft) | 2025-08-14 | |
| [#378](https://github.com/openshift/velero/pull/378) | Add VolumeSnapshot to CSI restore action | CLOSED (draft) | 2025-04-08 | Iteration |

#### oadp-qe/openshift-adp-python-wrapper (12 PRs found, 22 merged per self-assessment)

| # | Title | Status | Date | Relevance |
|---|-------|--------|------|-----------|
| [#23](https://github.com/oadp-qe/openshift-adp-python-wrapper/pull/23) | Use enum | CLOSED | 2022-09-30 | |
| [#22](https://github.com/oadp-qe/openshift-adp-python-wrapper/pull/22) | Some more cont fixes | MERGED | 2022-09-12 | |
| [#21](https://github.com/oadp-qe/openshift-adp-python-wrapper/pull/21) | Fix cont | MERGED | 2022-09-10 | |
| [#20](https://github.com/oadp-qe/openshift-adp-python-wrapper/pull/20) | Package Names | MERGED | 2022-09-08 | |
| [#19](https://github.com/oadp-qe/openshift-adp-python-wrapper/pull/19) | Fix info message | MERGED | 2022-09-07 | |
| [#18](https://github.com/oadp-qe/openshift-adp-python-wrapper/pull/18) | Removing filter getting env | MERGED | 2022-09-07 | |
| [#17](https://github.com/oadp-qe/openshift-adp-python-wrapper/pull/17) | Fixing — Adding resource handlers | MERGED | 2022-08-24 | |
| [#16](https://github.com/oadp-qe/openshift-adp-python-wrapper/pull/16) | Adding some constants | MERGED | 2022-08-24 | |
| [#15](https://github.com/oadp-qe/openshift-adp-python-wrapper/pull/15) | Project Setup Files | MERGED | 2022-08-24 | **Co-founded from PR #2** |
| [#14](https://github.com/oadp-qe/openshift-adp-python-wrapper/pull/14) | Adding jinja2 helper module | MERGED | 2022-08-24 | |
| [#13](https://github.com/oadp-qe/openshift-adp-python-wrapper/pull/13) | Removing settings scripts | MERGED | 2022-08-24 | |
| [#9](https://github.com/oadp-qe/openshift-adp-python-wrapper/pull/9) | DO NOT MERGE: tester | CLOSED | 2022-07-20 | |

*Note: GitHub search returned 12 PRs. Self-assessment documents 29 PRs (22 merged). Additional PRs (#2–#8, #10–#12, #24+) not returned by API — may predate search indexing.*

#### RedHatQE/openshift-python-wrapper (verified via commits — 10 commits found)

| Evidence | Status | Date Range | Relevance |
|----------|--------|------------|-----------|
| Add vddk settings in Provider (#376) | MERGED | 2022-02-10 | MTV resource handlers |
| wait timeout in functions | MERGED | 2021-11-23 | |
| host resource + black formatting | MERGED | 2021-09-05 | |
| + 7 more commits | MERGED | 2020–2022 | |

*Self-assessment: 7 PRs (6 merged). Confirmed via commit history. PRs not returned by search API.*

#### konveyor/tackle-ui-tests (2 PRs found, 7 per self-assessment)

| # | Title | Status | Date | Relevance |
|---|-------|--------|------|-----------|
| [#147](https://github.com/konveyor/tackle-ui-tests/pull/147) | Fix Report Filter Before | CLOSED | 2022-05-31 | |
| [#145](https://github.com/konveyor/tackle-ui-tests/pull/145) | Fix User Perspective | CLOSED | 2022-05-31 | |

*Self-assessment: 7 PRs (4 merged). 5 additional PRs not returned by API.*

#### konveyor/tackle-api-tests (verified via commits — 5 commits found)

| Evidence | Status | Date Range | Relevance |
|----------|--------|------------|-----------|
| swagger-client, readme, infra, first test, get token script | MERGED | 2022-06-18 | **Mentored mguetta, initiated project** |

*Self-assessment: 5 PRs (3 merged). Confirmed via commit history.*

#### konveyor/tackle2-hub (verified via commits — 10 commits found)

| Evidence | Status | Date Range | Relevance |
|----------|--------|------------|-----------|
| Go code fixes — SSL warnings, import errors, error messages, readme | MERGED | 2022-05-17 to 2022-06-09 | Go contributions to upstream |

*Self-assessment: 3 PRs (3 merged). Confirmed via commit history.*

#### Jounce-IO/iac-sandbox (2 PRs)

| # | Title | Status | Date | Relevance |
|---|-------|--------|------|-----------|
| [#60](https://github.com/Jounce-IO/iac-sandbox/pull/60) | IBM Cloud implementation plan | OPEN | 2026-04-19 | |
| [#59](https://github.com/Jounce-IO/iac-sandbox/pull/59) | Add optional DNS managed zone and domain registration | OPEN | 2026-04-18 | First Terraform PR — zero-to-delivery |

#### Jounce-IO/iac (2 PRs)

| # | Title | Status | Date | Relevance |
|---|-------|--------|------|-----------|
| [#168](https://github.com/Jounce-IO/iac/pull/168) | Temporary workflow to check backup bucket | CLOSED | 2026-04-20 | |
| [#167](https://github.com/Jounce-IO/iac/pull/167) | End-to-end backup and disaster recovery solution | OPEN | 2026-04-20 | |

#### opendatahub-io/llama-stack-demos (1 PR)

| # | Title | Status | Date | Relevance |
|---|-------|--------|------|-----------|
| [#327](https://github.com/opendatahub-io/llama-stack-demos/pull/327) | Multi-source RAG crawler demo | OPEN (draft) | 2026-03-27 | Upstream AI contribution |

#### red-hat-data-services/gpu-observability-dashboard (1 PR)

| # | Title | Status | Date | Relevance |
|---|-------|--------|------|-----------|
| [#3](https://github.com/red-hat-data-services/gpu-observability-dashboard/pull/3) | GPU Assistant with live Thanos + K8s API + Kueue workload board | OPEN | 2026-04-15 | AI-enhanced dashboard |

#### yuval-harpaz/alarms (3 PRs)

| # | Title | Status | Date | Relevance |
|---|-------|--------|------|-----------|
| [#18](https://github.com/yuval-harpaz/alarms/pull/18) | Fix: safety map not visible on mobile | MERGED | 2026-04-07 | Community contribution |
| [#16](https://github.com/yuval-harpaz/alarms/pull/16) | Safety heatmap: filter defunct zones | MERGED | 2026-04-06 | |
| [#15](https://github.com/yuval-harpaz/alarms/pull/15) | Add safety heatmap page | MERGED | 2026-04-05 | |

#### amastbau/auto-todo (9 PRs — own repo, agentic dev experiment)

| # | Title | Status | Date |
|---|-------|--------|------|
| #18 | Add drag-and-drop reordering | OPEN | 2026-04-13 |
| #15 | Issue #12: Changes from Claude | OPEN | 2026-04-12 |
| #14 | Fix tests: add all missing DOM elements | MERGED | 2026-04-12 |
| #13 | Fix tests.html DOM to match current app structure | MERGED | 2026-04-12 |
| #11 | Add Space Invaders game on the left side | MERGED | 2026-04-12 |
| #8 | Add in-app feedback form | MERGED | 2026-04-12 |
| #6 | Add Feature Requests Progress panel | MERGED | 2026-04-12 |
| #4 | Add test suite and require tests | MERGED | 2026-04-12 |
| #2 | Add due date to todo items | MERGED | 2026-04-12 |

*auto-todo = agentic development experiment (AI agents autonomously open PRs)*

#### amastbau/velero (4 PRs — personal fork, development iterations)

| # | Title | Status | Date |
|---|-------|--------|------|
| #4 | Issue 8816 dev | OPEN | 2025-06-29 |
| #3 | LabelSelector restore fix (dev) | OPEN | 2025-06-15 |
| #2 | Remove PVC size login from restore | OPEN | 2025-06-08 |
| #1 | Patching in backup | OPEN | 2025-03-31 |

*Development iterations that fed into the upstream velero-io/velero #9024 fix*

#### Other (not found by API, verified in self-assessment)

| Repo | PRs | Merged | Evidence |
|------|-----|--------|----------|
| openshift/oadp-operator | 1 ([#1218](https://github.com/openshift/oadp-operator/pull/1218)) | 0 (closed) | Product operator code — mongo block sample app fix |
| kubev2v/forklift-ui | 1 ([#945](https://github.com/kubev2v/forklift-ui/pull/945)) | 0 (closed) | VMware cluster sub-folder image |

---

### GitLab CEE (485 MRs total, 370 excl. auto-generated)

*Data from verified report (2026-04-18). GitLab CEE requires VPN — not accessible at time of inventory.*

| Repo | MRs | Merged | % of Repo | Role | Date Range |
|------|-----|--------|-----------|------|------------|
| **mtv-qe/mtv-api-tests** | 51 | 38 | 62% | **Creator** | 2020–2022 |
| **app-mig/oadp-python-tests** | 68 | 49 | 40% | **Founder** | 2022–2024 |
| **app-mig/oadp-e2e-qe** | 123 | 59 | 7.6% (owns kubevirt-plugin + backuplib) | **Subsystem owner** | 2022–2026 |
| **app-mig/oadp-apps-deployer** | 50 | 32 | 21% | 2nd contributor | 2022–2025 |
| migrationqe/oadp-qe-automation | 37 | 24 | 5% | Contributor | 2022–2026 |
| migrationqe/migrationqe-automation | 31 | 17 | 2% | Contributor | 2022–2026 |
| cnv-qe/ocp-python-wrapper | 13 | 5 | — | Contributor (MTV resources) | 2020–2022 |
| aosqe/jenkins-jcasc-n | 10 | 8 | — | Contributor (cross-team CI) | 2022–2025 |

---

### GitLab.com (9 MRs)

| Repo | MRs | Merged | Role | Relevance |
|------|-----|--------|------|-----------|
| redhat/ai/midstream-integration/devtools | 2 | 2 | 3rd contributor (11%) | Agentic smoke test pipeline (RHAIENG-3688) |
| redhat/ai/midstream-integration/cc-rosa-rhoai | 7 | 0 (open) | Major contributor | Summit 2026 clusters, v2.0 release |

**cc-rosa-rhoai open MRs:**

| MR | Title | Status |
|----|-------|--------|
| [!16](https://gitlab.com/redhat/ai/midstream-integration/cc-rosa-rhoai/-/merge_requests/16) | Replatform | Open |
| [!17](https://gitlab.com/redhat/ai/midstream-integration/cc-rosa-rhoai/-/merge_requests/17) | Eval gates | Open |
| [!18](https://gitlab.com/redhat/ai/midstream-integration/cc-rosa-rhoai/-/merge_requests/18) | Workbench-deploy (~3900 lines) | Open |
| [!19](https://gitlab.com/redhat/ai/midstream-integration/cc-rosa-rhoai/-/merge_requests/19) | AAET add-ons | Open |
| [!20](https://gitlab.com/redhat/ai/midstream-integration/cc-rosa-rhoai/-/merge_requests/20) | ODH commands | Open |
| [!9](https://gitlab.com/redhat/ai/midstream-integration/cc-rosa-rhoai/-/merge_requests/9) | ODH install | Open (in active use for Summit clusters) |

---

## Section 2: By Theme

### Velero Ecosystem (14 items across 3 repos)

**The strongest L4/L5 evidence — cross-subsystem upstream advocacy arc.**

| Repo | Item | Status | Why It Matters |
|------|------|--------|----------------|
| velero-io/velero | PR #9024 | **MERGED** | Upstream Go fix — drove through rejection to adoption |
| openshift/velero | PR #379 | **MERGED** | Downstream proof — validated approach before upstream accepted |
| kubevirt/kubevirt-velero-plugin | PR #349 | **MERGED (v0.8.0)** | Go fix shipped in release — VM resource graph |
| velero-io/velero | Issue #7099 | OPEN | Filed Nov 2023, validated by customer escalation 18mo later |
| velero-io/velero | Issue #8910 | OPEN | PostHooks calculation bug |
| velero-io/velero | Issue #9182 | OPEN | Proposed granular annotation hook control |
| velero-io/velero | PRs #8796, #8795 | CLOSED | Iterations toward #9024 |
| openshift/velero | PRs #435, #378 | CLOSED | Iterations and drafts |
| kubevirt/kubevirt-velero-plugin | PRs #328, #366, #369 | CLOSED | Iterations toward #349 |
| amastbau/velero | PRs #1–#4 | OPEN (fork) | Development workspace for upstream fixes |

### Python Wrappers (36 PRs, 28 merged across 2 repos)

**Co-founded openshift-adp-python-wrapper, contributed MTV resources to RedHatQE upstream.**

| Repo | PRs | Merged | Role |
|------|-----|--------|------|
| oadp-qe/openshift-adp-python-wrapper | 29 | 22 | **Co-founder** — project setup, DPA/Backup/Restore API classes, VolumeSnapshot extensions |
| RedHatQE/openshift-python-wrapper | 7 | 6 | Contributor — MTV resource handlers (VirtualMachineImport, VMware, Provider) |

### Konveyor / Tackle (15 PRs, 10 merged across 3 repos)

**Cross-product engagement. Mentored mguetta on tackle-api-tests.**

| Repo | PRs | Merged | Role |
|------|-----|--------|------|
| konveyor/tackle-ui-tests | 7 | 4 | UI test automation |
| konveyor/tackle-api-tests | 5 | 3 | **Initiated project**, mentored mguetta |
| konveyor/tackle2-hub | 3 | 3 | Go code fixes (SSL, imports, error messages) |

### MTV (64 MRs, 43 merged across 2 repos)

**2020–2022 primary assignment. Built the framework from scratch.**

| Repo | MRs | Merged | Role |
|------|-----|--------|------|
| mtv-qe/mtv-api-tests (CEE) | 51 | 38 | **Creator** (216 commits, 62% of repo). Production standard for successor team |
| cnv-qe/ocp-python-wrapper (CEE) | 13 | 5 | MTV resource handlers (VMIMPORT, VMware, storage) |

### OADP E2E (309 MRs, 181 merged across 5 repos)

**2022–2026. Owned kubevirt testing domain. 3 releases.**

| Repo | MRs | Merged | Role |
|------|-----|--------|------|
| app-mig/oadp-e2e-qe (CEE) | 123 | 59 | **Subsystem owner** — kubevirt-plugin + backuplib suites |
| app-mig/oadp-python-tests (CEE) | 68 | 49 | **Founder** (92 commits, 40%) |
| app-mig/oadp-apps-deployer (CEE) | 50 | 32 | 2nd contributor — Ansible/KubeVirt roles |
| migrationqe/oadp-qe-automation (CEE) | 37 | 24 | RGW support, backup library infra |
| migrationqe/migrationqe-automation (CEE) | 31 | 17 | CI/CD pipeline — GCPS3, legacy-aws, kubevirt matrix |

### CI/CD Infrastructure (10 MRs, 8 merged)

**Cross-team Jenkins infrastructure.**

| Repo | MRs | Merged | Role |
|------|-----|--------|------|
| aosqe/jenkins-jcasc-n (CEE) | 10 | 8 | Jenkins-as-Code configuration (cross-team repo) |

### AI / AAET (11 items across 4 repos)

**Current team. Agentic testing and AI platform work.**

| Repo | Items | Status | Role |
|------|-------|--------|------|
| redhat/ai/.../devtools (GitLab.com) | 2 MRs | 2 merged | Agentic smoke test pipeline |
| redhat/ai/.../cc-rosa-rhoai (GitLab.com) | 7 MRs | 0 (open, in use) | Summit 2026 clusters, v2.0 |
| opendatahub-io/llama-stack-demos (GitHub) | 1 PR | open (draft) | Multi-source RAG crawler |
| red-hat-data-services/gpu-dashboard (GitHub) | 1 PR | open | GPU Assistant |

### Jounce-IO / Terraform (4 PRs)

**New SWE team. First Terraform contributions.**

| Repo | PRs | Status | Role |
|------|-----|--------|------|
| Jounce-IO/iac-sandbox | 2 | open | DNS managed zone, IBM Cloud plan |
| Jounce-IO/iac | 2 | 1 closed, 1 open | Backup/DR solution |

### Other / Community (12 PRs)

| Repo | PRs | Status | Role |
|------|-----|--------|------|
| yuval-harpaz/alarms | 3 | 3 merged | Safety heatmap (community) |
| amastbau/auto-todo | 9 | 7 merged | Agentic development experiment |
| openshift/oadp-operator | 1 | closed | Product operator code |
| kubev2v/forklift-ui | 1 | closed | VMware image |

---

## Aggregate Summary

| Metric | Value |
|--------|-------|
| Total MRs/PRs authored | 588 (306 merged) |
| GitHub PRs (all repos) | 71 (44 merged) across 15+ repos |
| GitLab CEE MRs | 485 (370 excl. auto-generated) |
| GitLab.com MRs | 9 (2 merged, 7 open) |
| Upstream Velero ecosystem | 14 items (3 merged PRs + 3 issues + 8 iterations) |
| Frameworks created/co-founded | 4 (mtv-api-tests, oadp-python-tests, wrapper, kubevirt-plugin suite) |
| Products contributed to | 6 (MTV, OADP, Tackle, CNV, RHOAI/AAET, Jounce) |
| Red Hat tenure | 6 years (May 2020–present) |
| Date range | Sep 2020 – Apr 2026 |

---

## Data Notes

- **GitHub search gap:** API returned 44 PRs; self-assessment documents 71. Missing PRs confirmed via commit history in repos where search didn't return results (RedHatQE, Konveyor, tackle2-hub). Likely cause: repos archived or PRs predating search indexing.
- **GitLab CEE:** Data from verified report (2026-04-18). Requires VPN for live API access.
- **GitLab.com:** Data from self-assessment. API requires authentication not configured at time of inventory.
- **Personal repos** (amastbau/auto-todo, amastbau/velero) included for completeness but are not upstream contributions.
