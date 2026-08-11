---
name: quote-to-jtbd
description: 'Turn stakeholder quotes into Jobs to be Done statements for discovery. Use when separating customer, agent, manager, and finance perspectives, rewriting feature requests into outcome-focused jobs, and prioritizing by business impact and evidence strength.'
argument-hint: 'Stakeholder quote(s) and optional context such as role, process area, or evidence IDs'
user-invocable: true
disable-model-invocation: false
---

# Quote to JTBD

Convert stakeholder quotes into outcome-focused Jobs to be Done (JTBD) statements using:

When ..., I want to ..., so that ...

This skill is for discovery framing. It emphasizes what people are trying to achieve, not the features they ask for.

## When to Use
- You have interview quotes, notes, or observations and need structured JTBD statements.
- Stakeholders are asking for solutions, but the underlying job is unclear.
- You need to separate jobs by perspective: customer, agent, manager, and finance.
- You need to rank jobs by impact and confidence of evidence.

## Inputs
- One quote or a batch of quotes.
- Stakeholder role if known.
- Optional evidence reference (for example note ID).
- Optional operating context (process stage, channel, policy, metric).

## Core Output
For each selected quote, produce:
- Perspective: customer, agent, manager, or finance.
- JTBD statement in exact format:
  - When ...
  - I want to ...
  - so that ...
- Business impact summary.
- Evidence strength rating.
- Priority recommendation.

Then provide a second synthesized view:
- Deduplicated JTBD list merged from related quote-level jobs.
- Priority ranked list using business impact and evidence strength.

## Procedure
1. Parse the quote.
   - Extract pain point, trigger moment, desired progress, and consequence.
2. Detect perspective.
   - Classify quote as customer, agent, manager, or finance.
   - If ambiguous, infer from wording and role clues.
3. Strip solution bias.
   - Rewrite feature asks into desired outcomes.
   - Keep user intent; remove implementation wording.
4. Build JTBD statement.
   - Write one concise statement using:
     - When ..., I want to ..., so that ...
5. Attach business impact.
   - State operational and/or financial consequence if the job is unmet.
6. Score evidence strength.
  - High: specific quote with clear consequence and at least 2 corroborating quotes.
   - Medium: specific quote but limited corroboration.
   - Low: generic claim or weak consequence link.
7. Prioritize.
   - Set priority using combined view of business impact and evidence strength.
   - Recommended rule:
    - High impact + High evidence -> Critical
    - High impact + Medium evidence -> High
    - Medium impact + High evidence -> High
    - Medium impact + Medium evidence -> Medium
    - Low impact or Low evidence -> Low
8. Validate quality.
   - Ensure outputs are outcome-led, role-correct, and traceable.
9. Produce final two-part output.
  - Part A: one JTBD per quote for traceability.
  - Part B: deduplicated JTBD list for synthesis and prioritization.

## Perspective Rules
- Customer:
  - Focus on clarity, confidence, speed, control, fairness, trust.
- Agent:
  - Focus on handling efficiency, rework reduction, decision support, handoff quality.
- Manager:
  - Focus on visibility, governance, planning, risk management, adoption.
- Finance:
  - Focus on forecast reliability, recovery uplift, cost-to-serve, measurable ROI.

## Decision Points
- If quote includes multiple needs:
  - Split into separate JTBD candidates and keep each atomic.
- If quote is a feature request:
  - Translate into intent before writing JTBD.
- If perspective is unclear:
  - Choose best-fit perspective and flag assumption.
- If evidence is thin:
  - Keep the JTBD but lower evidence strength and priority.
- If two or more quote-level JTBDs describe the same underlying job:
  - Merge them in the deduplicated view and retain references to source quotes.

## Quality Checks
- Statement follows exact pattern: When ..., I want to ..., so that ...
- Language describes outcomes, not product features.
- Perspective is explicitly one of customer/agent/manager/finance.
- Business impact is concrete and decision-useful.
- Evidence strength rationale is explicit.
- Priority reflects both impact and evidence strength.
- Priority labels use Critical, High, Medium, Low.
- Output includes both quote-level and deduplicated JTBD views.

## Prompt Starters
- `/quote-to-jtbd "Customers call back three times because they do not remember what they were told"`
- `/quote-to-jtbd "Every status update requires manual re-keying" role=agent`
- `/quote-to-jtbd data/stakeholder_interview_notes.csv output=both-views`
