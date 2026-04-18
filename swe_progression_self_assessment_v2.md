*This self-assessment was generated with [Claude Code](https://claude.com/claude-code), using verified data from parent repos on GitLab CEE, GitLab.com, GitHub, Jira, Slack, Google Docs, Google Sheets, and local performance reviews. I reviewed every claim in this document — trust no code, regardless of source. I'm fairly confident there's at least one mistake left. Hopefully not a big one.*

# Amos Mastbaum — Senior Software Engineer (L4) Self-Assessment

**Target Level:** 4 — Senior Software Engineer
**Current Role:** Senior Software Quality Engineer → Software Engineer (AAET, Nov 2025)
**Red Hat Tenure:** May 2020 – Present (6 years)

---

## 1. Technical Impact
**L4 Requirement:** Leads the design and development of software solutions for features that cross multiple subsystems or components.

* **Upstream Code Contributions (Go) — velero-io/velero:**
  - [**PR #9024** (MERGED)](https://github.com/velero-io/velero/pull/9024): LabelSelector restore fix — PVC and VolumeSnapshot not included during restore. Iterated through [#8795](https://github.com/velero-io/velero/pull/8795), [#8796](https://github.com/velero-io/velero/pull/8796) before accepted. Initially questioned by maintainer; proved viability in OADP fork; upstream adopted.
  - [**Issue #7099**](https://github.com/velero-io/velero/issues/7099) (Nov 2023): Post-restore hooks timing bug — hooks run before DataDownload releases PV. Filed upstream, initially deprioritized.
  - [**Issue #8910**](https://github.com/velero-io/velero/issues/8910) (May 2025): PostHooks multiple exec hooks ignored in HooksAttempts calculation.
  - [**Issue #9182**](https://github.com/velero-io/velero/issues/9182) (Aug 2025): Proposed granular control over Velero annotation hooks.

* **Upstream Code — openshift/velero (downstream carry):**
  - [**PR #379** (MERGED)](https://github.com/openshift/velero/pull/379): Selective PVC restore — moved size patch to backup action, added VolumeSnapshot/VolumeSnapshotContent to CSI additional items. Iterated through [#360](https://github.com/openshift/velero/pull/360), [#378](https://github.com/openshift/velero/pull/378).
  - [**PR #435** (Draft)](https://github.com/openshift/velero/pull/435): Skip annotation hooks during backup (in progress).

* **Upstream Code — kubevirt/kubevirt-velero-plugin:**
  - [**PR #349** (MERGED, in release v0.8.0)](https://github.com/kubevirt/kubevirt-velero-plugin/pull/349): Fixed critical bug in VM resource graph — PVCs silently excluded during restore. 22 lines across 5 files. Iterated from [#328](https://github.com/kubevirt/kubevirt-velero-plugin/pull/328).
  - [#366](https://github.com/kubevirt/kubevirt-velero-plugin/pull/366), [#369](https://github.com/kubevirt/kubevirt-velero-plugin/pull/369): E2E test improvements (closed/draft).

  **Total upstream footprint: 3 merged PRs + 3 issues filed + 7 additional PRs (iterations/drafts) = 13 upstream items across 3 repos.**

* **Framework Creation & Contribution:**
  - `mtv-api-tests` — **Created and led** (216 commits, 62% of repo). Built VM provider API abstraction layers for VMware and RHV. Production standard for successor team. Other contributors: Qin Yuan (29), Maayan Hadasi (30).
  - `oadp-python-tests` — **Founded** (92 commits, ~40% of repo). Top contributor. Shahaf Bahar became 2nd contributor (39 merges). Still the production standard.
  - `openshift-adp-python-wrapper` — **Co-founded** (52 contributions, 32%). 26 merged PRs. Others: sbahar619 (57), mperetzred (41).
  - `oadp-apps-deployer` — 2nd largest contributor (66 commits, ~21% merge share). Prasad Joshi leads (52 merges). Established Ansible/KubeVirt role patterns.
  - `oadp-e2e-qe` — Contributor (85 commits, ~7.6% overall merge share), but **owns two subsystems within the repo:**
    - **`e2e/kubevirt-plugin/`** — Created this test suite (commit `fa294b76`, 325 lines, 3 files). 2 of 3 non-merge commits are Amos's.
    - **Backup library test suite** — 64+ commits (sole contributor to backuplib tests). Built and maintained the entire `backup_lib_test.go` suite across 10+ branches.
    - Note: The older `e2e/kubevirt/` dir was created by mperetz (2022); Amos created the newer `e2e/kubevirt-plugin/` dir (2024) for the plugin-specific test suite.

* **Agentic E2E Smoke Test Pipeline (Delivered):** Built and delivered the agentic E2E smoke test CI pipeline into the team's shared `redhat/ai/midstream-integration/devtools` repo (11 commits, 3rd largest contributor at 11%). Three-tier test framework (minimal/medium/full) covering operators, KServe, vLLM, Kagenti, MCP Gateway, GPU nodes, LlamaStack. GitLab CI with Slack notifications, UBI9 containers. Validated on real cluster: 11 passed, 6 skipped, 1 xfailed. Jira: RHAIENG-3688 (Critical), RHAIENG-3923.

  **Methodology note:** This pipeline was built rapidly using AI-assisted research — agentic exploration across multiple team repos, prompting with proper architectural context, then rigorous human review of every generated artifact. Every line of code was reviewed, understood, and approved before merge. The approach is ~100x faster than manual development, but the human-in-the-loop verification layer is non-negotiable: I question and verify all generated code, and I don't merge what I don't understand. This discipline comes from 30 years of QE mindset — trust no code, regardless of source.

* **ADR: AI-Assisted Code Reviews** — Reviewed and contributed to ADR for AI-assisted code reviews across AAET GitLab repositories (AAET-MI004, authored by Kamesh Akella). Provided input on local CLI tooling and CI workflow patterns. Jira: RHAIENG-2757.

* **Active SWE Transition:** "Movement readiness to Software Engineer" discussed in 1:1 with Klara Bezdekova (Apr 2026). Integration into Model Validation team. Research: GCP to IBM migration, logging consolidation via agentic solutions, GPUaaS working group.

* **First Terraform PR Delivered (Apr 2026):** With no prior Terraform-specific knowledge (but experience with other IaC tools), completed a comprehensive self-onboarding using AI-assisted deep-dive into the `iac-sandbox` Terraform/GCP project. After a short meeting and agentic exploration, produced PR [#59](https://github.com/Jounce-IO/iac-sandbox/pull/59) — adding optional DNS managed zone and Cloud Domains registration to `project-bootstrap/gcp/`. Validated with `terraform plan` against the live GCP project. Corrected starter code from ticket (added missing required blocks identified via provider docs research). Total time: a few hours from zero Terraform knowledge to merged-ready PR.

  **TODO (update after Klara 1:1, ~week of Apr 28 2026):** Update with GCP→IBM migration design discussion outcomes and next SWE task assignment.

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
* **Cross-Team Bug Reporting:** Filed 28+ bugs to CNV developers (Sam Lucidi, Fabien Dupont, Piotr Kliczewski, others) covering VMIO, warm migration, VMware source, storage class, and hot-plug disk issues. 6 documentation bugs filed to Avital Pinnick. 1 OCPBUGS filed (CRC virsh auth).

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
* **MTV Cross-Team Return (Q3 2024):** While fully embedded in OADP, returned to assist the MTV team for approximately a month when they needed help — recognized in Q3 2024 quarterly review as "MTV work (cross-team collaboration)."
* **Legacy Backup Library:** Led the effort to create a library of backups from past releases for 2–3 year customer compliance retention (verified by manager in quarterly review).
* **Upstream Bug Advocacy:** Identified upstream bugs initially deprioritized as edge cases. One resurfaced when Siemens was impacted — validating the original assessment.
* **Release Delivery:** Delivered E2E quality sign-off for 3 major OADP releases.

> *"Amos lead the effort to create a library of backups from past releases... This is quite critical as some businesses have 2-3 year compliance requirements."* — **Wes Hayutin (Q4 2024 review)**

---

## 6. AI / Agentic Engineering
**L4 Requirement:** Evaluates and introduces new AI-driven methodologies that resolve complex issues and improve Engineering efficiency.

**Team-adopted / upstream-contributed work:**

* **cc-rosa-rhoai** ([gitlab.com/redhat/ai/midstream-integration/cc-rosa-rhoai](https://gitlab.com/redhat/ai/midstream-integration/cc-rosa-rhoai)): ROSA HCP cluster lifecycle automation. 7 open MRs for v2.0 release, building on Roland Huß's codebase. [MR !9](https://gitlab.com/redhat/ai/midstream-integration/cc-rosa-rhoai/-/merge_requests/9) (ODH install) is actively used — Summit 2026 clusters are built on main + this MR. Versioned by other team members. Not merged due to no repo owner assigned yet. v2.0 MRs: [!16](https://gitlab.com/redhat/ai/midstream-integration/cc-rosa-rhoai/-/merge_requests/16) (replatform), [!17](https://gitlab.com/redhat/ai/midstream-integration/cc-rosa-rhoai/-/merge_requests/17) (eval gates), [!18](https://gitlab.com/redhat/ai/midstream-integration/cc-rosa-rhoai/-/merge_requests/18) (workbench-deploy ~3900 lines), [!19](https://gitlab.com/redhat/ai/midstream-integration/cc-rosa-rhoai/-/merge_requests/19) (AAET add-ons), [!20](https://gitlab.com/redhat/ai/midstream-integration/cc-rosa-rhoai/-/merge_requests/20) (ODH commands). Sprint demo (Feb 2026): established performance benchmarks.
**Personal POC/experimental (no verified team adoption):**

* **midstream-integration-chatbot**: RAG chatbot built on Llama Stack to "eat our own dog food" — validating Red Hat's AI stack internally. Includes detailed trace exposing RAG and LLM payloads for full transparency. Demoed to team with positive reviews. Manager feedback: "positive feedback on the RAG chatbox" (1:1 with Chris Bynum, Nov 2025). Underwent security review. Not in team production use.
* **test-analyser**: Claude/Vertex AI regression analysis — aimed at reducing manual triage from hours to minutes. Motivation: QE teams spend disproportionate time diagnosing flaky tests; automated classification changes the economics of test maintenance.
* **classifier-eng**: FastAPI log classifier for CI pipelines — automated categorization of failure patterns. Motivation: pattern recognition across thousands of CI runs is something humans do poorly at scale.
* **hybrid-llm**: Local/cloud LLM routing proof-of-concept — demonstrated that a mobile device (Samsung 24FE) can offload specific workloads from cloud providers. Motivation: exploring cost-efficient AI inference for engineers who need AI assistance without enterprise GPU budgets.
* **auto-todo**: Agentic GitHub issue handling — AI agents autonomously read codebase, write code, open PRs, auto-fix on test failure. Motivation: testing the boundaries of fully autonomous development loops with verification gates.
* **dual-llm-chat**, **source-pad**: Multi-model orchestration and source-aware chat experiments exploring how different models complement each other for different task types.

Each project deliberately explored a different facet of AI engineering (local inference, token routing, agentic CI, RAG architectures, autonomous coding). The learnings from each fed directly into the production tools and architectural decisions that followed — this is an engineer's lab notebook, not abandoned code.

**Gap acknowledged:** POC projects need adoption metrics. Team-adopted work (devtools smoke tests, cc-rosa-rhoai) is stronger evidence.

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

## Performance History

**Quarterly performance (manager evaluations):**

| Quarter | Manager | VIC % | Manager Highlight |
|---------|---------|-------|-------------------|
| **Q2 2025** | Wesley Hayutin | **150%** | *"Amos was key this quarter... FIXED BUGS in OADP and in Velero. Spot on performance and I could not ask for anything more."* |
| Q1 2025 | Wesley Hayutin | 100% | Upstream Velero PRs submitted, OADP 1.5 preparation |
| Q4 2024 | Wesley Hayutin | 95% | *"Very nice work... Amos lead the effort to create a library of backups... This is quite critical."* |
| Q3 2024 | Aziza Karol | 90% | MTV cross-team assistance (~1 month). *"Your engagement on Slack channel and providing face-to-face guidance to Solution Architects is awesome."* |
| Q2 2024 | Aziza Karol | 90% | OADP release quality, KubeVirt test coverage |
| Q1 2024 | Aziza Karol | 90% | OADP 1.3.x delivery |
| Q3 2021 | Daniel Gur | **127%** | MTV API framework peak delivery |
| Q2 2021 | Daniel Gur | 110% | MTV framework established |

**Career VIC average: ~97%** (23 quarters). Peaks at **150%** (Q2 2025 — Velero upstream delivery) and **127%** (Q3 2021 — MTV framework peak).

**2025 H2 – 2026 Q1 (80%):** Lower VIC during team transition — split across OADP and AAET simultaneously, self-investing in AI skills on personal time. Manager acknowledged context.

**Annual talent assessments:**

| Period | Manager | What | How | Overall |
|--------|---------|------|-----|---------|
| Q4 2023 | Aziza Karol | Meets Expectations | **Surpasses Expectations** | Successful Performer |
| H2 2024 | Wesley Hayutin | Meets Expectations | Meets Expectations | Successful Performer |

**Career progression:** Software Quality Engineer (2020) → **Senior SQE** (by 2023, ~3 years) → SWE transition in progress (2025–2026). FY2021 goal "Main Automation contributor for MTV API area" — achieved (216 commits, 62% of repo).

**Manager highlights from quarterly reviews:**
- *"Amos lead the effort to create a library of backups from past releases... This is quite critical as some businesses have 2-3 year compliance requirements."* — Wes Hayutin (Q4 2024)
- *"Amos was key this quarter... FIXED BUGS in OADP and in Velero... Spot on performance and I could not ask for anything more."* — Wes Hayutin (Q2 2025, Slack)

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
| `velero-io/velero` | 1 merged PR + 2 closed PRs + 3 issues filed | <0.1% | Bug fix, advocacy, proposals | 5000+ commits in repo |
| `openshift/velero` | 1 merged PR + 3 closed PRs | <0.1% | Carry fix + iterations | — |
| `kubevirt/kubevirt-velero-plugin` | 1 merged PR + 3 closed PRs | ~1% | Bug fix (v0.8.0) + E2E | alromeros, skagan, Lee Yarwood |

**Total verified professional commits: ~550-600 across 12 team/upstream repos (2020-2026)**

| Other Metric | Value | Source |
|-------------|-------|--------|
| GitLab CEE MRs authored | 485 (370 excl. auto-generated) | GitLab API |
| GitHub repos | 47 (17 forks with 0 upstream contributions, 30 personal/POC) | GitHub API |
| `redhat/ai/midstream-integration/devtools` (gitlab.com) | 11 commits (3rd contributor, 11%) | Agentic smoke test pipeline | Kamesh (36), pditmars (12) |
| Upstream items (Velero ecosystem) | 3 merged PRs + 3 issues + 7 iteration PRs = 13 items | GitHub API |
| Upstream merged PRs (all projects) | 22 (across Velero, kubevirt, openshift-python-wrapper, konveyor) | GitHub API |

---

## Self-Assessment vs. L5 Gap Analysis

| Dimension | Current Level | L5 Gap |
|-----------|--------------|--------|
| Technical Impact | L4 | Need to drive architecture across multiple subsystems, not just contribute |
| Software Quality | L4/Emerging L5 | Need to establish practices for large-scale systems across multiple teams |
| Collaboration | L4 | Need to lead community initiatives, not just contribute |
| Mentorship | **L4 met** | L4 requirement satisfied — Shahaf's promotion, cross-team coaching, docs training |
| Business Impact | L4 | Need to drive initiatives across the organization |
| AI/Agentic | Emerging L5 | Need adoption metrics and team-wide process changes |
| SDLC | L4 | Need to drive SDLC evolution across the organization |
| Influence | L4 | Need to build broad consensus for complex strategies |

See companion document: `l5_development_plan.md`

---

> *"Amos is very responsible for his work, eager to help others and comes up with ideas and suggestions to automate and improve things and processes."* — **Shveta Sachdeva**
> *"Looking at you makes others improve themselves as well."* — **Igor Braginsky**

