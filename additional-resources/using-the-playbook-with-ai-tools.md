---
layout:
  width: default
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: false
  pagination:
    visible: true
  metadata:
    visible: true
  tags:
    visible: true
---

# Using the Playbook with AI Tools

You don't need to read through the entire playbook every time you want to apply the 4-level framework. This page shows you five ways to bring the playbook directly into the AI tools you're already using — so you can ask questions, build evaluation plans, and get guidance in plain conversation.

Each option has a different level of setup and works best for different situations. Start with whichever feels most approachable.

---

## Option 1: Claude Skills

**Best for: Most people. Works by just having a conversation — no links to paste, no setup needed.**

Claude Skills are pre-built assistants that know the 4-level framework. Once installed, the skill activates automatically when you ask evaluation-related questions — you don't need to know the playbook exists or do anything differently. Just ask Claude naturally.

For example: *"Help me build an evaluation plan for our agriculture chatbot"*, *"What should we measure before we scale?"*, or *"How do I explain this to my funder?"* — and Claude will respond using the framework.

**How to install**

You need [Claude Code](https://claude.ai/code) — Anthropic's free desktop and CLI app — to use skills.

**Step 1.** Download the skill file from this repository:

[`skills/ai-eval-playbook-guide.skill.md`](../skills/ai-eval-playbook-guide.skill.md)

![](<../.gitbook/assets/ai-tools-skills-01-download.png>)

**Step 2.** Open your terminal and copy the file to Claude's global skills folder:

```bash
cp ai-eval-playbook-guide.skill.md ~/.claude/skills/
```

If the `skills` folder doesn't exist yet, create it first:

```bash
mkdir -p ~/.claude/skills
cp ai-eval-playbook-guide.skill.md ~/.claude/skills/
```

![](<../.gitbook/assets/ai-tools-skills-02-terminal.png>)

**Step 3.** Open Claude Code and start a new conversation. The skill is now active — no further configuration needed.

![](<../.gitbook/assets/ai-tools-skills-03-claude-code.png>)

**Step 4.** Ask any evaluation question as you normally would. Claude will use the playbook framework to answer.

![](<../.gitbook/assets/ai-tools-skills-04-conversation.png>)

{% hint style="info" %}
**Project-level install:** If you only want the skill active for a specific project rather than all your Claude conversations, copy the file to `.claude/skills/` inside your project folder instead of `~/.claude/skills/`.
{% endhint %}

**Things to keep in mind**

* Skills are a snapshot of the playbook at the time they were built. If the playbook is updated, the skill file in this repository will be updated too — but you'll need to re-copy it to your skills folder to get the latest version.
* Skills work in Claude Code (desktop app and CLI). They do not currently work in ChatGPT, Gemini, or the standard claude.ai web interface.

---

## Option 2: NotebookLM

**Best for: Learning the framework, exploring ideas, and getting answers grounded only in the playbook.**

NotebookLM is a free Google tool that lets you upload documents as "sources" and then ask questions about them. When you add the playbook as a source, every answer it gives you is drawn directly from the playbook — nothing made up, nothing from outside.

This makes it a great option if you're new to the framework and want to explore it, or if you want to be confident that responses are grounded in the actual content.

**How to set it up**

**Step 1.** Go to [notebooklm.google.com](https://notebooklm.google.com). You'll need a Google account. Click **Create new notebook**.

![](<../.gitbook/assets/ai-tools-notebooklm-01-homepage.png>)

**Step 2.** In the new notebook, you'll see a panel on the left asking you to add sources. Click **Add source**.

![](<../.gitbook/assets/ai-tools-notebooklm-02-add-source.png>)

**Step 3.** Choose **Website** from the list of source types.

![](<../.gitbook/assets/ai-tools-notebooklm-03-source-type.png>)

**Step 4.** Paste in the following URL, which contains the full playbook text, and click **Insert**:

```
https://eval.playbook.org.ai/llms-full.txt
```

![](<../.gitbook/assets/ai-tools-notebooklm-04-paste-url.png>)

**Step 5.** NotebookLM will process the content. Once it's ready, you can start asking questions in the chat panel on the right.

![](<../.gitbook/assets/ai-tools-notebooklm-05-chat.png>)

You can see an example conversation [here](https://notebooklm.google.com/notebook/983c252d-b579-489a-aa9a-58be877f907d).

**Things to keep in mind**

* NotebookLM keeps responses strictly within what you've uploaded — it won't draw on outside knowledge. This is great for accuracy, but means it won't combine the framework with other context you haven't added.
* You'll need a Google account.
* If the playbook is updated, you can simply remove the source and re-add the URL to get the latest version.
* It's not well-suited to running the same type of task repeatedly — for that, see Gemini Gems below.

---

## Option 3: Gemini Gems

**Best for: Repeatable workflows, especially if your team already uses Google Workspace (Docs, Sheets, Drive).**

Gemini Gems let you create a customised version of Gemini with specific instructions — think of it as a dedicated assistant pre-configured to work with the 4-level framework. You can also connect it to Google Docs, Sheets, and Drive files, making it useful when you want to apply the framework alongside your own organisation's data and documents.

A good way to get started is to use the ready-made sample Gem as a starting point, then build your own with your team's specific context.

**How to use the sample Gem**

**Step 1.** Open the sample Gem [here](https://gemini.google.com/gem/671f8bf9faaf). You'll need a Google account with access to Gemini.

![](<../.gitbook/assets/ai-tools-gems-01-sample-gem.png>)

**Step 2.** Click **Chat** to open a conversation with the Gem. You can ask it evaluation questions the same way you would any AI assistant.

![](<../.gitbook/assets/ai-tools-gems-02-chat.png>)

You can see an example conversation [here](https://gemini.google.com/share/9faf3005399f).

**How to create your own Gem**

**Step 3.** Go to [gemini.google.com/gems](https://gemini.google.com/gems) and click **Create a Gem**.

![](<../.gitbook/assets/ai-tools-gems-03-create.png>)

**Step 4.** Give your Gem a name and write instructions describing what it should do (for example: *"You are an AI evaluation assistant. Use the 4-level framework from the AI Evaluation Playbook to help users design evaluation plans."*). You can also add sources like Google Docs or Sheets from your Drive.

![](<../.gitbook/assets/ai-tools-gems-04-instructions.png>)

**Step 5.** Click **Save** and your Gem is ready to use.

![](<../.gitbook/assets/ai-tools-gems-05-save.png>)

**Things to keep in mind**

* Gems work best for tasks you run regularly — like reviewing an evaluation plan against the framework, or checking whether a set of metrics maps to the right level.
* You'll need a Google account with Gemini access (available on most Google Workspace plans).
* You can add NotebookLM notebooks as sources inside a Gem, combining grounded playbook knowledge with your own files.
* Unlike NotebookLM, Gems can blend the framework with other knowledge — which is powerful, but means answers aren't limited only to the playbook.

---

## Option 4: Paste the Playbook Directly

**Best for: One-off deep dives using any AI tool — Claude, ChatGPT, Gemini, or anything else.**

Every AI assistant has a text box you can type or paste into. The playbook is available as a single text file you can copy and paste at the start of any conversation. Once pasted, the AI will use it as the reference for everything it says next.

This is the most flexible option — it works with any AI tool, no account or setup needed.

**How to do it**

**Step 1.** Open the full playbook text file by visiting this URL in your browser:

```
https://eval.playbook.org.ai/llms-full.txt
```

![](<../.gitbook/assets/ai-tools-markdown-01-url.png>)

**Step 2.** Select all the text on the page (press **Cmd+A** on Mac or **Ctrl+A** on Windows) and copy it (press **Cmd+C** / **Ctrl+C**).

![](<../.gitbook/assets/ai-tools-markdown-02-select-all.png>)

**Step 3.** Open your AI tool of choice — Claude, ChatGPT, Gemini, or any other. Paste the text at the start of a new conversation, followed by your question. For example:

> *[paste playbook text here]*
>
> Based on this framework, what Level 3 evaluations should we run for a health information chatbot used by community health workers?

![](<../.gitbook/assets/ai-tools-markdown-03-paste-chat.png>)

**Things to keep in mind**

* This works in any AI tool — no setup required.
* The playbook text is around 60,000 tokens (roughly 45,000 words). Most modern AI tools can handle this, but very long pastes may slow down responses or incur higher costs if you're on a paid plan.
* You need to paste it fresh every new conversation — it won't carry over.
* For a single page rather than the whole playbook, you can append `.md` to any page URL (for example: `https://eval.playbook.org.ai/level-3-user-evaluation/overview/why-is-this-level-of-evaluation-important.md`).

---

## Option 5: Connect via MCP (for Claude users)

**Best for: People who use Claude regularly and want a live, seamless connection to the playbook.**

MCP (Model Context Protocol) is a way to connect Claude to external resources so it can look things up during a conversation without you needing to paste anything. Once you've added the playbook as a connector, Claude can pull in the relevant sections automatically whenever you ask evaluation-related questions.

This is the most powerful option for regular Claude users — but it does require a small one-time setup.

**How to set it up**

**Step 1.** Open Claude at [claude.ai](https://claude.ai) and go to **Settings**.

![](<../.gitbook/assets/ai-tools-mcp-01-settings.png>)

**Step 2.** In Settings, find the **Integrations** or **Connectors** section and click **Add connector** (the exact wording may vary slightly).

![](<../.gitbook/assets/ai-tools-mcp-02-connectors.png>)

**Step 3.** Paste in the following URL and save:

```
https://eval.playbook.org.ai/~gitbook/mcp
```

![](<../.gitbook/assets/ai-tools-mcp-03-add-url.png>)

**Step 4.** Make sure the connector is toggled on for your chat session, then start a conversation as normal. You don't need to do anything differently — Claude will use the playbook as a reference in the background.

![](<../.gitbook/assets/ai-tools-mcp-04-enabled.png>)

**Example:** Your Theory of Change was written 12 months ago, and you now have Level 1–3 data available. You want to check whether your original assumptions still hold before committing to a Level 4 study. With the playbook connected, Claude can pull up the relevant framework sections and work through the analysis with you — no copying and pasting required.

**Things to keep in mind**

* Some organisations restrict external connections in their IT or security settings. If the connector doesn't work, check with your IT team.
* This only works in Claude — not in ChatGPT or Gemini.
* Once set up, Claude always has access to the latest version of the playbook.

---

## Which option is right for you?

| | Best for | Works in | Stays current? | Setup needed? |
|---|---|---|---|---|
| **Skills** | Everyday use, no setup | Claude only | No (manual update) | None |
| **NotebookLM** | Learning, grounded Q&A | NotebookLM | Yes (re-add source) | Low |
| **Gemini Gems** | Repeatable workflows, G-Suite users | Gemini only | Depends on setup | Medium |
| **Paste directly** | One-off tasks, any AI tool | Any AI tool | Yes (fresh paste) | None |
| **MCP connector** | Regular Claude users | Claude only | Yes (automatic) | Low |

If you're not sure where to start, **NotebookLM** is the easiest way to explore the playbook interactively. Once you're comfortable, **Claude Skills** (when available) will make it even simpler.

---

---

## Example use cases by role

The prompts below are ready to use. Copy one, paste it into Claude (or any AI tool), and adapt the context to your own project. Each one is grounded in a specific part of the 4-level framework.

---

### AI / ML Engineer

_Builds and maintains the AI pipeline, evaluation rubrics, golden datasets, and automated scoring. Primarily works at Level 1 but feeds into Levels 2–4._

**Example 1 — Drafting an evaluation rubric**

> You're building an agricultural advisory chatbot for smallholder farmers in Kenya. You need a Level 1 rubric before writing a single golden dataset entry.

**Try this prompt:**
> I'm building a RAG-based agricultural chatbot for smallholder farmers in Kenya. It answers questions about crop disease, planting schedules, and input sourcing via WhatsApp in Swahili and English.
>
> Using the evaluation rubric guidance from the AI Evaluation Playbook (Level 1), help me draft a 5-dimension rubric. For each dimension include: the qualitative definition, a concrete example of a passing and failing response, and a suggested scorer type (statistical, model-based, or LLM-as-judge).

**What you'll get:** A structured rubric with pass/fail examples and scorer recommendations — ready to hand to your team before the dataset sprint begins.

---

**Example 2 — Seeding a golden dataset**

> Your domain expert has 2 hours. You need to get maximum value from that session by pre-drafting diverse golden dataset entries for their review.

**Try this prompt:**
> I have 2 hours with an agronomist before my golden dataset sprint. My chatbot handles crop disease, planting advice, and input sourcing for maize farmers in Western Kenya.
>
> Generate 15 draft golden dataset entries covering: typical user queries in varying formality and Swahili-English code-switching, out-of-scope requests, and adversarial/safety edge cases. For each entry provide: user input, ideal output structure, and which rubric dimension it primarily tests. Flag the 3 entries most critical for the expert to validate first.

**What you'll get:** A diverse draft dataset that makes the expert session far more productive — with the highest-risk entries flagged for priority review.

---

### Product Manager

_Owns product metrics, the user funnel, A/B test design, and translating evaluation insights into the roadmap. Primarily works at Level 2._

**Example 1 — Designing a user funnel**

> You're launching a maternal health WhatsApp chatbot for expectant mothers in Nigeria. You need a user funnel with metrics before your engineering sprint.

**Try this prompt:**
> We're launching a maternal health chatbot on WhatsApp for expectant mothers in Nigeria. Our theory of change: mothers receive timely health information → increase antenatal care visits → reduce maternal mortality.
>
> Using the user funnel framework from the AI Evaluation Playbook (Level 2), design a complete funnel from Acquisition to Development Outcome. For each funnel stage: define the metric, explain how to measure it in a WhatsApp context, and identify the leading indicator that predicts the next stage.

**What you'll get:** A complete funnel with stage-by-stage metrics, measurement methods, and leading indicators — ready for your engineering sprint planning.

---

**Example 2 — Writing an A/B test plan**

> Retention drops after week 2. You suspect the onboarding tone is too clinical. You need a clean hypothesis and test design before the next sprint.

**Try this prompt:**
> Our maternal health chatbot has a 40% week-2 retention drop. Level 2 data shows users engage heavily in week 1 but disengage after the first prenatal reminder message.
>
> Help me write an A/B test plan following the experimentation guidance in the AI Evaluation Playbook. Include: the specific hypothesis, treatment vs control variants, primary and secondary metrics, minimum detectable effect, guardrail metrics to monitor, and a pre-analysis plan summary. Then list 3 alternative hypotheses I should rule out first via process evaluation.

**What you'll get:** A rigorous test plan with a clear hypothesis, MDE calculation, and a checklist of things to investigate before running the experiment.

---

### Data Scientist

_Builds ETL pipelines, defines metric schemas, runs A/B analysis, and connects data across evaluation levels._

**Example 1 — Designing a data schema across all four levels**

> You need to design a data warehouse schema that links model traces, product events, and survey responses across all four evaluation levels.

**Try this prompt:**
> I'm building the data infrastructure for a digital agriculture platform serving 50,000 farmers. We collect: LLM trace logs (Level 1), WhatsApp engagement events (Level 2), quarterly SMS surveys (Level 3), and annual yield data from partner NGOs (Level 4).
>
> Using the ETL pipeline guidance from the AI Evaluation Playbook, propose a data warehouse schema that links all four levels. Include: table structures, key joins, and how to handle data that arrives at different frequencies. Flag the 3 most common pipeline failures in this kind of multi-level setup.

**What you'll get:** A multi-level schema design with join logic, data frequency handling, and a practical failure checklist.

---

**Example 2 — Building a surrogate index**

> Your Level 4 RCT is 18 months away. You need a surrogate index from Level 2–3 data to run faster product iterations now.

**Try this prompt:**
> We're 18 months from our Level 4 RCT measuring smallholder farmer income gains. We have 6 months of Level 2 data (session depth, feature uptake) and Level 3 data (self-efficacy surveys, question complexity scores).
>
> Following the Surrogate Index framework in the AI Evaluation Playbook, help me construct a surrogate index. Suggest which Level 2–3 metrics to include, how to weight them based on theoretical proximity to income outcomes, how to validate the index against any available Level 4 pilot data, and what the assumptions and limitations are. Output this as a draft methods note I can share with our impact evaluator.

**What you'll get:** A surrogate index design with weightings, validation approach, and a methods note — ready to share with your impact evaluation partner.

---

### User Researcher

_Measures cognitive, affective, and behavioural outcomes. Runs surveys, interviews, and NLP analysis on conversation logs. Primarily works at Level 3._

**Example 1 — Designing an in-chat survey**

> You need a 3-question in-chat survey to measure self-efficacy and knowledge gain after a tutoring session, without disrupting the conversation flow.

**Try this prompt:**
> I'm evaluating an AI math tutoring chatbot for secondary school students in Ghana. I want to measure self-efficacy and immediate knowledge gain after each session, embedded naturally in the WhatsApp conversation.
>
> Using the survey guidance from the AI Evaluation Playbook (Level 3), design a 3-item in-chat survey. For each item: write the question in natural conversational language, specify the response format (e.g. 1–5 scale, yes/no, open text), explain what construct it measures and why, and flag any cultural adaptation considerations for a West African student population.

**What you'll get:** A 3-item survey with conversational wording, validated constructs, and cultural adaptation notes — ready to embed in your chatbot flow.

---

**Example 2 — Analysing conversation logs at scale**

> You have 500 conversation logs from a health chatbot. You need to extract cognitive and affective signals at scale without reading every log.

**Try this prompt:**
> I have 500 conversation logs from a postpartum mental health chatbot deployed in South Africa. I need to extract Level 3 signals at scale without manually reading each log.
>
> Based on the NLP analysis methods in the AI Evaluation Playbook (Level 3), design an analysis pipeline. Specify: which sentiment and linguistic signals to extract and why, the appropriate NLP method for each signal (LIWC, LLM-as-judge, topic modelling), a sample LLM-as-judge prompt for scoring 'perceived empathy' from a conversation excerpt, and guardrail checks to detect AI dependency patterns.

**What you'll get:** A scalable analysis pipeline with method-to-signal mappings, a ready-to-use judge prompt, and dependency detection checks.

---

### Impact Evaluator

_Designs RCTs and quasi-experimental studies, manages counterfactual selection, and connects Level 1–3 evidence to long-term outcomes. Leads Level 4._

**Example 1 — Drafting an RCT pre-analysis plan**

> You're pre-registering a Level 4 RCT for an AI agricultural advisory tool. You need a pre-analysis plan that handles the unique challenges of evaluating a product that will change during the trial.

**Try this prompt:**
> I'm pre-registering a cluster-randomised RCT to evaluate an AI agricultural advisory tool for 800 maize farmers across 40 villages in Ethiopia. Primary outcome: crop yield at harvest. The product will likely update 2–3 times during the 8-month trial.
>
> Using the Level 4 guidance in the AI Evaluation Playbook, draft the key sections of a pre-analysis plan. Include: counterfactual justification, how product versions will be tagged and handled analytically, spillover mitigation strategy (the tool is on WhatsApp and can be shared), power calculation assumptions, primary and secondary outcomes, and pre-specified subgroup analyses by gender and land size. Flag the top 3 AI-specific pitfalls to address.

**What you'll get:** A structured pre-analysis plan with AI-specific versioning and spillover sections — ready for pre-registration.

---

**Example 2 — Stress-testing a Theory of Change**

> Your Theory of Change was written 12 months ago. Level 1–3 data is now available. You need to check whether the causal chain still holds before committing to a Level 4 study.

**Try this prompt:**
> We built a Theory of Change 12 months ago for an AI literacy tutor in rural India. Now we have: Level 1 accuracy data (87% on golden dataset), Level 2 data (35% week-4 retention, most drop-off at onboarding), and Level 3 data (self-efficacy scores improving but knowledge test scores flat).
>
> Using the framework linkages guidance in the AI Evaluation Playbook, stress-test our Theory of Change against this evidence. Identify which causal links are supported, which are broken or uncertain, what the flat knowledge scores imply about our proximal outcome assumptions, whether we are ready for a Level 4 RCT or should iterate further, and what process evaluation questions to answer first. Output this as a structured memo I can share with our funder.

**What you'll get:** A structured memo identifying which causal links hold and which don't — with a clear recommendation on whether to proceed to Level 4 or iterate first.

---

### Domain Expert

_Validates rubrics, golden datasets, metric definitions, and Theory of Change assumptions across health, education, or agriculture domains. Supports all levels._

**Example 1 — Critiquing a rubric from a clinical perspective**

> The engineering team has drafted a Level 1 rubric for a clinical decision support tool. As a nurse supervisor, you need to validate it before the golden dataset sprint.

**Try this prompt:**
> I'm a nurse supervisor reviewing a Level 1 evaluation rubric drafted by engineers for an AI clinical decision support tool used by community health workers in Uganda. The rubric has 5 dimensions: medical accuracy, response completeness, safety, tone, and latency.
>
> Help me critique this rubric from a clinical domain expert perspective, following the AI Evaluation Playbook's guidance on rubric validation. For each dimension: flag what the engineers likely missed from a clinical workflow standpoint, suggest a concrete real-world failure case that the current definition would miss, and propose a sharper domain-specific definition. Then suggest one additional dimension the engineers have overlooked entirely.

**What you'll get:** A detailed critique with dimension-by-dimension gaps, real failure cases, sharper definitions, and a missing dimension — ready to return to the engineering team.

---

**Example 2 — Annotating a Theory of Change**

> You're reviewing a Theory of Change for an AI advisory tool for smallholder farmers in Northern Ghana. The causal chain looks clean on paper — your job is to find where it breaks in the field.

**Try this prompt:**
> I'm a domain expert reviewing a Theory of Change for an AI advisory tool for smallholder farmers in Northern Ghana. The ToC assumes: farmers receive AI crop advice → act on advice within 48 hours → improve crop management → increase yields.
>
> Using the Theory of Change guidance from the AI Evaluation Playbook, help me identify the weakest assumptions from a field implementation perspective. For each weak link: explain the real-world constraint that breaks the assumption (e.g. input availability, weather, land tenure), suggest a Level 2 or Level 3 metric that would detect when this link is failing, and recommend a process evaluation method to investigate it. Format this as annotated ToC review notes I can return to the research team.

**What you'll get:** Annotated ToC notes with field-grounded constraints, early-warning metrics, and process evaluation methods — ready to send back to the research team.

---

### Policy Analyst

_Works in government, multilaterals, or think tanks. Interprets evaluation findings, assesses whether a tool is ready to scale, and translates technical evidence into recommendations for decision-makers._

**Example 1 — Writing a policy brief from evaluation data**

> Your ministry is deciding whether to integrate an AI agricultural advisory tool into the national extension service for 2 million smallholder farmers. You have technical evaluation reports and need a 2-page brief for the Secretary.

**Try this prompt:**
> I'm a policy analyst at a ministry of agriculture. We're evaluating whether to integrate an AI advisory chatbot into the national extension service. I have the following evaluation summary: Level 1 accuracy 89% overall but 74% word error rate in Amharic; Level 2 week-4 retention 52%, with heavy urban/rural split; Level 3 self-efficacy scores up 0.4 SD after 8 weeks, knowledge test scores flat, 12% of users show AI dependency signals.
>
> Using the AI Evaluation Playbook's 4-level framework, help me interpret this evidence for a non-technical Secretary-level audience. Structure your response as: (1) a plain-language verdict on each level — what it means in practice, not what the number is; (2) the 2 biggest risks of scaling now versus waiting; (3) the 3 conditions the implementer must meet before national rollout; and (4) a one-paragraph executive summary I can put at the top of the brief.

**What you'll get:** A structured brief with plain-language verdicts, risk analysis, scale conditions, and a one-paragraph executive summary — ready to hand to the Secretary.

---

**Example 2 — Comparing two competing interventions**

> Two AI tools are competing for the same budget. You need to compare them not by their marketing claims, but by the strength of their evidence chains.

**Try this prompt:**
> I need to compare two AI interventions competing for the same funding:
>
> Option A — AI maternal health chatbot: Level 1 accuracy 91%, Level 2 week-4 retention 61%, Level 3 showing reduced anxiety (effect size 0.3 SD), no Level 4 evidence yet. Cost per user: $4.
>
> Option B — AI teacher coaching tool: Level 1 accuracy 78%, Level 2 week-4 retention 44%, Level 3 knowledge gains 0.5 SD but self-efficacy flat, one Level 4 RCT in progress (results in 9 months). Cost per user: $11.
>
> Using the AI Evaluation Playbook's evidence strength framework across all four levels, help me structure a comparison. For each option: assess the strength and gaps in the evidence chain, flag what is missing before a scaling decision is justified, estimate the relative risk of a premature scale-up, and suggest what interim condition or milestone should be attached to any funding decision.

**What you'll get:** A structured comparison that reads the evidence pattern — not just the numbers — and surfaces what each product still needs to prove before it earns a scaling decision.

---

### Funding Reviewer

_Works at a foundation, bilateral donor, or multilateral. Reviews grant proposals for GenAI projects, assesses whether proposed evaluation plans are rigorous enough, and sets evaluation conditions for funding._

**Example 1 — Reviewing a proposal's evaluation plan**

> A promising NGO has submitted a $2M proposal for an AI literacy tutor. Their evaluation section is 3 paragraphs. You need a structured critique before the investment committee meeting.

**Try this prompt:**
> I'm reviewing a $2M grant proposal for an AI literacy tutor targeting out-of-school girls aged 10–14 in rural Pakistan. The applicant's entire evaluation plan reads: "We will track user satisfaction surveys and engagement analytics, aiming for 80% satisfaction and 70% weekly active users by month 6. A third-party evaluation will be commissioned in year 2."
>
> Using the AI Evaluation Playbook's Minimum Viable Evaluation checklists for all four levels, score this evaluation plan against what the playbook considers the minimum bar for each level. For each level: state whether the plan meets, partially meets, or fails to meet the MVE standard, explain the specific gap, and write 1–2 specific questions I should ask the applicant in the clarification call. Then give an overall readiness verdict: fund as-is, fund with conditions, request a resubmission, or decline. Include the 3 non-negotiable conditions I would attach to any funding decision.

**What you'll get:** A level-by-level gap analysis mapped to the MVE checklists, specific clarification questions, and a funding verdict with non-negotiable conditions — reviewable by your investment committee.

---

**Example 2 — Setting evaluation requirements for an RFP**

> Your foundation is launching a $10M RFP for GenAI tools in primary healthcare. You need evaluation requirements that are rigorous but won't exclude smaller organisations.

**Try this prompt:**
> I'm designing evaluation requirements for a $10M RFP for GenAI tools in primary healthcare across Sub-Saharan Africa. Applicants will range from small local NGOs to established international organisations. We want rigorous evaluation without creating requirements so burdensome that only large organisations with research departments can apply.
>
> Using the AI Evaluation Playbook's Minimum Viable Evaluation framework and tiered approach, help me design a two-tier evaluation requirement: a baseline tier all applicants must meet, and an enhanced tier for applicants requesting over $500K. For each tier and each of the 4 evaluation levels, specify the minimum required activities, the evidence format you'd accept, and the red lines that would disqualify a proposal regardless of tier.

**What you'll get:** A two-tier evaluation framework with per-level requirements, accepted evidence formats, and disqualifying red lines — ready to paste into your RFP.

---

<details>

<summary>💬 Want to suggest edits or provide feedback?</summary>

{% embed url="https://tally.so/r/A788l0?originPage=references%2Fusing-the-playbook-with-ai-tools" %}

</details>
