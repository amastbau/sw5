# Amos Mastbaum — Senior Software Engineer (L4) Self-Assessment

**Target Level:** 4 — Senior Software Engineer
**Current Role:** Senior Software Quality Engineer → Software Engineer (AAET, Nov 2025)
**Red Hat Tenure:** May 2020 – Present (6 years)

---

## 1. Technical Impact
**L4 Requirement:** Leads the design and development of software solutions for features that cross multiple subsystems or components.

* **Upstream Code Contributions (Go):** Authored and merged Go code in upstream projects outside my QE scope:
  - **Velero core** (`velero-io/velero#9024`): LabelSelector restore fix — 1 merged PR in a repo with 5000+ commits. Initially submitted as PR #8796 (Mar 2025), questioned by upstream maintainer. Implemented in the OADP fork to prove viability. Upstream merged PR #9166 (Jan 2026), validating the approach.
  - **openshift/velero** (`#379`): Downstream carry fix — selective PVC restore with VolumeSnapshot/VolumeSnapshotContent handling.
  - **kubevirt-velero-plugin** (`kubevirt/kubevirt-velero-plugin#349`): Fixed critical bug in VM resource graph logic — PVCs silently excluded during restore with label selectors, causing DataVolumes to hang. 22 lines across 5 files. Included in release v0.8.0.

* **Framework Creation & Contribution:**
  - `mtv-api-tests` — **Created and led** (216 commits, 62% of repo). Built VM provider API abstraction layers for VMware and RHV. Production standard for successor team. Other contributors: Qin Yuan (29), Maayan Hadasi (30).
  - `oadp-python-tests` — **Founded** (92 commits, ~40% of repo). Top contributor. Shahaf Bahar became 2nd contributor (39 merges). Still the production standard.
  - `openshift-adp-python-wrapper` — **Co-founded** (52 contributions, 32%). 26 merged PRs. Others: sbahar619 (57), mperetzred (41).
  - `oadp-apps-deployer` — 2nd largest contributor (66 commits, ~21% merge share). Prasad Joshi leads (52 merges). Established Ansible/KubeVirt role patterns.
  - `oadp-e2e-qe` — Contributor (85 commits, ~7.6% overall merge share), but **owns two subsystems within the repo:**
    - **`e2e/kubevirt-plugin/`** — Created this test suite (commit `fa294b76`, 325 lines, 3 files). 2 of 3 non-merge commits are Amos's.
    - **Backup library test suite** — 64+ commits (sole contributor to backuplib tests). Built and maintained the entire `backup_lib_test.go` suite across 10+ branches.
    - Note: The older `e2e/kubevirt/` dir was created by mperetz (2022); Amos created the newer `e2e/kubevirt-plugin/` dir (2024) for the plugin-specific test suite.

* **Agentic E2E Framework (In Progress):** Architecting the Agentic E2E framework for RHOAI Summit 2026. Jira: RHAIENG-3688 (Critical), RHAIENG-3923.

* **ADR: AI-Assisted Code Reviews** — Reviewed and contributed to ADR for AI-assisted code reviews across AAET GitLab repositories (AAET-MI004, authored by Kamesh Akella). Provided input on local CLI tooling and CI workflow patterns. Jira: RHAIENG-2757.

* **Active SWE Transition:** "Movement readiness to Software Engineer" discussed in 1:1 with Klara Bezdekova (Apr 2026). First SWE task assigned: DNS timezone fix in Terraform. Integration into Model Validation team. Research: GCP to IBM migration, logging consolidation via agentic solutions, GPUaaS working group.

> *"Amos leveled up this quarter. Really enjoying watching Amos grow into new areas here. Really nice debug, investigation, development and collaboration!!"* — **Wes Hayutin (Manager)**

---

## 2. Technical Acumen & Polyglot Expertise
**L4 Requirement:** An expert in multiple areas of the tech stack who leads the design of multi-component systems.

* **Languages:** Go (upstream contributions), Python (primary — frameworks, AI tools), Bash, Ansible, Groovy, Java (prior: Forcepoint), C#/.NET (prior: Orange).
* **Infrastructure:** Kubernetes, OpenShift, OCP-Virt, Velero, OADP, CSI, Restic, Kopia, S3/MinIO, ROSA, Jenkins (JCasC), GitLab CI.
* **AI/ML Stack:** ChromaDB, LlamaIndex, Llama Stack, VLLM, LLaMA.cpp, PyTorch, Whisper.cpp, FastAPI.
* **Career breadth:** Intel chip design CAD (2005–2008) → Orange cross-platform automation (2009–2013) → Forcepoint enterprise security (2014–2018) → Red Hat cloud-native (2020–present).

---

## 3. Software Quality & Reliability
**L4 Requirement:** Establishes, maintains, and monitors testing practices involving multiple components and teams.

* **Framework Ownership:** Created mtv-api-tests (62% of repo), founded oadp-python-tests (40% of repo), co-founded openshift-adp-python-wrapper (32%).
* **Release Quality Ownership:** Owned E2E QE strategy for OpenShift Virtualization data protection across 3 major OADP releases (1.3.x, 1.4.x, 1.5.x).
* **Review Authority:** Reviewed 137+ MRs across 7+ team members and 55+ OADP documentation PRs.
* **Cross-Platform Test Coverage:** Test matrices spanning AWS, GCP, Azure, ODF/CephFS, MinIO, FIPS, SNO, proxy, cross-cluster, and KubeVirt (verified via Jira: 20+ automated test execution tickets).
* **Automation:** Built jira-auto tooling for automated test result tracking from CI pipelines.

> *"Thank you for your hard work, attention to detail, and commitment to delivering a high-quality OADP 1.3 and timely release."* — **Aziza Karol**

---

## 4. Mentorship
**L4 Requirement:** Across teams, coaches and mentors senior engineers.

* **Promotion Impact:** Shahaf Bahar explicitly credited my mentorship as instrumental in their recent promotion.
* **Technical Coaching:** Guided engineers on Go framework usage, Python test architecture, and AI tool adoption (Slack evidence: directing colleagues to specific functions, explaining patterns).
* **Docs Training:** Organized and delivered multi-day OADP training for MMS documentation writers, including homework exercises (`qe-docs-train` repo).
* **AI Coaching:** Coaching engineers across teams (devtools, ROSA, agents) on verification-first AI workflows.

> *"Thanks to your mentorship, I've been able to overcome challenges and achieve new heights, culminating in my recent promotion."* — **Shahaf Bahar**
> *"I couldn't think of myself for where I am right now without you."* — **Aadarsh Raj**
> *"You support my team and teach them with passion and dedication."* — **Meital Arki**

---

## 5. Business Impact
**L4 Requirement:** Owns and delivers technical initiatives with visible business impact, enabling the entire team to deliver value to the end user.

* **MTV Stabilization:** Joined Red Hat and was immediately tasked with stabilizing MTV during a critical period.
* **Legacy Backup Library:** Led the effort to create a library of backups from past releases for 2–3 year customer compliance retention (verified by manager in quarterly review).
* **Upstream Bug Advocacy:** Identified upstream bugs initially deprioritized as edge cases. One resurfaced when Siemens was impacted — validating the original assessment.
* **Release Delivery:** Delivered E2E quality sign-off for 3 major OADP releases.

> *"Amos lead the effort to create a library of backups from past releases... This is quite critical as some businesses have 2-3 year compliance requirements."* — **Wes Hayutin (Q4 2024 review)**

---

## 6. AI / Agentic Engineering
**L4 Requirement:** Evaluates and introduces new AI-driven methodologies that resolve complex issues and improve Engineering efficiency.

**Note:** All AI projects below are personal POC/experimental repos under `amastbau`. None have verified team adoption yet.

* **midstream-integration-chatbot**: RAG chatbot with MCP tools (Jira, Confluence, GitLab, GitHub, Google Docs). Demonstrated in sprint review. Underwent security review.
* **test-analyser**: Claude/Vertex AI regression analysis tool.
* **classifier-eng**: FastAPI log classifier for CI pipelines.
* **auto-todo**: AI agents autonomously handle GitHub issues.
* **cc-rosa-rhoai**: ROSA HCP cluster lifecycle automation (GitLab CEE, internal).
* **ai-tools hub**: Shared section in devtools repository for cross-team AI workflow documentation.

* **cc-rosa-rhoai Sprint Demo** (Feb 2026): Demonstrated ROSA tool in team sprint demo. Session established performance benchmarks (2.5 hours vs 15 min manual). Tool's session summary capability praised for debugging and documentation value.

**Gap acknowledged:** These are POC/experimental projects. Manager gave "positive feedback on the RAG chatbox" (1:1 with Chris Bynum, Nov 2025) but no team adoption metrics yet. Measuring adoption is a priority for 2026 H2.

> *"Amos has had some great ideas and there is code to back it too."* — **Wes Hayutin**

---

## 7. SDLC
**L4 Requirement:** Leads the definition and implementation of the SDLC for complex multi-component systems.

* **CI/CD Automation:** 8 commits to `aosqe/jenkins-jcasc-n` (shared Jenkins infra with 2800+ MRs). Built MR_tester integration in oadp-e2e-qe.
* **Test Execution Automation:** Built jira-auto system for automated Jira issue creation from CI test results.
* **Agentic SDLC (Emerging):** Developing a verification-first approach to AI-assisted development. Currently applying in the AAET team.

---

## 8. Collaboration & Community
**L4 Requirement:** Acts as a key representative and leader within the community, advocating for internal or external customer needs.

* **Upstream Contributions (verified merged):**
  - `velero-io/velero` — 1 merged PR (#9024)
  - `openshift/velero` — 1 merged PR (#379)
  - `kubevirt/kubevirt-velero-plugin` — 1 merged PR (#349), included in release v0.8.0
  - `RedHatQE/openshift-python-wrapper` — 9 merged PRs (MTV resource handlers)
  - `konveyor/tackle-ui-tests` — 4 merged PRs
  - `konveyor/tackle-api-tests` — 3 merged PRs
  - `konveyor/tackle2-hub` — 3 merged PRs
  - `opendatahub-io/llama-stack-demos` — 1 PR open (#327, not yet merged)
* **Cross-Team Collaboration:** Active across CNV-QE, OADP, migrationQE, RHAIENG, AIPCC teams.
* **Internal Channels:** Active contributor in #forum-oadp, #oadp-qe, #oadp-cnv, #forum-mig-velero.

**Note:** 17 of 47 GitHub repos are forks with zero upstream contributions. 30 non-fork repos are personal/POC projects.

---

## 9. Knowledge Sharing
**L4 Requirement:** Shares expertise through design documents, blog posts, and mentoring on best practices.

* Delivered multi-day OADP training for MMS documentation writers (verified via Slack).
* Reviewed 55+ OADP documentation PRs for technical accuracy.
* Created READMEs and onboarding documentation for frameworks and AI tools.

**Gap acknowledged:** No conference presentations or external blog posts yet.

---

## Official Performance History

| Period | Manager | What | How | Overall |
|--------|---------|------|-----|---------|
| Q4 2023 | Aziza Karol | Meets Expectations | Surpasses Expectations | Successful Performer |
| H2 2024 | Wesley Hayutin | Meets Expectations | Meets Expectations | Successful Performer |

**Manager highlights from quarterly reviews:**
- *"Amos lead the effort to create a library of backups from past releases... This is quite critical as some businesses have 2-3 year compliance requirements."* — Wes Hayutin (Q4 2024)
- *"Amos was key this quarter... FIXED BUGS in OADP and in Velero... Spot on performance and I could not ask for anything more."* — Wes Hayutin (Q2 2025, Slack)

**Performance trajectory:**
- Career VIC average ~97%, with peaks at 127% (2021) and 150% (Q2 2025 — Velero upstream delivery)
- 2025 H2 – 2026 Q1: Lower VIC during team transition — split across OADP and AAET simultaneously, self-investing in AI skills on personal time. Manager acknowledged context.

**Self-identified development areas (Q4 2024 review):**
- Improving WIP management to avoid overcommitting to parallel priorities
- Enhancing communication on task statuses and interdependencies

---

## Contribution Metrics (Verified from Parent Repos)

| Repo (Parent) | Amos Commits | % of Repo | Role | Other Top Contributors |
|---------------|-------------|-----------|------|----------------------|
| `mtv-qe/mtv-api-tests` | 216 | 62% | **Creator/leader** | Qin Yuan (29), Maayan Hadasi (30) |
| `app-mig/oadp-python-tests` | 92 | 40% | **Founder, top contributor** | Shahaf Bahar (39 merges), Prasad (16) |
| `oadp-qe/openshift-adp-python-wrapper` | 52 | 32% | **Co-founder** | sbahar619 (57), mperetzred (41) |
| `app-mig/oadp-apps-deployer` | 66 | 21% | 2nd contributor | Prasad Joshi (52 merges) |
| `app-mig/oadp-e2e-qe` | 85 + 64 backuplib | 7.6% overall, **owns kubevirt-plugin + backuplib suites** | Subsystem owner | Prasad (205+), Sachin (99), Shahaf (99) |
| `migrationqe/oadp-qe-automation` | 37 | 5% | Contributor | Tareq Alayan (97), Md Nadeem |
| `migrationqe/migrationqe-automation` | 28 | 2% | Contributor | M Sajid Mansoori, Tareq, Nadeem |
| `RedHatQE/openshift-python-wrapper` | 9 PRs | 2% | Minor contributor | myakove (1247), rnetser (358) |
| `velero-io/velero` | 1 PR | <0.1% | Bug fix | 5000+ commits in repo |
| `kubevirt/kubevirt-velero-plugin` | 1 PR | ~1% | Bug fix | alromeros, skagan, Lee Yarwood |

**Total verified professional commits: ~550-600 across 12 team/upstream repos (2020-2026)**

| Other Metric | Value | Source |
|-------------|-------|--------|
| GitLab CEE MRs authored | 485 (370 excl. auto-generated) | GitLab API |
| GitHub repos | 47 (17 forks with 0 upstream contributions, 30 personal/POC) | GitHub API |
| Upstream merged PRs | 22 (across Velero, kubevirt, openshift-python-wrapper, konveyor) | GitHub API |

---

## Self-Assessment vs. L5 Gap Analysis

| Dimension | Current Level | L5 Gap |
|-----------|--------------|--------|
| Technical Impact | L4 | Need to drive architecture across multiple subsystems, not just contribute |
| Software Quality | L4/Emerging L5 | Need to establish practices for large-scale systems across multiple teams |
| Collaboration | L4 | Need to lead community initiatives, not just contribute |
| Mentorship | L4 | Need to mentor principal engineers, role-model mentorship at org level |
| Business Impact | L4 | Need to drive initiatives across the organization |
| AI/Agentic | Emerging L5 | Need adoption metrics and team-wide process changes |
| SDLC | L4 | Need to drive SDLC evolution across the organization |
| Influence | L4 | Need to build broad consensus for complex strategies |

See companion document: `l5_development_plan.md`

---

> *"Amos is very responsible for his work, eager to help others and comes up with ideas and suggestions to automate and improve things and processes."* — **Shveta Sachdeva**
> *"Looking at you makes others improve themselves as well."* — **Igor Braginsky**

*This self-assessment was generated with Claude Code, using verified data from parent repos on GitLab CEE, GitHub, Jira, Slack, and Google Sheets APIs.*
