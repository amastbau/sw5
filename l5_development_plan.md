# L5 (Principal Software Engineer) Development Plan

**Candidate:** Amos Mastbaum
**Starting Level:** Senior Software Engineer (L4)
**Target Level:** Principal Software Engineer (L5)
**Timeline:** 12–18 months (Apr 2026 – Oct 2027)
**Current Team:** Agentic & AI Engineering Tools (AAET), Red Hat AI Engineering

---

## Guiding Principle

The L5 ladder consistently uses: *"across the organization," "large-scale systems," "multiple teams," "drives strategy."* The gap is not capability — it's **demonstrated scope.** Every action in this plan targets expanding impact from team/component level to organizational level.

---

## Dimension 1: Technical Impact

**Current:** L4 — component-level contributions, upstream bug fixes
**Target:** L5 — "Drives the technical strategy and design of software solutions across multiple subsystems, influencing the overall architecture"

### Actions

| # | Action | Measurable Outcome | Target Date |
|---|--------|--------------------|-------------|
| 1.1 | Deliver Agentic E2E framework for Summit 2026 | Framework in production, used by ≥2 teams beyond AAET | Jul 2026 |
| 1.2 | Author an ADR (Architecture Decision Record) for agentic testing strategy that is adopted cross-team | ADR reviewed and approved by ≥2 engineering leads | Sep 2026 |
| 1.3 | Drive a technical design that spans RHOAI + OADP or RHOAI + another subsystem | Design doc with cross-team sign-off, implementation delivered | Dec 2026 |
| 1.4 | Contribute upstream code to a second major project (beyond Velero) | Merged PR in llama-stack, vllm, or equivalent | Mar 2027 |

### Evidence to collect
- Design documents with cross-team reviewers listed
- Slack/email threads showing other teams adopting your architectural decisions
- Git history showing multi-subsystem PRs

---

## Dimension 2: Software Quality & Reliability

**Current:** L4/Emerging L5 — strong within OADP ecosystem
**Target:** L5 — "Establishes, maintains, and monitors testing practices for large-scale systems involving multiple teams"

### Actions

| # | Action | Measurable Outcome | Target Date |
|---|--------|--------------------|-------------|
| 2.1 | Extend the Agentic E2E framework to cover ≥3 RHOAI components (not just AAET) | Framework used for smoke/sanity across model serving, pipelines, and agentic components | Sep 2026 |
| 2.2 | Define and publish a testing strategy document for RHOAI agentic workflows | Document reviewed by QE leads from ≥2 other RHOAI teams | Oct 2026 |
| 2.3 | Establish shared test infrastructure patterns (cluster provisioning, test data, teardown) used by multiple teams | ≥2 teams adopt the patterns without your direct involvement | Jan 2027 |
| 2.4 | Quantify quality improvements: track and report test coverage, regression cycle time, defect escape rate | Dashboard or quarterly report shared with engineering leadership | Ongoing |

### Evidence to collect
- Usage metrics for shared test infrastructure
- Before/after metrics (cycle time, coverage, escape rate)
- Testimonials from other team QE leads

---

## Dimension 3: Collaboration & Community

**Current:** L4 — active upstream contributor
**Target:** L5 — "Drives innovation by leading significant product-area initiatives with a community-first mindset. Participates across multiple communities"

### Actions

| # | Action | Measurable Outcome | Target Date |
|---|--------|--------------------|-------------|
| 3.1 | Become a regular contributor to opendatahub-io or llama-stack upstream | ≥5 merged PRs, recognized in community (reviewer role or mention) | Dec 2026 |
| 3.2 | Lead or co-lead an internal working group (e.g., AI testing practices, agentic CI standards) | Working group charter, ≥3 meetings, published outcomes | Sep 2026 |
| 3.3 | Participate in community health activities: issue triage, PR reviews for external contributors | ≥20 upstream PR reviews in a 6-month period | Mar 2027 |
| 3.4 | Evaluate a new community/technology for potential Red Hat adoption and write a recommendation | Written evaluation shared with engineering leadership | Jun 2027 |

### Evidence to collect
- Upstream contributor profile (commits, reviews, discussions)
- Working group meeting notes and outcomes
- Community evaluation document

---

## Dimension 4: Mentorship

**Current:** L4 — team-level mentoring with promotion outcome
**Target:** L5 — "Across organizations, coaches and mentors principal engineers and role models mentorship for the organization"

### Actions

| # | Action | Measurable Outcome | Target Date |
|---|--------|--------------------|-------------|
| 4.1 | Mentor ≥1 senior engineer from a different team toward their next level | Mentee's manager confirms growth impact | Dec 2026 |
| 4.2 | Create a structured onboarding program for AI/agentic engineering in AAET | Program used by ≥3 new team members | Sep 2026 |
| 4.3 | Run a cross-team workshop on agentic testing or AI-assisted development | ≥15 attendees from ≥3 teams, post-workshop survey | Oct 2026 |
| 4.4 | Document and share mentorship patterns (what worked with Shahaf, Aadarsh) | Internal blog post or knowledge base article | Jul 2026 |

### Evidence to collect
- Mentee feedback (written)
- Workshop attendance and survey results
- Onboarding program usage metrics

---

## Dimension 5: Business Impact

**Current:** L4 — feature/release-level impact
**Target:** L5 — "Owns and drives technical initiatives across the organization recognizing which pieces flow together"

### Actions

| # | Action | Measurable Outcome | Target Date |
|---|--------|--------------------|-------------|
| 5.1 | Quantify cost savings from AI automation (e.g., reduced cluster provisioning time, reduced manual regression hours) | Dollar or hour savings documented and shared with management | Sep 2026 |
| 5.2 | Own a technical initiative that spans ≥2 teams and has a direct line to product quality/velocity | Initiative tracked in Jira as an epic, with cross-team dependencies | Dec 2026 |
| 5.3 | Present business impact of your work in a sprint review or quarterly business review | Presentation delivered to ≥director-level audience | Oct 2026 |
| 5.4 | Identify and propose a cost-optimization opportunity in CI/CD infrastructure | Proposal reviewed by engineering leadership, savings estimated | Mar 2027 |

### Evidence to collect
- Cost/time savings with before/after data
- Jira epic with cross-team issues
- Presentation slides and attendee list

---

## Dimension 6: AI / Agentic Engineering

**Current:** Emerging L5 — prolific building, limited adoption
**Target:** L5 — "Drives the strategy and best practices for integrating advanced AI ecosystems to automate large-scale systems"

### Actions

| # | Action | Measurable Outcome | Target Date |
|---|--------|--------------------|-------------|
| 6.1 | Get ≥1 AI tool (test-analyser, classifier-eng, or chatbot) adopted by another team | Team using it in their CI pipeline or workflow, with usage metrics | Sep 2026 |
| 6.2 | Write a best-practices document for AI-assisted testing in RHOAI | Document reviewed and endorsed by ≥2 engineering leads | Oct 2026 |
| 6.3 | Publish internal metrics: time saved, bugs caught, accuracy of AI classifications | Monthly or quarterly report | Ongoing |
| 6.4 | Drive adoption of agentic workflows (Claude Code, Cursor, etc.) across AAET with measurable productivity impact | ≥50% of team using agentic tools regularly, survey data | Dec 2026 |
| 6.5 | Contribute AI testing patterns upstream (opendatahub-io or equivalent) | Merged PR or accepted RFC | Mar 2027 |

### Evidence to collect
- Usage dashboards for AI tools
- Before/after productivity metrics
- Team survey results on AI tool adoption
- Upstream contributions

---

## Dimension 7: SDLC

**Current:** L4 — team-level process improvements
**Target:** L5 — "Drives the evolution of the SDLC within the organization"

### Actions

| # | Action | Measurable Outcome | Target Date |
|---|--------|--------------------|-------------|
| 7.1 | Formalize the agentic SDLC methodology and get it adopted beyond AAET | Written methodology, adopted by ≥1 additional team | Dec 2026 |
| 7.2 | Introduce a new testing methodology (e.g., AI-generated test cases, property-based testing) to the org | Methodology in use by ≥2 teams | Mar 2027 |
| 7.3 | Lead a retrospective or process improvement initiative that changes how multiple teams work | Documented process change with before/after metrics | Sep 2026 |

### Evidence to collect
- Methodology document with adoption evidence
- Process change documentation
- Team feedback on new practices

---

## Dimension 8: Influence

**Current:** L4 — team/adjacent team influence
**Target:** L5 — "Drives significant technical change within their organization by building broad consensus"

### Actions

| # | Action | Measurable Outcome | Target Date |
|---|--------|--------------------|-------------|
| 8.1 | Present at ≥1 technical conference (DevConf, Red Hat Summit, KubeCon) | Accepted talk, delivered presentation | Jun 2027 |
| 8.2 | Write ≥2 internal or external blog posts on AI-assisted engineering | Published, ≥100 views each | Dec 2026 |
| 8.3 | Lead a technical decision that changes another team's roadmap | Decision documented, team lead confirmation | Mar 2027 |
| 8.4 | Get recognized as a go-to person for AI/agentic engineering beyond your immediate team | ≥3 unsolicited requests for guidance from other teams (tracked) | Ongoing |

### Evidence to collect
- Conference talk recording/slides
- Blog post URLs and view counts
- Slack threads showing cross-team guidance requests
- Decision records showing your influence on other teams

---

## Knowledge Sharing (Cross-Cutting)

**L5 Requirement:** "Presents at technical conferences"

| # | Action | Target Date |
|---|--------|-------------|
| K.1 | Submit a CFP to DevConf.cz 2027 or Red Hat Summit 2027 | CFP deadline (varies) |
| K.2 | Write first blog post: "From SQE to SWE: What Test Engineering Teaches About AI Safety" | Aug 2026 |
| K.3 | Write second blog post: "Agentic E2E Testing at Scale" (after Summit framework delivery) | Oct 2026 |
| K.4 | Deliver a lightning talk at an internal Red Hat engineering all-hands | Dec 2026 |

---

## Quarterly Milestones

### Q2 2026 (Apr–Jun)
- [ ] Deliver Summit 2026 Agentic E2E framework MVP
- [ ] Document mentorship patterns (blog/KB article)
- [ ] Start tracking AI tool usage metrics
- [ ] Submit first CFP

### Q3 2026 (Jul–Sep)
- [ ] Framework adopted by ≥2 teams
- [ ] Cross-team workshop delivered
- [ ] AI best-practices document published
- [ ] First blog post published
- [ ] Cost savings quantified and reported

### Q4 2026 (Oct–Dec)
- [ ] Testing strategy document for RHOAI reviewed by other teams
- [ ] ≥1 AI tool adopted by another team with metrics
- [ ] Second blog post published
- [ ] Agentic SDLC methodology formalized
- [ ] Cross-team technical decision documented

### Q1 2027 (Jan–Mar)
- [ ] Shared test infrastructure patterns adopted by ≥2 teams
- [ ] ≥5 upstream PRs merged (opendatahub-io or equivalent)
- [ ] Conference talk delivered or confirmed
- [ ] L5 self-assessment refresh with evidence

### Q2 2027 (Apr–Jun)
- [ ] Community evaluation document published
- [ ] Cross-org mentoring outcome verified
- [ ] **L5 promotion case assembled with verified evidence**

---

## How to Track Progress

1. **Monthly self-check:** Review this plan, update checkboxes, note blockers
2. **Evidence folder:** Collect screenshots, links, metrics in `/home/amos/git/sw5/l5-evidence/`
3. **Manager alignment:** Share this plan with your manager within 2 weeks. Get buy-in on priorities.
4. **Quarterly refresh:** Update this document every quarter with actual vs. planned progress

---

## Key Principle: Scope Over Activity

Building more tools won't get you to L5. Getting other teams to adopt your tools, follow your designs, and change their processes because of your influence — that's L5. Every action in this plan has a **"used by others"** or **"adopted by X teams"** qualifier for exactly this reason.

---

*Generated with Claude Code. Review and adjust priorities with your manager.*
