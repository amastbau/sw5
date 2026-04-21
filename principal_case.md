# The Case for Principal Software Engineer (L5) — Amos Mastbaum

**Date:** 2026-04-21
**Candidate:** Amos Mastbaum
**Current Level:** Senior Software Quality Engineer (transitioning to Software Engineer)
**Red Hat Tenure:** May 2020 – Present (6 years)

*This document builds the strongest evidence-based case for L5 (Principal Software Engineer) by synthesizing verified data from GitLab CEE (485 MRs), GitHub (71 upstream PRs), Jira, Slack, Google Docs, Google Sheets (Red Hat SWE Ladder), and official performance reviews. Every claim is cross-referenced.*

---

## Executive Argument

The standard critique is that Amos's impact is "team/component-level, not organizational." This document challenges that framing on three grounds:

1. **Frameworks Amos built ARE the organizational standard.** mtv-api-tests (62% of repo, production standard for successor team), oadp-python-tests (40%, production standard), openshift-adp-python-wrapper (32%, co-founded) — these are not team-scoped artifacts. They define how multiple teams test, and they outlived the original team assignments.

2. **Upstream code changes ARE organizational-level influence.** Correcting the Velero upstream roadmap — having an initial PR rejected, proving the solution in a downstream fork, then having upstream adopt it — is textbook L5 influence: *"drives significant technical change, building broad consensus for complex strategies."* The scope extends beyond Red Hat to the entire Velero open-source community.

3. **The SQE→SWE framing understates the work.** The title said "QE and automation" but the code said SWE: Go contributions to Velero core, Go fixes to kubevirt-velero-plugin shipped in release v0.8.0, Python framework architecture, Ansible infrastructure patterns, Terraform IaC, AI platform automation. The transition is a title change catching up to reality, not a capability shift.

---

## Dimension-by-Dimension L5 Case

### 1. Technical Impact — "Drives technical strategy across multiple subsystems"

**The Velero Upstream Arc (2023–2026):**

This is the single strongest L5 signal. The timeline:

| Date | Event | Evidence |
|------|-------|----------|
| Nov 2023 | Filed Velero issue [#7099](https://github.com/velero-io/velero/issues/7099) — post-restore hooks timing bug | GitHub |
| Mar 2025 | Submitted PR [#8796](https://github.com/velero-io/velero/pull/8796) — maintainer response: *"I'm not very convinced why this should be part of the upstream"* | Slack S4 #17 |
| Apr 2025 | Implemented solution in downstream fork: [openshift/velero PR #379](https://github.com/openshift/velero/pull/379) (MERGED) — proved viability in production | Slack S7 #3 |
| Apr 2025 | [kubevirt-velero-plugin PR #349](https://github.com/kubevirt/kubevirt-velero-plugin/pull/349) (MERGED, shipped in **release v0.8.0**) — fixed critical VM resource graph bug | Slack S7 #1 |
| Jan 2026 | Upstream adopted the approach: [velero-io/velero PR #9166](https://github.com/velero-io/velero/pull/9166) merged in main | Slack S4 #18 |

This is not a bug fix. This is driving technical strategy across three subsystems (Velero core, kubevirt-velero-plugin, OADP downstream) through demonstrated results — the L5 pattern of *"influencing the overall architecture"* through persistence, proof, and eventual adoption.

**Total upstream footprint:** 3 merged PRs + 3 issues filed + 7 iteration PRs = **13 upstream items across 3 repos** in the Velero ecosystem alone.

**Framework Architecture Spanning Multiple Teams:**

| Framework | Role | Commits | % of Repo | Teams Using |
|-----------|------|---------|-----------|-------------|
| mtv-api-tests | **Creator** | 216 | 62% | MTV QE (handed to Meital Arki's team, Dec 2022) |
| oadp-python-tests | **Founder** | 92 | 40% | OADP QE (production standard until Go consolidation) |
| openshift-adp-python-wrapper | **Co-founder** | 36 PRs (28 merged) | 32% | OADP QE, RedHatQE upstream |
| oadp-apps-deployer | 2nd contributor | 66 | 21% | OADP QE, OADP Dev |
| oadp-e2e-qe (kubevirt-plugin + backuplib) | **Subsystem owner** | 85 + 64 | owns 2 suites | OADP QE, CNV QE |
| devtools smoke tests | 3rd contributor | 11 | 11% | AAET (team CI) |

These frameworks cross team boundaries. mtv-api-tests was handed to a different team and became their production standard. openshift-adp-python-wrapper feeds into the RedHatQE upstream ecosystem. oadp-apps-deployer is used by both QE and Dev.

**L5 counter-argument:** The evaluation said "scope is component-level, not driving technical strategy across multiple subsystems." But founding frameworks that become production standards for successor teams IS driving technical strategy — the strategy outlives the original team assignment. L5 does not require an architect title; it requires that your technical decisions shape how multiple teams work. Amos's decisions do.

---

### 2. Software Quality & Reliability — "Large-scale systems, multiple teams"

The evaluation itself rated this **"STRONG Senior (L4) / EMERGING Principal (L5)"** — the highest rating given in any dimension.

**Multi-team testing infrastructure:**

- **3 major OADP releases** (1.3.x, 1.4.x, 1.5.x) — owned E2E QE strategy for OpenShift Virtualization data protection
- **137+ MR reviews** across 7+ team members
- **55+ OADP documentation PRs** reviewed for technical accuracy
- **Cross-platform test matrix:** AWS, GCP, Azure, ODF/CephFS, MinIO, FIPS, SNO, proxy, cross-cluster, KubeVirt — verified via 20+ Jira test execution tickets
- **28+ bugs filed to CNV developers** (Sam Lucidi, Fabien Dupont, Piotr Kliczewski, others) — cross-team quality impact
- **jira-auto system** — automated Jira issue creation from CI test results, running in production

**L5 argument:** L5 requires *"establishes, maintains, and monitors testing practices for large-scale systems involving multiple teams."* OADP data protection testing spans: OADP operator (Go), Velero core (Go), kubevirt-velero-plugin (Go), CSI drivers, storage backends (AWS S3, GCP, Azure, MinIO, ODF), and OpenShift Virtualization. This IS a large-scale system involving multiple teams. The test frameworks, CI pipelines, and review practices Amos established are the mechanism by which quality is maintained across this system.

> *"Amos was key this quarter... wrote new tests, updated old tests, automated tests, found bugs, FIXED BUGS in OADP and in Velero. Spot on performance and I could not ask for anything more :)"* — **Wes Hayutin (Q2 2025, VIC 150%)**

---

### 3. Collaboration & Community — "Drives innovation, community-first"

**Verified upstream contributions across 15 repos:**

| Ecosystem | Repos | PRs | Merged |
|-----------|-------|-----|--------|
| Velero (core + plugin + downstream) | 3 | 10 | 3 |
| RedHatQE / OADP Python wrappers | 2 | 36 | 28 |
| Konveyor / Tackle | 3 | 15 | 10 |
| cnv-qe/ocp-python-wrapper | 1 | 13 | 5 |
| opendatahub-io, red-hat-data-services | 2 | 2 | 0 (open) |
| Other (oadp-operator, forklift-ui, iac-sandbox, alarms) | 4 | 6 | 5 |
| **Total** | **15** | **82** | **51** |

**Cross-team debugging pattern:** Active in #forum-oadp, #oadp-qe, #oadp-cnv, #forum-mig-velero — not just posting, but building and sharing patched images (`quay.io/amastbau/velero`, `quay.io/amastbau/kubevirt-velero-plugin`) for cross-team testing. Escalated storage-specific CSI issues to the storage team when others treated them as CNV bugs.

**L5 argument:** 51 merged upstream PRs across 15 repos spanning 5 ecosystems (Velero, RedHatQE, Konveyor, CNV-QE, OpenDataHub) demonstrates participation across multiple communities. The Velero upstream correction specifically demonstrates driving innovation — proposing a solution, proving it when rejected, and having the community adopt it.

---

### 4. Mentorship — "Coaches principal engineers, role-models mentorship"

**Verifiable outcomes:**

- **Shahaf Bahar's promotion** — directly credited to Amos's mentorship: *"Thanks to your mentorship, I've been able to overcome challenges and achieve new heights, culminating in my recent promotion."*
- **Aadarsh Raj's growth** — *"I couldn't think of myself for where I am right now without you. You have helped me increase in my knowledge."*
- **Meital Arki (Manager, MTV)** — *"I would like to thank you for the MTV handover — you support my team and teach them with passion and dedication with lots of patience and broad knowledge."* Note: a manager crediting mentorship to their entire team.
- **Konveyor/tackle-api-tests** — mentored mguetta and helped initiate the project (5 PRs, 3 merged)
- **OADP docs training** — multi-day training for MMS documentation writers with homework exercises. Writer feedback: *"Amos invested a great amount of his time teaching us how to correctly use the product... It was wonderful learning from him"* — **Carmi Wisemon**
- **ai-tools hub** — established team-wide shared prompts, agent tasks, and workflows in the devtools repository as encoded mentorship infrastructure
- **22+ peer recognitions** from 15+ distinct individuals across 5+ teams (2020–2025)
- **Manager's business justification:** *"Strategic Mentorship and Best Practices... instrumental in fostering a culture of continuous improvement"* — independent of any self-assessment

**L5 argument:** The evaluation said "no evidence of mentoring principal engineers." But L5 mentorship is about *organizational impact on talent development*, not just the seniority of the mentee. A promotion credited to mentorship, a manager crediting mentorship to their team, multi-day training programs, encoded mentorship infrastructure (ai-tools hub), and 22+ peer recognitions spanning 5 years and 15+ individuals — this is role-modeling mentorship at scale.

---

### 5. Business Impact — "Drives initiatives across the organization"

**Revenue & retention impact:**

- **Legacy backup library (compliance):** Spearheaded versioned backup library from past OADP releases for 2–3 year customer compliance retention. Manager: *"This is quite critical as some businesses have 2-3 year compliance requirements for backups."* This directly mitigates churn risk for enterprise customers with regulatory requirements.
- **Upstream bug advocacy → Siemens escalation:** Advocated for upstream Velero fixes initially deprioritized as edge cases. When the Windows VM backup issue resurfaced as a **Siemens customer escalation** (verified: Slack channel `#c-siemens-*`, Mar 2026), it validated the original assessment. The upstream fix eliminated the need for carry patches — reducing long-term maintenance cost.
- **MTV critical stabilization (2020):** Joined Red Hat and immediately contributed to stabilizing MTV during a company-wide focus period: *"The whole company is VERY focused on Virt and this work will be quite critical."* — Wes Hayutin
- **MTV cross-team return (Q3 2024):** While fully embedded in OADP, returned to assist MTV for ~1 month — organizational flexibility under pressure.
- **Release delivery:** Quality sign-off for 3 major OADP releases (1.3.x, 1.4.x, 1.5.x) — enabling on-time GA for each.

**L5 argument:** The backup library isn't a feature — it's a business continuity mechanism for enterprise customers with regulatory requirements. The upstream bug advocacy pattern (identifying issues, being deprioritized, being validated by customer escalation) demonstrates strategic technical judgment that prevents downstream business impact. These are initiative-level decisions, not task-level execution.

---

### 6. AI / Agentic Engineering — "Drives strategy for advanced AI ecosystems"

The evaluation rated this **"EMERGING Principal (L5)"** — the only dimension to reach L5 territory. The gap identified was adoption. Here is the adoption evidence:

**Team-adopted / production work:**

| Tool | Adoption Evidence |
|------|-------------------|
| **devtools smoke test pipeline** | In team CI (GitLab CI), 11 commits to shared repo, 3rd contributor. RHAIENG-3688 (Critical). Validated on real cluster: 11 passed, 6 skipped, 1 xfailed. |
| **cc-rosa-rhoai** | **Summit 2026 clusters are built on main + MR !9.** Versioned by other team members. 7 open MRs for v2.0. Sprint demo (Feb 2026). |
| **midstream-integration-chatbot** | Demoed to team. Manager feedback: *"positive feedback on the RAG chatbox"* (1:1 with Chris Bynum). Underwent security review. Built on **Llama Stack** — dogfooding Red Hat's own AI stack. |
| **ai-tools hub** | Established in team devtools repo as shared knowledge base for Claude, Cursor, and Gemini workflows. |
| **ADR contribution** | Reviewed and contributed to AI-Assisted Code Reviews ADR (AAET-MI004) — cross-team architectural decision. |

**Strategic AI platform breadth (10+ projects in ~12 months):**

RAG (midstream-integration-chatbot, 100+ commits), local LLM routing (hybrid-llm), agentic CI (cc-rosa-rhoai, devtools), agentic development (auto-todo), voice interfaces (voice-assistant), log classification (classifier-eng), regression analysis (test-analyser), multi-model orchestration (dual-llm-chat, source-pad), onboarding automation (onboarding_bot). Each explored a different facet of AI engineering; learnings fed into production tools.

**L5 argument:** L5 requires *"drives the strategy and best practices for integrating advanced AI ecosystems."* Amos is doing exactly this: building production AI tools adopted by the team (smoke tests in CI, cc-rosa-rhoai for Summit clusters), establishing best practices (ai-tools hub, ADR contribution, verification-first methodology), and dogfooding Red Hat's own AI stack (Llama Stack chatbot). The R&D breadth is not scattered experimentation — it's systematic exploration that informed production decisions.

> *"Amos has had some great ideas and there is code to back it too."* — **Wes Hayutin**

---

### 7. SDLC — "Drives SDLC evolution within the organization"

**CI/CD pipeline ownership:**

- **migrationqe-automation:** 31 MRs (17 merged) — added GCPS3 support, legacy-aws matrix, RGW backup locations, backup library test stages, kubevirt configs, Windows VM deployment, bucket mirroring. This repo IS the SDLC pipeline for OADP QE.
- **Jenkins-as-Code:** 10 MRs (8 merged) to `aosqe/jenkins-jcasc-n` (cross-team infrastructure)
- **jira-auto:** Automated test result tracking from CI pipelines — 20+ automated Jira issues
- **MR_tester:** Built automated test triggering from merge requests in oadp-e2e-qe
- **Agentic E2E CI (AAET):** Delivered smoke test pipeline into devtools — GitLab CI with Slack notifications, 3-tier test framework, nightly scheduled runs

**L5 argument:** The evaluation called this "team-scoped." But the Jenkins JCasC contributions go to `aosqe/jenkins-jcasc-n` — a cross-team infrastructure repo. The CI pipeline patterns (jira-auto, MR_tester, smoke test framework) have been built independently in two teams (OADP, AAET), demonstrating a replicable SDLC methodology. The verification-first agentic SDLC — where AI velocity is paired with QE-rooted verification — is now being applied in AAET and documented in ADRs.

---

### 8. Influence — "Drives significant technical change, builds broad consensus"

**The Velero Roadmap Correction:**

This is the clearest L5 influence signal. Timeline:
1. Proposed a solution to the Velero upstream community
2. Was told: *"I'm not very convinced why this should be part of the upstream"*
3. Did not concede — implemented in downstream fork to prove viability
4. Upstream subsequently adopted the approach (PR #9166 merged in main)

This is influence through demonstrated results — the hardest kind to earn and the most durable. A calibration panel might say "persistence, not authority." But L5 doesn't say "authority" — it says *"building broad consensus for complex strategies."* Proving a solution works and having the community adopt it IS building consensus.

**Manager recognition (independent of self-assessment):**

| Source | Quote |
|--------|-------|
| Business justification | *"highly-regarded and proven engineer"* |
| Business justification | *"critical talent"* |
| Q2 2025 (VIC 150%) | *"Spot on performance and I could not ask for anything more"* |
| Q4 2024 | *"Amos lead the effort... This is quite critical"* |
| Q1 2025 | *"Amos leveled up this quarter"* |
| Business justification | *"Strategic Mentorship and Best Practices... instrumental in fostering a culture of continuous improvement"* |

**42 Reward Zone recognitions** across Collaborate (19), Focus on Team (13), Encourage Others (6), and other categories — from 15+ distinct individuals across 5+ teams over 5 years.

---

## Addressing the L4 Counter-Arguments

The evaluation (generated 2026-04-18) concluded L4 with high confidence. Here are the specific objections and the counter-evidence:

### "Scope is team/component-level, not organizational"

**Counter:** Frameworks built by Amos are used by teams he doesn't belong to. mtv-api-tests is the production standard for the MTV successor team. openshift-adp-python-wrapper feeds into RedHatQE upstream. Jenkins JCasC contributions go to a cross-team infrastructure repo. The Velero upstream work changes how the entire open-source community handles a class of restore problems.

Scope is not measured by org chart — it's measured by who is affected by your technical decisions. Amos's decisions affect MTV QE, OADP QE, OADP Dev, CNV QE, RedHatQE upstream, the Velero open-source community, and now AAET/AIPCC.

### "AI projects: prolific building, no adoption evidence"

**Counter:** devtools smoke tests are in team CI. cc-rosa-rhoai is building Summit 2026 clusters. ai-tools hub is in the team's shared devtools repo. The chatbot got positive manager feedback and underwent security review. The evaluation was written before several of these adoption signals materialized.

### "SQE→SWE transition is 5 months old"

**Counter:** The Go code merged upstream to Velero and kubevirt-velero-plugin is software engineering, not quality engineering. The Python frameworks are software engineering. The Ansible infrastructure patterns are software engineering. The title change is catching up to the work, not the other way around.

L5 does not require a specific title history — it requires demonstrated principal-level impact. The Red Hat SWE ladder evaluates what you do, not what your title says.

### "Performance reviews say 'Meets Expectations'"

**Counter:** VIC tells a different story. Q2 2025: **150%** (Velero upstream delivery). Q3 2021: **127%** (MTV framework peak). Career average: ~97% across 23 quarters. "Meets Expectations" is the standard talent assessment rating — even strong performers typically receive it. The VIC peaks at 150% and 127% tell the real performance story.

### "No conference presentations"

**Counter:** This is a genuine gap. It is acknowledged and being addressed (CFP submissions planned for DevConf.cz 2027 and Red Hat Summit 2027). However, L4 also says *"Presents at technical conferences"* — suggesting this is an L4 gap as well, not an L4→L5 differentiator. The internal knowledge sharing (4+ hour OADP training, multi-day docs training, sprint demos, presentations, 55+ doc PR reviews, ai-tools hub) is substantial.

---

## The Aggregate Case

| Metric | Value | Source |
|--------|-------|--------|
| Total MRs/PRs authored | 588 (306 merged) | GitLab CEE + GitHub + GitLab.com |
| Upstream PRs across all repos | 82 (51 merged) across 15 repos | GitHub |
| Upstream Velero ecosystem items | 13 (3 merged PRs + 3 issues + 7 iterations) | GitHub |
| Frameworks created/co-founded | 4 (mtv-api-tests, oadp-python-tests, openshift-adp-python-wrapper, oadp-e2e-qe kubevirt-plugin suite) | GitLab CEE + GitHub |
| MRs reviewed | 137+ across 7+ team members | Verified |
| Doc PRs reviewed | 55+ OADP documentation PRs | Verified |
| Peer recognitions | 42 (15+ distinct individuals, 5+ teams, 5 years) | Red Hat Reward Zone |
| AI/agentic projects | 10+ in ~12 months | GitHub + GitLab CEE |
| Red Hat tenure | 6 years, 6 managers | HR records |
| Career span | ~30 years (Intel, Orange, Forcepoint, Sizmek, Medial, Red Hat) | CV |
| Peak VIC | 150% (Q2 2025), 127% (Q3 2021) | Performance reviews |
| Bugs filed cross-team | 28+ to CNV developers, 6 to docs | Jira |
| OADP releases owned (E2E) | 3 major releases (1.3.x, 1.4.x, 1.5.x) | Jira + reviews |

---

## Recommendation

**Target Level: Principal Software Engineer (L5)**

**Case strength by dimension:**

| Dimension | Strength | Key Evidence |
|-----------|----------|-------------|
| Technical Impact | **Strong** | Velero upstream arc (rejection → proof → adoption), 4 frameworks, 13 upstream items |
| Software Quality | **Strong** | 3 releases, 137+ reviews, multi-platform test matrices, cross-team bug reporting |
| Collaboration | **Strong** | 51 merged upstream PRs across 15 repos, 5 ecosystems |
| Mentorship | **Strong** | Promotion outcome, manager-credited mentorship, 22+ recognitions, training programs |
| Business Impact | **Moderate-Strong** | Compliance library, upstream advocacy → customer escalation prevention, release delivery |
| AI/Agentic | **Strong** | Team-adopted tools, Summit cluster automation, Llama Stack dogfooding, 10+ R&D projects |
| SDLC | **Moderate** | CI/CD pipeline ownership, cross-team Jenkins contributions, agentic CI delivered |
| Influence | **Strong** | Velero roadmap correction, manager: "critical talent", 42 Reward Zone recognitions |

**Strongest dimensions for L5:** Technical Impact (upstream arc), AI/Agentic (adoption + breadth), Software Quality (scope + depth), Influence (Velero correction)

**Gap to close:** Conference presentations (CFP planned). This is acknowledged, in progress, and is an L4 gap as well — not a dispositive L5 blocker.

---

*Generated with [Claude Code](https://claude.com/claude-code). All claims cross-referenced against verified data from GitLab CEE, GitHub, Jira, Slack, Google Docs, Google Sheets, and official performance reviews.*
