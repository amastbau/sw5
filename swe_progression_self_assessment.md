*Note: This self-assessment was itself created using a Claude Code terminal connected to all relevant Git repositories, Google Sheets, GitLab, and GitHub — with every PR/MR reference programmatically verified against actual commit history. This artifact is a living demonstration of the agentic methodology described within it.*

# Amos Mastbaum — Principal Software Engineer (IC5) Self-Assessment

**Target Level:** 5 — Principal Software Engineer  
**Core Philosophy:** My primary programming language is **English**. By architecting agentic workflows and human-in-the-loop verification systems, I have compressed the SDLC to a point where my primary interface is a Claude Code terminal — I architect, review, and ship from any device because the engineering happens through strategic direction, not manual coding at a workstation.

I believe my deep roots in production systems, support, and testing made me a better software developer. Especially now, at the dawn of agentic software development. I am trained to trust **no code** — not agent-generated, not human-written. This test-oriented mindset is not just a "nice to have" anymore; **human-in-the-loop is essential for successful AI implementations.** I bring extended knowledge that spans from old-school manual testing through full automation pyramids to state-of-the-art AI-enhanced SDLC — and I wear every hat in the process: user, product owner, developer, QE. That breadth is rare, and it is precisely what a Principal Software Engineer needs to set technical direction that actually works in production.

I wrote my first program in BASIC on a Dragon 32 when I was nine years old, and I knew then that this is what I wanted to do with my life. That has never changed. When I joined Red Hat, I immediately felt I had found my professional home — a company whose values I genuinely share. The evidence is in the trajectory: in six years, I have made a quantum leap. In my six years at Red Hat, I have had six excellent managers, and taking the advice of my first Red Hat manager, Daniel Gur, I learned something meaningful from every single one of them.

---

## 1. Technical Impact: Architecture & Strategy
**L5 Requirement:** Drives the technical strategy and design of software solutions across multiple subsystems.

* **Strategic Upstream Advocacy & Course Correction (Velero):** I led a significant research effort within the Velero upstream community. When my proposal for data protection gaps was initially rejected in favor of a different architectural direction, I did not concede. I implemented the solution within the OADP fork to prove its viability. Months later, the upstream community admitted my solution was the correct path and adopted it. This persistence changed the roadmap for `velero-io/velero#9024`, `openshift/velero#379`, and `kubevirt/kubevirt-velero-plugin#349`.
* **Critical Bug Discovery & Fix (kubevirt-velero-plugin):** I identified a critical bug in the VM resource graph logic during restore — PVCs were silently excluded when using label selectors, causing DataVolumes to hang indefinitely. I authored and submitted the PR (`kubevirt/kubevirt-velero-plugin#349`) that fixed the issue, working in collaboration with the CNV development team. The fix was small (22 lines changed across 5 files) but the root cause was non-trivial to trace through the graph-building code. I also identified and advocated for other upstream bugs that were initially deprioritized as edge cases; in one instance, the issue resurfaced years later when a major enterprise customer was impacted — validating the original assessment.
* **Agentic Framework Architecture:** I am currently architecting the **Agentic E2E framework for Summit 2026**. This involves defining how AI agents automate infrastructure and CI/CD across ROSA, devtools, and agent repositories.
* **Foundational Project Building:** I founded `midstream-integration-chatbot` (100+ commits), built `oadp-python-tests` from the ground up (authored all framework code from day 1, 118 commits), and became a major contributor to `oadp-apps-deployer` (68 commits, established the Ansible/KubeVirt role patterns). This is a career-long pattern: I architected Java-based test automation frameworks at Forcepoint and built automation and monitoring tools for Intel's chip design CAD infrastructure — building foundational systems from scratch is what I do.
* **First Terraform PR (Apr 2026):** With no prior Terraform knowledge (but IaC experience), AI-assisted self-onboarding into the `iac-sandbox` GCP project. Produced PR [#59](https://github.com/Jounce-IO/iac-sandbox/pull/59) — optional DNS managed zone + Cloud Domains registration — in a few hours. Corrected starter code, validated with `terraform plan` against live project. Demonstrates rapid ramp-up capability and agentic workflow effectiveness in unfamiliar domains.

  **TODO (update after Klara 1:1, ~week of Apr 28 2026):** Add GCP→IBM migration design outcomes and next SWE task.

> *"Amos was key this quarter... wrote new tests, updated old tests, automated tests, found bugs, FIXED BUGS in OADP and in Velero. Spot on performance and I could not ask for anything more :)"* — **Wes Hayutin (Q2 2025, VIC 150%)**
> *"Amos leveled up this quarter. Really enjoying watching Amos grow into new areas here. Really nice debug, investigation, development and collaboration!!"* — **Wes Hayutin (Q1 2025)**

---

## 2. Technical Acumen & Polyglot Expertise
**L5 Requirement:** An expert in multiple areas of the tech stack who leads the design of multi-component systems.

Nearly three decades of hands-on engineering across every layer of the stack — from Intel's chip design CAD infrastructure (Perl, Bash, Java) to Orange's mission-critical cross-platform automation (.NET, C#, Control-M, SQL) to Forcepoint's enterprise security products (Java REST API/UI frameworks) to Red Hat's cloud-native ecosystem. This is not a narrow specialization; it is a broad, architectural understanding of the entire product lifecycle.
* **Languages & Frameworks:** Go, Python, Bash, Java, C#, .NET, Perl, Ansible, Groovy, Cypress.
* **Infrastructure & AI Stack:** Kubernetes, OpenShift, OCP-Virt, Velero, OADP, CSI, Restic, Kopia, S3/MinIO, Jenkins (JCasC), GitLab CI, Docker, ChromaDB, LlamaIndex, Llama Stack, VLLM, LLaMA.cpp, PyTorch.
* **The Mobile-Agnostic Workflow:** My setup allows me to coordinate features across **4–5 repos per feature** from any device. Key deliveries include: RGW backup location, GCP-S3 support, legacy-aws plugin, and Windows VM testing.

---

## 3. Software Quality & Reliability
**L5 Requirement:** Establishes and monitors testing practices for large-scale systems involving multiple teams.

* **Standard Setting:** I built the **MTV API test framework** from scratch and became an early core contributor to **openshift-adp-python-wrapper** (38+ commits). Both remain the production standard for successor teams. Critically, I authored and fixed bugs directly in the OADP (Go) and upstream Velero (Go) codebases — performing complex development tasks outside of a typical QE role.
* **Release Integrity:** Owned E2E QE strategy for OpenShift Virtualization data protection across **3 major OADP releases (1.3.x, 1.4.x, 1.5.x)**.
* **Review Authority:** I have reviewed **137+ MRs** across 7+ team members and **55+ OADP documentation PRs**, ensuring technical accuracy for customer-facing documentation.

> *"Thank you for your hard work, attention to detail, and commitment to delivering a high-quality OADP 1.3 and timely release."* — **Aziza Karol**
> *"Your outstanding efforts in testing the OADP 1.4.0 release. This was a critical and exceptional release... your dedication played a pivotal role in our success."* — **Daniel Gur (Jul 2024)**

---

## 4. Mentor & Develop Engineering Talent
**L5 Requirement:** Coaches and mentors senior/principal engineers and role models mentorship.

* **Instrumental Promotion Impact:** **Shahaf Bahar** explicitly credited my mentorship as instrumental in their recent promotion.
* **AI-First Coaching:** I actively coach engineers across teams (devtools, ROSA, agents) to overcome "AI anxiety" by adopting a **verification-first workflow**. This allows engineers to use agents as a learning accelerator, compressing the learning curve for Go, RAG, and infrastructure automation.
* **Mentorship at Scale:** I established the **ai-tools** section in the devtools repository as a team-wide hub for shared prompts, agent tasks, and workflows across Claude, Cursor, and Gemini — this is mentorship encoded as infrastructure, teaching the organization rather than individuals.

> *"Thanks to your mentorship, I've been able to overcome challenges and achieve new heights, culminating in my recent promotion."* — **Shahaf Bahar**
> *"I couldn't think of myself for where I am right now without you."* — **Aadarsh Raj**
> *"You support my team and teach them with passion and dedication."* — **Meital Arki**

---

## 5. Business Impact & Financial Stewardship
**Definition:** Owns technical initiatives with visible business impact; identifies cost-saving opportunities.

* **Compute Cost Leadership (`hybrid-llm`):** I developed `hybrid-llm` as a strategic model for **routing and decentralized compute**. By proving that a mobile device (like a Samsung 24FE) can offload specific AI workloads from expensive cloud providers to local silicon, I am advocating for a "Smart Routing" strategy that has the potential to save significant costs for both individual engineers and the enterprise.
* **MTV Critical Escalation Resolution:** Joined Red Hat and was immediately tasked with stabilizing MTV, proving critical to resolving initial critical escalations for a product the entire company was focused on.
* **MTV Cross-Team Assistance (Q3 2024):** While already in OADP, returned to assist the MTV team for approximately a month when they needed help — demonstrating cross-team ownership and organizational flexibility. This was recognized in my Q3 2024 quarterly review under Aziza Karol as "MTV work (cross-team collaboration)."
* **Revenue & Retention:** I architected the **legacy backup library** supporting 2–3 year customer compliance, directly preventing churn for enterprise OADP customers.
* **Organizational Mobility:** My ability to execute complex cluster lifecycles and reviews from a mobile device sets a new standard for engineering responsiveness.

> *"The whole company is VERY focused on Virt and this work will be quite critical."* — **Wes Hayutin**
> *"Your engagement on Slack channel and providing face-to-face guidance to Solution Architects is awesome."* — **Aziza Karol**
> *"Your dedication and contributions have been invaluable to the team, and I appreciate the positive impact you've had on our projects."* — **Aziza Karol (Year-End Summary)**

---

## 6. SDLC Innovation & AI Leadership
**Definition:** Drives the strategy for integrating advanced AI ecosystems and evolves the SDLC.

* **Strategic "Dogfooding":** I advocated for and built **Llama Stack-based implementations** for our internal tooling — notably the **midstream-integration-chatbot**, a RAG chatbot built on Llama Stack with detailed trace exposing RAG and LLM payloads for full transparency. Demoed to the team with positive reviews. This ensures Red Hat validates its own AI stack internally, creating a critical engineering-to-product feedback loop.
* **Agentic SDLC:** I have defined a net-new SDLC for agentic systems where velocity (PRs in minutes) is paired with a rigorous, QE-rooted **verification layer** that makes AI output trustworthy. In this dimension, my evidence meets L5 and approaches L6 ("Sets the technical vision for AI-driven engineering") — I am not just driving strategy but defining how AI engineering works for the team.
* **Efficiency Tools:** Built **test-analyser** (Claude/Vertex AI) to automate E2E regression analysis, reducing diagnosis time from hours to minutes. Built **classifier-eng**, a FastAPI log classifier service integrated into CI pipelines for automated log classification. Built **auto-todo**, a self-evolving application where AI agents autonomously handle GitHub issues — reading the codebase, writing code, opening PRs, auto-fixing on test failure, and deploying via Vercel preview.
* **AI Ecosystem Breadth:** Beyond the production tools, I systematically explored different facets of AI engineering through targeted POCs — each one designed to answer a specific question and feed learnings into production decisions:
  - **ai-midstream-integration-chatbox** (51 commits): unified Q&A chatbot with RAG + live MCP tools for Jira, Confluence, GitLab, GitHub, and Google Docs
  - **ai_midstream_lib**: reusable patterns library for Red Hat AI Integration agents
  - **hybrid-llm**: local/cloud LLM routing — proved a mobile device can offload workloads from cloud GPU, exploring cost-efficient inference
  - **voice-assistant**: Whisper.cpp STT with hotword detection, learning commands locally for token efficiency
  - **auto-todo**: fully autonomous agentic development loop — AI reads codebase, writes code, opens PRs, auto-fixes on test failure
  - **dual-llm-chat**, **source-pad**: multi-model orchestration exploring how different models complement each other
  - Established the **ai-tools** section in the devtools repository as a team-wide hub for shared prompts, agent tasks, and workflows across Claude, Cursor, and Gemini.
  
  This is an engineer's lab notebook, not abandoned code — each experiment informed architectural decisions in the production tools that followed.

> *"Amos has had some great ideas and there is code to back it too."* — **Wes Hayutin**
> *"This work was vital for improving the quality and velocity of docs creation."* — **Daniel Gur**

---

## Job Skills Summary

* **Technical Acumen (L5):** Polyglot across Go, Python, Bash, and Ansible. Expertise in local LLM orchestration and resource-aware routing. Nearly 30 years of hands-on engineering from Intel chip design infra to cloud-native AI platforms.
* **Leadership (L5):** Career-long leadership trajectory — from scaling NetVision's support function from a small expert team to a full call center (1996), to being recognized by 4+ managers as a critical technical leader at Red Hat.
* **Influence (L5):** Corrected Velero upstream roadmap; peers seek guidance proactively.
* **Collaboration (L5):** Actively evaluated and joined the opendatahub-io/llama-stack-demos community to validate Red Hat's AI stack direction — contributing a multi-source RAG crawler demo (PR #327).
* **System Design (L5):** Architected fault-tolerant systems — the verification layer in the agentic SDLC is specifically a fault-tolerance mechanism for AI-generated code, ensuring reliability at scale.
* **Communication (L5):** Despite learning disabilities, communicates complex strategies effectively across the organization — chatbot sprint review demo, multi-hour Docs training, face-to-face SA guidance, ai-tools README as cross-team documentation.
* **Knowledge Sharing (L5):** Delivered 4+ hour OADP training; reviewed 55+ OADP doc PRs. Established ai-tools hub as internal knowledge base. Conference talks are a gap to address — current knowledge sharing is primarily internal and through code/tooling.

> *"Amos is very responsible for his work, eager to help others and comes up with ideas and suggestions to automate and improve things and processes."* — **Shveta Sachdeva**
> *"Looking at you makes others improve themselves as well."* — **Igor Braginsky**

