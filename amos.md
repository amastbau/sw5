# Projects & Technical Experience

Amos Mastbaum

---

## AIPCC (2026–present)

### Release Cycle Metrics Dashboard (RHOAIENG-76482)
Team needed release cycle timing visibility in the release-readiness dashboard. Metrics like code-freeze-to-release duration and checkpoint timing were tracked manually, no automated tracking or trend analysis.

**What I did**:
- Designed and implemented Release Cycle Timing Metrics backend (rhods-qe-tools MR !328)
- Built frontend dashboard component with visualizations (rhai-org-pulse PR #1448)
- Integrated Jira field extraction, date parsing, and scheduled metric uploads
- All CI checks passing; pending review and merge

**Tech**: Python, Jira API, GitLab CI/CD, React/frontend visualization

---

### RHAII on RHOAI Integration Test Suite (AIPCC-19537)
Team needed automated validation that RHAII builds work on stable RHOAI releases. Problem: mapt (team's cluster provisioning tool) only installed latest RHOAI from fast channel, but we needed to test against stable versions.

**What I did**:
- Added `--operator-channel` parameter to mapt upstream (Go: the parameter itself, SNO binary alias fix, shell-escape validation, propagation to Tekton templates, and an InstanceFamilies filter to avoid expensive GPU instance types)
- Built Tekton pipeline: provision SNO cluster with stable RHOAI → deploy RHAII as KServe → smoke test the inference API
- Pipeline specs in konflux-data, running on Konflux stone-prod-p02 cluster

**Tech**: Go, Tekton YAML, KServe/RHOAI APIs, AWS instance filtering

---

### IBM Cloud Infrastructure Automation (Q2 2026)
Team needed automated pipeline for provisioning and testing on IBM Cloud. Team had been using GCP; IBM Cloud was new territory.

**What I did**:
- Led the Designe and Wrote Terraform modules and github actions for project-bootstrap (resource groups, IAM policies, DNS zones), persistence (PostgreSQL databases with HMAC credentials stored in Secrets Manager), and cert-manager/External Secrets Operator integration
- Built pipeline infrastructure for provisioning and running tests

**Tech**: Terraform, IBM Cloud APIs (CIS, Secrets Manager, Certificate Manager, VPC), Bash scripting

---

### cc-rosa-rhoai CLI Tool (Q4 2025–Q1 2026)
Team needed repeatable way to provision ROSA clusters with RHOAI/ODH for Summit demos and testing. Manual provisioning was error-prone and inconsistent.

**What I did**:
- Extended the skills and scripts to support RHOAI (and upstream ODH) deployment over rosa.


**Tech**: Python, ROSA CLI, RHOAI/ODH APIs, click framework

---

### Agentic Smoke Test CI Pipeline (AIPCC-16104)
Summit demo clusters needed nightly health checks to catch regressions before customer-facing events.

**What I did**:
- Wrote ADR (Architecture Decision Record) defining 3-tier test strategy (minimal/medium/full coverage)
- Built Python pytest harness with Slack notifications
- Integrated into team CI for nightly runs

**Tech**: Python, pytest, GitLab CI/CD, Slack webhooks, RHOAI/ODH APIs

---

## OADP (2022–2025)

### Velero PVC Restore Graph Fix
VMs were silently losing PVCs during restore operations. Root cause was in the kubevirt-velero-plugin's resource graph builder — it wasn't correctly tracking PVC dependencies.

**What I did**:
- Traced the bug through 3 codebases (Velero core, kubevirt-velero-plugin, OADP downstream)
- Proposed fix upstream — maintainer initially rejected it ("not convinced this should be upstream")
- Implemented and tested in downstream fork, proved it worked
- Upstream adopted the approach later
- Shipped in kubevirt-velero-plugin v0.8.0

**Tech**: Go, Kubernetes API, Velero plugin architecture, CSI/DataMover internals

---

### KubeVirt Test Infrastructure
OADP needed comprehensive testing for OpenShift Virtualization (kubevirt) backup/restore scenarios. Nothing existed when I started.

**What I did**:
- Created kubevirt-plugin test suite from scratch
- build  backuplib test suite across multiple leases
- Built Ansible/KubeVirt deployment roles in oadp-apps-deployer
- Configured CI matrices: which kubevirt scenarios run on which platforms (AWS/GCP/Azure/ODF/MinIO/FIPS/SNO configs)

**Tech**: Python, Ansible, Jenkins, Kubernetes, storage backends

---

## MTV (Migration Toolkit for Virtualization, 2020–2022)

### MTV Test Automation Framework
Team needed automated E2E testing for VM migration workflows (VMware → OpenShift Virtualization).

**What I did**:
- Built mtv-api-tests framework from scratch (Python, API-driven E2E tests)
-
**Tech**: Python, REST APIs, VMware APIs, Kubernetes APIs

---

## Technical Background

### Languages
- **Go**: Upstream Velero + kubevirt-velero-plugin contributions
- **Python**: Test frameworks (mtv-api-tests, oadp-python-tests, backuplib, claudio-skills)
- **Terraform**: IBM Cloud infrastructure modules
- **Bash**: Automation, CI/CD orchestration, MCP tool development

### Platforms
- **Kubernetes/OpenShift**: OADP operator, Velero, kubevirt, CSI drivers, storage backends
- **RHOAI/ODH**: Cluster provisioning, KServe inference, workbench deployment
- **Cloud**: AWS (mapt, ROSA), IBM Cloud (VPC, databases, secrets management)
- **CI/CD**: Jenkins (including JCasC contributions), GitLab CI, Tekton, GitHub Actions

## Upstream Activity

- **Velero ecosystem**: velero-io/velero, vmware-tanzu/velero-plugin-for-vsphere, kubevirt-velero-plugin
- **mapt**: operator-channel parameter, SNO fixes, instance type filtering
- **konflux-data**: RHAII-on-RHOAI ITS pipeline
- **OADP/MTV**: kubevirt-velero-plugin, openshift-adp-python-wrapper, mtv-api-tests, oadp-apps-deployer
