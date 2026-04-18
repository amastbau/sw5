# SQE → SWE Transition Evaluation Plan

**Candidate:** Amos Mastbaum
**Evaluator Persona:** Director of AI Engineering, Red Hat
**Target:** Principal Software Engineer (IC5) — stress-test against Senior (L4) baseline
**Date:** 2026-04-18

---

## Phase 1 — Data Collection (parallel)

| # | Source | What to Extract | Tool | Status |
|---|--------|----------------|------|--------|
| 1a | Local: `swe_progression_self_assessment.md` | Full self-assessment — all claims, evidence, quotes | Read | ☐ |
| 1b | Local: `~/Downloads/amos_mastbaum_cv.md` | Career history, roles, timelines, skill claims | Read | ☐ |
| 1c | Google Spreadsheet | Red Hat SWE ladder criteria (L3–L5) | google-docs-mcp | ☐ |
| 1d | GitHub (`amastbau`) | 30 repos — commit counts, PR activity, contribution patterns, languages | gh CLI | ☐ |
| 1e | GitLab (Red Hat internal) | Projects, MRs authored, upstream contributions (OADP, Velero, KubeVirt) | gitlab MCP | ☐ |
| 1f | Jira | Issues assigned/reported — scope, impact, cross-team signals | mcp-atlassian | ☐ |
| 1g | Slack | Relevant threads — mentoring, cross-team collaboration, recognition | hrungnir MCP | ☐ |

### Data Collection Rules

- Query live data; do not build intermediate indexes
- Capture quantitative metrics where possible (commit counts, PR merge rates, Jira throughput)
- Note discrepancies between self-assessment claims and actual data
- Flag anything that cannot be verified

---

## Phase 2 — Evidence Mapping

For each of the 8 evaluation dimensions, extract and classify concrete evidence:

| # | Dimension | What Counts | Sources |
|---|-----------|-------------|---------|
| 2.1 | Technical Impact | Architecture decisions, multi-subsystem scope, upstream adoption | GitLab, GitHub, self-assessment |
| 2.2 | Software Quality & Reliability | Frameworks built and in use, testing practices, CI/CD ownership | GitHub, GitLab, Jira |
| 2.3 | Collaboration & Community | Upstream PRs/MRs, cross-team work, community leadership | GitLab, GitHub, Slack |
| 2.4 | Mentorship | Evidence of teaching, onboarding, leveling up others | Slack, Jira, self-assessment |
| 2.5 | Business Impact | Feature-level vs initiative-level outcomes, customer impact | Jira, self-assessment |
| 2.6 | AI / Agentic Engineering | Real adoption vs personal experiments, team enablement | GitHub, self-assessment |
| 2.7 | SDLC Influence | Process improvements, cross-team standards | Jira, GitLab, Slack |
| 2.8 | Influence | Roadmap/strategy impact, decision-making scope | Slack, Jira, self-assessment |

### Evidence Classification

Each piece of evidence rated as:
- **BELOW Senior** — not at L4 level
- **SOLID Senior (L4)** — meets Senior expectations
- **EMERGING Principal (L5)** — shows L5 signals but incomplete
- **STRONG Principal (L5)** — clear L5 evidence

### Cross-Reference Rules

- Self-assessment claims must be backed by at least one external source (repo, Jira, Slack)
- Unverified claims marked as WEAK
- Philosophical statements and narratives ignored unless tied to measurable impact
- Experimental/unused projects downweighted

---

## Phase 3 — Director-Level Evaluation

### 3.1 Structured Output

1. **Executive Summary** (3–5 sentences, hiring-decision tone)
2. **Level Assessment Table** (per dimension, L4/L5 classification with justification)
3. **Top 5 Strongest Signals** (promotion-worthy evidence)
4. **Top 5 Risks / Weak Signals** (gaps, overstatements, unverified claims)
5. **Recommendation**
   - Target Level: Senior (L4) or Principal (L5)
   - Confidence: High / Medium / Low
6. **Required Document Improvements**
   - What to REMOVE (overstatements, narratives without impact)
   - What to REWRITE (vague claims → concrete evidence)
   - What to ADD (missing evidence that exists in data but not in document)

### 3.2 Evaluation Principles

- Skeptical but fair — like defending this case in a calibration meeting
- 30 years experience is context, not a credential — impact is what counts
- SQE→SWE transition is a strength if positioned correctly (test-first mindset, production awareness)
- Age (50) is irrelevant to the evaluation — only evidence and impact matter
- AI/agentic work evaluated on adoption and team impact, not personal enthusiasm
- Every claim in the self-assessment will be stress-tested against live data

---

## Deliverable

Final evaluation written to: `evaluation.md`
Updated self-assessment (if requested): `swe_progression_self_assessment_v2.md`
