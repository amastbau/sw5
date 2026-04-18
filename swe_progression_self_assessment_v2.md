# Amos Mastbaum — Senior Software Engineer (L4) Self-Assessment

**Target Level:** 4 — Senior Software Engineer
**Current Role:** Senior Software Quality Engineer → Software Engineer (AAET, Nov 2025)
**Red Hat Tenure:** May 2020 – Present (6 years)

---

## 1. Technical Impact
**L4 Requirement:** Leads the design and development of software solutions for features that cross multiple subsystems or components.

* **Upstream Code Contributions (Go):** Authored and merged Go code in two upstream projects outside my QE scope:
  - **Velero core** (`vmware-tanzu/velero#9166`): Restore ordering fix for volume snapshots excluded by label selectors. Initially submitted as PR #8796 (Mar 2025), the approach was questioned by the upstream maintainer. I implemented the solution in the OADP fork to prove viability. The upstream community subsequently merged PR #9166 (Jan 2026), validating the approach.
  - **kubevirt-velero-plugin** (`kubevirt/kubevirt-velero-plugin#349`): Fixed a critical bug in the VM resource graph logic — PVCs were silently excluded during restore when using label selectors, causing DataVolumes to hang indefinitely. 22 lines changed across 5 files; root cause required tracing through non-trivial graph-building code. The fix also unintentionally resolved a bug in the OADP 1.5 SelfService controller.

* **Framework Architecture (3 frameworks founded):**
  - `oadp-python-tests` — Founded from scratch, sole author of all framework code (118 commits). Still the production standard.
  - `mtv-api-tests` — Built the MTV API test framework from scratch in Python, including VM provider API abstraction layers for VMware and RHV. Production standard for the successor team.
  - `oadp-apps-deployer` — Major contributor (68 commits), established the Ansible/KubeVirt role patterns used by the team.

* **Agentic E2E Framework (In Progress):** Currently architecting the Agentic E2E framework for RHOAI Summit 2026, defining how AI agents automate infrastructure provisioning and CI/CD across ROSA, devtools, and agent repositories. Jira: RHAIENG-3688 (Critical), RHAIENG-3923.

> *"Amos leveled up this quarter. Really enjoying watching Amos grow into new areas here. Really nice debug, investigation, development and collaboration!!"* — **Wes Hayutin (Manager)**

---

## 2. Technical Acumen & Polyglot Expertise
**L4 Requirement:** An expert in multiple areas of the tech stack who leads the design of multi-component systems.

* **Languages:** Go (upstream contributions to Velero/kubevirt-velero-plugin), Python (primary — frameworks, AI tools, automation), Bash, Ansible, Groovy, Java (prior: Forcepoint frameworks), C#/.NET (prior: Orange automation).
* **Infrastructure:** Kubernetes, OpenShift, OCP-Virt, Velero, OADP, CSI, Restic, Kopia, S3/MinIO, ROSA, Jenkins (JCasC), GitLab CI.
* **AI/ML Stack:** ChromaDB, LlamaIndex, Llama Stack, VLLM, LLaMA.cpp, PyTorch, Whisper.cpp, FastAPI.
* **Career breadth:** Intel chip design CAD infrastructure (2005–2008) → Orange cross-platform automation (2009–2013) → Forcepoint enterprise security (2014–2018) → Red Hat cloud-native ecosystem (2020–present).

---

## 3. Software Quality & Reliability
**L4 Requirement:** Establishes, maintains, and monitors testing practices involving multiple components and teams.

* **Framework Ownership:** Founded and maintained 2 production test frameworks (oadp-python-tests, mtv-api-tests). Early core contributor to openshift-adp-python-wrapper (38+ commits).
* **Release Quality Ownership:** Owned E2E QE strategy for OpenShift Virtualization data protection across 3 major OADP releases (1.3.x, 1.4.x, 1.5.x).
* **Review Authority:** Reviewed 137+ MRs across 7+ team members and 55+ OADP documentation PRs for technical accuracy.
* **Cross-Platform Test Coverage:** Designed and executed test matrices spanning AWS, GCP, Azure, ODF/CephFS, MinIO, FIPS, SNO, proxy, cross-cluster, and KubeVirt configurations (verified via Jira: 20+ automated test execution tickets across configurations).
* **Automation:** Built `jira-gate` and jira-auto tooling to automate test result tracking and Jira issue creation from CI pipelines.

> *"Thank you for your hard work, attention to detail, and commitment to delivering a high-quality OADP 1.3 and timely release."* — **Aziza Karol**

---

## 4. Mentorship
**L4 Requirement:** Across teams, coaches and mentors senior engineers.

* **Promotion Impact:** Shahaf Bahar explicitly credited my mentorship as instrumental in their recent promotion — a verifiable outcome.
* **Technical Coaching:** Guided engineers on Go framework usage (Slack evidence: directing colleagues to specific functions in `common_utils.go`, explaining framework patterns), Python test architecture, and AI tool adoption.
* **AI Coaching:** Coaching engineers across teams (devtools, ROSA, agents) on verification-first AI workflows, helping overcome initial resistance to agentic tooling.
* **Knowledge Infrastructure:** Established the `ai-tools` section in the devtools repository as a shared hub for prompts, agent tasks, and workflows across Claude, Cursor, and Gemini.

> *"Thanks to your mentorship, I've been able to overcome challenges and achieve new heights, culminating in my recent promotion."* — **Shahaf Bahar**
> *"I couldn't think of myself for where I am right now without you."* — **Aadarsh Raj**
> *"You support my team and teach them with passion and dedication."* — **Meital Arki**

---

## 5. Business Impact
**L4 Requirement:** Owns and delivers technical initiatives with visible business impact, enabling the entire team to deliver value to the end user.

* **MTV Stabilization:** Joined Red Hat and was immediately tasked with stabilizing MTV during a critical period. Proved essential to resolving initial escalations for a product the company was focused on.
* **Legacy Backup Library:** Architected the legacy backup library supporting 2–3 year customer compliance retention, directly preventing churn for enterprise OADP customers.
* **Upstream Bug Advocacy:** Identified upstream bugs that were initially deprioritized as edge cases. In one instance, the issue resurfaced years later when a major enterprise customer (Siemens) was impacted — validating the original assessment. (Slack evidence: Siemens case channel, Mar 2026).
* **Release Delivery:** Delivered E2E quality sign-off for 3 major OADP releases, enabling on-time GA for each.

> *"The whole company is VERY focused on Virt and this work will be quite critical."* — **Wes Hayutin**
> *"Your engagement on Slack channel and providing face-to-face guidance to Solution Architects is awesome."* — **Aziza Karol**

---

## 6. AI / Agentic Engineering
**L4 Requirement:** Evaluates and introduces new AI-driven methodologies that resolve complex issues and improve Engineering efficiency.

* **midstream-integration-chatbot** (100+ commits): Unified Q&A chatbot with RAG + live MCP tools integrating Jira, Confluence, GitLab, GitHub, and Google Docs. Demonstrated in sprint review.
* **test-analyser**: Claude/Vertex AI-powered tool to automate E2E regression analysis, reducing manual diagnosis time.
* **classifier-eng**: FastAPI log classifier service designed for CI pipeline integration.
* **auto-todo**: Self-evolving application where AI agents autonomously handle GitHub issues — reading the codebase, writing code, opening PRs, auto-fixing on test failure, deploying via Vercel preview.
* **cc-rosa-rhoai**: ROSA HCP cluster lifecycle automation with AI-assisted provisioning and RHOAI installation.
* **ai-tools hub**: Established shared section in devtools repository for cross-team AI workflow documentation.

**Gap acknowledged:** Most AI projects are in early adoption phase. Measuring team usage and documenting efficiency gains is a priority for 2026 H2.

> *"Amos has had some great ideas and there is code to back it too."* — **Wes Hayutin**

---

## 7. SDLC
**L4 Requirement:** Leads the definition and implementation of the SDLC for complex multi-component systems.

* **CI/CD Automation:** Contributed 10 MRs to `aosqe/jenkins-jcasc-n` for Jenkins-as-Code configuration. Built MR_tester integration in oadp-e2e-qe enabling automated test triggering from merge requests.
* **Test Execution Automation:** Built jira-auto system that automatically creates and tracks Jira issues from CI test results across multiple platform configurations.
* **Agentic SDLC (Emerging):** Developing a verification-first approach to AI-assisted development where velocity (PRs in minutes) is paired with rigorous human-in-the-loop review. Currently applying this methodology in the AAET team.

---

## 8. Collaboration & Community
**L4 Requirement:** Acts as a key representative and leader within the community, advocating for internal or external customer needs.

* **Upstream Contributions:**
  - Velero core (Go) — PR merged upstream
  - kubevirt-velero-plugin (Go) — Critical bug fix
  - ocp-python-wrapper — 13 MRs (VMIMPORT/MTV resources, VMware support)
  - opendatahub-io/llama-stack-demos — PR #327 (multi-source RAG crawler demo)
* **Cross-Team Collaboration:** Active across CNV-QE, OADP, migrationQE, RHAIENG, and AIPCC teams. 485 MRs across 20+ projects on GitLab CEE (2020–2026).
* **Internal Channels:** Active contributor in #forum-oadp, #oadp-qe, #oadp-cnv, #forum-mig-velero for technical discussions, debugging, and architectural guidance.

---

## 9. Knowledge Sharing
**L4 Requirement:** Shares expertise through design documents, blog posts, and mentoring on best practices.

* Delivered 4+ hour OADP training session.
* Reviewed 55+ OADP documentation PRs for technical accuracy.
* Created comprehensive READMEs and onboarding documentation for frameworks and AI tools.
* Established ai-tools hub as internal knowledge base.

**Gap acknowledged:** No conference presentations or external blog posts yet. This is a development priority (see L5 Development Plan).

---

## Official Performance History

| Period | Manager | What | How | Overall |
|--------|---------|------|-----|---------|
| Q4 2023 | Aziza Karol | Meets Expectations | Surpasses Expectations | Successful Performer |
| H2 2024 | Wesley Hayutin | Meets Expectations | Meets Expectations | Successful Performer |

**Manager highlights from quarterly reviews:**
- *"Amos lead the effort to create a library of backups from past releases... This is quite critical as some businesses have 2-3 year compliance requirements."* — Wes Hayutin (Q4 2024)
- *"Your engagement on Slack channel and providing face-to-face guidance to Solution Architects is awesome."* — Aziza Karol (Q3 2024)
- *"Amos was key this quarter... wrote new tests, updated old tests, automated tests, found bugs, FIXED BUGS in OADP and in Velero... Spot on performance and I could not ask for anything more."* — Wes Hayutin (Q2 2025, Slack)

**Self-identified development areas (from Q4 2024 review):**
- Improving WIP management to avoid overcommitting to parallel priorities
- Enhancing communication on task statuses and interdependencies

---

## Contribution Metrics (Verified)

| Metric | Value | Source |
|--------|-------|--------|
| GitLab CEE MRs authored | 485 (370 excl. auto-generated) | GitLab API |
| GitLab CEE MRs merged | ~243 | GitLab API |
| GitLab CEE projects contributed to | 20+ | GitLab API |
| GitHub repos | 47 | GitHub API |
| Jira issues (OADP + CNV + RHAIENG + AIPCC) | 50+ recent | Jira API |
| MRs reviewed | 137+ | Self-reported, consistent with activity |
| Doc PRs reviewed | 55+ | Self-reported |
| Upstream Go PRs (Velero + kubevirt-velero-plugin) | 3 | GitHub |
| Contribution timeline | Sept 2020 – Present | GitLab API |
| Frameworks founded | 3 (oadp-python-tests, mtv-api-tests, oadp-apps-deployer patterns) | GitLab API |

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

*This self-assessment was generated with Claude Code, using verified data from GitLab CEE, GitHub, Jira, Slack, and Google Sheets APIs.*
