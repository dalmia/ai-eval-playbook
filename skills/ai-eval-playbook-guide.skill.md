---
name: ai-eval-playbook-guide
description: >
  A deep guide to the AI Evaluation Playbook (eval.playbook.org.ai) — a 4-level framework for evaluating GenAI tools in the global development sector (health, education, agriculture, livelihoods in LMICs). Use this skill whenever anyone asks about AI evaluation for development outcomes, the 4-level framework (Model / Product / User / Impact evaluation), how to evaluate GenAI tools, what evaluations to run, what "good" looks like, how levels connect, or any question where the playbook would provide authoritative guidance. Also use it when someone says things like "how do I know my AI is working," "what should we measure," "how do I explain this to my funder," or "where do I start with evals." Always use this skill for any question touching GenAI evaluation in development, social impact, or LMIC contexts — even if the question seems basic.
---

# AI Evaluation Playbook — Deep Guide

> **The playbook is a living document.** The summaries below are a stable orientation, but the canonical content lives at the URLs listed under each section. **Always fetch the live page before composing a substantive answer** so your reply reflects the latest published content. State clearly when an answer is drawn from the live page vs. from cached summary content here.

**Canonical site:** https://eval.playbook.org.ai/
**Maintainer:** The Agency Fund (with IDinsight, CGD, OpenAI / AI4GD)

---

## How to fetch fresh content (priority order)

1. **`web_fetch`** the canonical URL directly. URLs only enter `web_fetch`'s provenance after they appear in a prior user message or prior `web_fetch` result, so work outward from a page you've already fetched (start at https://eval.playbook.org.ai/).
2. If `web_fetch` refuses, use **Control Chrome** to navigate:
   - `mcp__Control_Chrome__open_url` with the target URL
   - `mcp__Control_Chrome__list_tabs` to confirm the page loaded
   - `mcp__Control_Chrome__get_page_content` or `execute_javascript` to read the rendered content (may be flaky — fall back to opening the URL for the user so they can see it themselves).
3. **Dynamic Q&A**: every page has an `?ask=<question>` endpoint that returns a direct natural-language answer plus citations. Append `.md?ask=<URL-encoded-question>` to any page URL. Example: `https://eval.playbook.org.ai/model-behaviour/level-1-module-evaluation/overview.md?ask=what+is+a+golden+dataset`. Use this for narrow lookups when you don't want to fetch a whole page.
4. **Avoid the old GitBook-ID URLs** (`/spaces/<id>/pages/<id>` and `/pages/<id>`). They render but are internal IDs that don't always redirect to canonical paths. Use the semantic paths listed in this skill instead.

> **URL quirks to remember:**
> - Level 3 lives at **`/user-expereince`** — the misspelling is the canonical path. `/user-experience` 404s.
> - Two Level 3 sub-pages have slug/title mismatches: `/how-to-evaluate/descriptive-analysis` renders title "Identify outcome metrics"; `/how-to-evaluate/user-privacy-and-security` renders title "Why Aren't Thoughts, Feelings, and Behavior Changing?"
> - Section-root URLs (e.g. `/model-behaviour`) have a duplicate canonical at `…/overview.md` (e.g. `/model-behaviour/level-1-module-evaluation/overview.md`). Both work.
> - There is no standalone "Authors" page — authorship lives inside the Process and Contribute pages.

---

## High-Level Summary of the 4-Level Framework

The playbook is a unified framework for evaluating Generative AI (GenAI) tools deployed for social impact in low- and middle-income countries (LMICs). It bridges a long-standing gap: tech teams optimize for model performance and ignore impact; impact evaluators measure outcomes and ignore the underlying technology. The playbook ties both worlds together.

**Core premise:** Evaluating a GenAI tool for development outcomes requires four interconnected levels — none of which alone is sufficient.

| Level | Question | Primary owners |
|-------|----------|----------------|
| **L1 — Model** | Does the AI system perform as intended? | AI engineers, ML researchers; domain experts & PMs support |
| **L2 — Product** | Does the overall product engage and retain users? | Product managers, data scientists, UX researchers |
| **L3 — User** | Does the product change users' thoughts, feelings, knowledge, and behavior? | Behavioral scientists, social psychologists, public health researchers, M&E specialists |
| **L4 — Impact** | Do users with access to the product improve development outcomes? | Impact evaluators, economists, independent researchers (J-PAL, IPA, World Bank) |

The four levels form a logical progression: users won't stay engaged (L2) if the system doesn't perform (L1), and development outcomes won't improve (L4) if engagement or user beliefs/behavior break down (L3). They are cyclical, not linear — issues at any level should trigger checks across the others. **Level Linkages** is its own section covering risk assessment, data protection, and process evaluations that span multiple levels.

---

## Sections & Pages — Verified Link Map

Every URL below was independently verified (HTTP 200, rendered title checked) on the most recent crawl. When answering a user question, identify the relevant section, **fetch that page live**, and quote from the live content.

### Introduction — Overview

The "About" entry points and the meta pages explaining how the playbook was made.

- **About this playbook (Home)** — https://eval.playbook.org.ai/
  The landing page. Explains why the playbook exists, who it's for (Implementors & Program Managers; Funders & Policy Makers), and introduces the 4-level framework. Use this as the first stop for funders, board members, or new team members.
- **The Process Behind it** — https://eval.playbook.org.ai/overview/the-process-behind-this-playbook
  How the playbook was built — lessons from the 2025 AI4GD Accelerator (TAF + OpenAI + CGD) with 8 non-profit GenAI products. Cite this when someone asks "who wrote this and why should I trust it?" Authorship/credit info lives here.
- **How to Contribute to the Playbook** — https://eval.playbook.org.ai/overview/how-to-contribute-to-the-playbook
  Steering Committee info, quarterly release cadence, how to suggest edits. Send grantees / partners here who want to add a case study or join the working group.

### Introduction — Setting the Foundation ("Getting Started")

Pre-evaluation building blocks that every team needs in place before diving into the four levels.

- **Building Blocks for GenAI Evaluation (section hub)** — https://eval.playbook.org.ai/getting-started/building-blocks-for-genai-evaluation
  Frames the two pillars of evaluation readiness: people (the team) and process (the infrastructure).
- **Building the Team** — https://eval.playbook.org.ai/getting-started/building-the-team
  Skillsets you need (AI engineers, data engineers, user researchers, social scientists, PMs) and how cross-functional teams should collaborate. Send users here for org/staffing/hiring-sequence questions.
- **Building the Infrastructure** — https://eval.playbook.org.ai/getting-started/building-the-infrastructure
  The reusable building blocks (theory of change, data infrastructure, version tagging, shared user/session IDs) teams should set up before diving into the four levels.

### Introduction — Additional Resources

Cross-cutting reference material — FAQs, terminology, MVE checklists, templates.

- **Frequently Asked Questions** — https://eval.playbook.org.ai/additional-resources/frequently-asked-questions
  Common doubts on roles, when to use each level, "do we need an RCT?", funder-facing concerns. Useful when answering basic orientation questions.
- **Glossary** — https://eval.playbook.org.ai/additional-resources/glossary
  Definitions of every term used throughout (continuous evaluation, golden dataset, rubric, MVE, etc.). Cite this when terminology is at stake.
- **Minimum Viable Evaluations** — https://eval.playbook.org.ai/additional-resources/minimum-viable-evaluations
  Consolidated MVE checklist across all four levels. The single most-requested page by implementors with limited budget/team — "what's the floor I should still do?"
- **Tools & Templates** — https://eval.playbook.org.ai/additional-resources/additional-resources
  External resources and templates: LLM evals guides, evaluation frameworks from PROMPTS / Jacaranda / Farmer.Chat / mMitra, etc. Send users here when they want artifacts to use, not theory to read.

---

### Level 1 — Model Evaluation (Section root: `/model-behaviour`)

**Question: Does the AI system perform as intended?**

The foundational "stress test." Because LLMs predict text rather than "understand" reality, they are prone to hallucinations, knowledge gaps, and instruction failures — especially in LMIC contexts where local languages, norms, and data are underrepresented.

**What it covers:**
- The entire AI pipeline, not just the foundation model: pre-processing (language translation, query refinement, input sanitization), context preparation (system prompt, RAG, tools), and post-processing (safety guardrails, output formatting, hallucination checks).
- Evaluation rubric: up to 5 dimensions — Accuracy, Tone, Safety, Robustness, Linguistic Consistency.
- Scoring methods: Statistical (fast/cheap), LLM-as-Judge (flexible), Human-as-Judge (gold standard).
- Golden Dataset: 30–50 high-quality input/output pairs representing key user interactions.
- A 6-step continuous loop: define rubric → select metrics → build golden dataset → score/analyze → automate in CI/CD → red-team.

**Minimum Viable Evaluation for L1:** 2–3 rubrics with success thresholds; 30–50 item golden dataset; expert review process; ≥1 robust safety/guardrail metric.

**Who does this:** AI engineers and ML researchers lead; domain experts, product owners, and user researchers support.

**Pages in this section:**

- **Overview (section hub)** — https://eval.playbook.org.ai/model-behaviour
- **Who is most involved / Why is this level important?** — https://eval.playbook.org.ai/model-behaviour/level-1-module-evaluation/why-is-this-level-of-evaluation-important
- **What is the "AI system" being evaluated?** — https://eval.playbook.org.ai/model-behaviour/level-1-module-evaluation/what-is-the-ai-system-being-evaluated
- **What is the Minimum Viable Evaluation for Level 1?** — https://eval.playbook.org.ai/model-behaviour/level-1-module-evaluation/what-is-the-minimum-viable-evaluation-for-level-1
- **How is Level 1 evaluation performed?** — https://eval.playbook.org.ai/model-behaviour/how-to-evaluate/how-is-level-1-evaluation-performed
- **Step 1 — Decide on an evaluation rubric** — https://eval.playbook.org.ai/model-behaviour/how-to-evaluate/1.-decide-on-an-evaluation-rubric
- **Step 2 — Decide on metrics** — https://eval.playbook.org.ai/model-behaviour/how-to-evaluate/2.-decide-on-metrics
- **Step 3 — Develop a golden dataset** — https://eval.playbook.org.ai/model-behaviour/how-to-evaluate/3.-develop-a-golden-dataset
- **Step 4 — Scoring & error analysis** — https://eval.playbook.org.ai/model-behaviour/how-to-evaluate/4.-scoring-and-error-analysis
- **Step 5 — Automate your evaluations** — https://eval.playbook.org.ai/model-behaviour/how-to-evaluate/5.-automate-your-evaluations
- **Step 6 — Red-teaming** — https://eval.playbook.org.ai/model-behaviour/how-to-evaluate/6.-red-teaming

---

### Level 2 — Product Evaluation (Section root: `/product-analytics`)

**Question: Does the overall product engage and retain users?**

- **Overview** — https://eval.playbook.org.ai/product-analytics
- **Why is this level important?** — https://eval.playbook.org.ai/product-analytics/level-2-product-evaluation/why-is-this-level-of-evaluation-important
- **What is the "Product" being evaluated?** — https://eval.playbook.org.ai/product-analytics/level-2-product-evaluation/what-is-the-product-being-evaluated
- **Minimum Viable Evaluation** — https://eval.playbook.org.ai/product-analytics/level-2-product-evaluation/what-is-the-minimum-viable-evaluation
- **How is Level 2 evaluation performed?** — https://eval.playbook.org.ai/product-analytics/how-to-evaluate/how-is-level-2-evaluation-performed
- **A/B testing and beyond** — https://eval.playbook.org.ai/product-analytics/how-to-evaluate/methods-for-experimentation-a-b-testing-and-beyond
- **Connection with other levels** — https://eval.playbook.org.ai/product-analytics/how-to-evaluate/connection-with-other-levels
- **Why Aren't Users Engaging?** — https://eval.playbook.org.ai/product-analytics/how-to-evaluate/why-arent-users-engaging

---

### Level 3 — User Evaluation (Section root: `/user-expereince` — typo is canonical)

**Question: Does the product change users' thoughts, feelings, knowledge, and behavior?**

- **Overview** — https://eval.playbook.org.ai/user-expereince
- **Why is this level important?** — https://eval.playbook.org.ai/user-expereince/level-3-user-evaluation/why-is-this-level-of-evaluation-important
- **Who is the "User" being evaluated?** — https://eval.playbook.org.ai/user-expereince/level-3-user-evaluation/who-is-the-user-being-evaluated
- **Minimum Viable Evaluation** — https://eval.playbook.org.ai/user-expereince/level-3-user-evaluation/what-is-the-minimum-viable-evaluation
- **How is Level 3 evaluation performed?** — https://eval.playbook.org.ai/user-expereince/how-to-evaluate/how-is-level-3-evaluation-performed
- **Identify outcome metrics** *(slug: descriptive-analysis)* — https://eval.playbook.org.ai/user-expereince/how-to-evaluate/descriptive-analysis
- **Define guardrail metrics** — https://eval.playbook.org.ai/user-expereince/how-to-evaluate/defining-guardrail-metrics-measuring-potential-harm
- **Consider conducting experiments** *(slug: why-arent-thoughts-feelings-and-behavior-changing)* — https://eval.playbook.org.ai/user-expereince/how-to-evaluate/why-arent-thoughts-feelings-and-behavior-changing
- **Why Aren't Thoughts, Feelings, and Behavior Changing?** *(slug: user-privacy-and-security)* — https://eval.playbook.org.ai/user-expereince/how-to-evaluate/user-privacy-and-security

---

### Level 4 — Impact Evaluation (Section root: `/social-impact`)

**Question: Do users with access to the product improve development outcomes?**

- **Overview** — https://eval.playbook.org.ai/social-impact
- **Who is involved?** — https://eval.playbook.org.ai/social-impact/level-4-impact-evaluation/why-is-this-level-of-evaluation-important
- **What is the "intervention" being evaluated?** — https://eval.playbook.org.ai/social-impact/level-4-impact-evaluation/what-is-the-intervention-being-evaluated
- **Minimum Viable Evaluation** — https://eval.playbook.org.ai/social-impact/level-4-impact-evaluation/minimum-viable-evaluation
- **How is Level 4 evaluation performed?** — https://eval.playbook.org.ai/social-impact/how-to-evaluate/how-is-level-4-evaluation-performed
- **A Quick Primer on Impact Evaluation Methods** — https://eval.playbook.org.ai/social-impact/how-to-evaluate/a-quick-primer-on-impact-evaluation-methods
- **Key design considerations for AI-specific impact evaluations** — https://eval.playbook.org.ai/social-impact/how-to-evaluate/key-design-considerations-for-ai-specific-impact-evaluations
- **Common pitfalls to avoid** — https://eval.playbook.org.ai/social-impact/how-to-evaluate/common-pitfalls-to-avoid
- **Process Evaluation: Why Aren't Outcomes Changing?** — https://eval.playbook.org.ai/social-impact/how-to-evaluate/process-evaluation-why-arent-outcomes-changing

---

### Level Linkages (`/level-linkages`)

- **Overview** — https://eval.playbook.org.ai/level-linkages
- **Risk assessment and mitigation** — https://eval.playbook.org.ai/level-linkages/linkage-across-levels/risk-assessment-and-mitigation
- **Data protection** — https://eval.playbook.org.ai/level-linkages/linkage-across-levels/data-protection
- **Process Evaluations (hub)** — https://eval.playbook.org.ai/level-linkages/linkage-across-levels/process-evaluations
- **Do I need a Process Evaluation?** — https://eval.playbook.org.ai/level-linkages/linkage-across-levels/process-evaluations/do-i-need-a-process-evaluation
- **What does it take to do a process evaluation?** — https://eval.playbook.org.ai/level-linkages/linkage-across-levels/process-evaluations/what-does-it-take-to-do-a-process-evaluation

---

## Minimum Viable Evaluations — Quick Reference

| Level | MVE |
|-------|-----|
| L1 | 2–3 rubrics with thresholds; 30–50 golden dataset items; ≥1 safety/guardrail metric; expert review process |
| L2 | Engagement/retention tracking; Helpful/Not Helpful feedback |
| L3 | 10 conversation logs/week reviewed by expert; 1 proximal outcome measured |
| L4 | Counterfactual study with adequate sample; version control; cost data |

---

## How to Use This Skill

When a user asks a question:

1. **Identify which section and sub-pages are relevant** using the Verified Link Map above.
2. **Fetch the live page(s) before composing a substantive answer.**
3. **Adapt language to the user's role:**
   - Policy makers / funders → evidence standards, cost-effectiveness, risk, readiness for scale.
   - Behavioral scientists / M&E → measurement frameworks, constructs, survey design, causal inference.
   - Engineers / PMs → pipelines, metrics, CI/CD, rubrics, tooling.
   - Nonprofit leaders / implementors → MVEs, team building, practical first steps.
4. **Cite the specific URL you fetched** and quote from the live content.
5. **If a cached summary disagrees with the live page, the live page wins.**
6. **Be honest about tradeoffs.** Help users think about what's *enough* for their stage rather than chasing the maximum.
