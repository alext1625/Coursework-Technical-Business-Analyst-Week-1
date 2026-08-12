# JTBD Priority Summary

Source evidence: [data/stakeholder_interview_notes.csv](../data/stakeholder_interview_notes.csv)

## Prioritised JTBD Statements

| JTBD ID | Actor | Statement | Frequency of evidence | Business impact | Relevance to portal | Overall priority | Evidence link(s) |
|---|---|---|---|---|---|---|---|
| JTBD-001 | Customer | When I have an outstanding balance, I want transparent information on what I owe and what options I have, so that I can act confidently without repeated support calls. | M | H | H | High | [SN-001](#sn-001), [SN-002](#sn-002) |
| JTBD-002 | Agent | When I start contacting customers, I want a single reliable view of prior contact activity, so that I do not duplicate outreach or waste time checking multiple sheets. | H | H | H | High | [SN-063](#sn-063), [SN-073](#sn-073) |
| JTBD-003 | Operations Manager | When simple and complex cases enter the queue, I want routing to separate them correctly first time, so that straightforward cases are resolved quickly instead of waiting days. | M | H | M | Medium | [SN-003](#sn-003) |
| JTBD-004 | Operations Manager | When I run day-to-day collections operations, I want concise case context at handoff, so that agent time is spent on customer contact rather than reconstructing case history. | M | M | M | Medium | [SN-094](#sn-094) |
| JTBD-005 | Finance Partner | When I forecast recovery revenue, I want trusted and timely activity data, so that forecasts are credible for planning and target setting. | H | H | M | High | [SN-070](#sn-070), [SN-012](#sn-012) |
| JTBD-006 | Finance Partner | When I evaluate self-service savings claims, I want measurable and attributable workload reduction, so that business cases reflect real rather than theoretical benefits. | M | H | M | Medium | [SN-031](#sn-031), [SN-046](#sn-046) |
| JTBD-007 | Head of Debt Recovery Operations | When callback commitments are made, I want callback dates to be enforced and owned, so that cases do not remain indefinitely pending and recovery momentum is maintained. | H | H | M | High | [SN-118](#sn-118), [SN-040](#sn-040) |
| JTBD-008 | Compliance Liaison | When deciding whether to scale a change, I want clear before-and-after performance evidence, so that rollout decisions are based on proven value and controlled risk. | L | M | M | Medium | [SN-043](#sn-043) |

## Evidence Reference

### SN-001
Stakeholder: Amina Rahman (Compliance Liaison)  
Quote: Customers respond well when they have control and transparency about what they owe.

### SN-002
Stakeholder: Daniel Okoye (Finance Business Partner)  
Quote: Customers call back three times because they do not remember what they were told on the first call.

### SN-003
Stakeholder: Priya Nair (Operations Manager)  
Quote: Simple cases that could be resolved in minutes take days because they get stuck in the wrong queue.

### SN-012
Stakeholder: Ms Andrea Lamb (Collections Agent)  
Quote: The data quality is so poor that we stopped running management reports altogether.

### SN-031
Stakeholder: Andrea Hunt (Finance Analyst)  
Quote: If self-service reduces agent workload, that headcount saving needs to be real, not theoretical.

### SN-040
Stakeholder: Catherine Frost (Data Analyst)  
Quote: We lose at least 20% of follow-ups because they fall between shifts and no one owns the handoff.  
Caveat: this is a stakeholder estimate, not a measured system figure.

### SN-043
Stakeholder: Simon Burns (Compliance Liaison)  
Quote: We need to measure whether this is better before we commit to rolling it out.

### SN-046
Stakeholder: Christopher Richards (Collections Agent)  
Quote: No one can tell me how much the current workarounds are costing us because the cost is hidden.

### SN-063
Stakeholder: Mr Martyn Akhtar (Operations Analyst)  
Quote: I cannot tell which customers have already been contacted this month without manually checking three different sheets.

### SN-070
Stakeholder: Daniel Farmer (Finance Analyst)  
Quote: The finance team cannot forecast recovery revenue because they do not trust the activity data.

### SN-073
Stakeholder: Mr Dale Jackson (Collections Agent)  
Quote: The activity log does not distinguish between actual contact and failed contact attempts.

### SN-094
Stakeholder: Thomas Wright (Operations Manager)  
Quote: I spend more time reading notes from other agents than I spend actually calling customers.

### SN-118
Stakeholder: Amina Rahman (Head of Debt Recovery Operations)  
Quote: Cases get stuck in 'pending callback' status indefinitely because the callback date is never enforced.


## Top 3 unmet jobs - short justification

### JTBD-002: Unified contact history view
- Why this matters now: Agents currently check multiple sheets to trace contact history, creating duplication, wasted time, and risk of repeated outreach that damages customer relationships.
- Supporting evidence: [SN-063](#sn-063), [SN-073](#sn-073).
- Influence on Phase 1 scope: Unified activity logging with contact-type classification must be a core Phase 1 feature. To turn this into a defensible pound figure, Phase 1 must first baseline current agent time spent per duplicate-check and the resulting case volume, then apply a validated hourly cost rate — until that baseline exists, any savings estimate remains directional, not provable.

### JTBD-005: Trusted activity data for finance forecasting
- Why this matters now: Finance cannot forecast recovery revenue with confidence because activity data quality is too poor, blocking credible planning, target setting, and business case validation.
- Supporting evidence: [SN-070](#sn-070), [SN-012](#sn-012).
- Influence on Phase 1 scope: Phase 1 must establish a data quality baseline and reliable activity capture to create the single source of truth required for finance confidence and ROI measurement.

### JTBD-007: Callback enforcement and ownership
- Why this matters now: Cases remain indefinitely pending because callback dates are not enforced or owned, causing follow-up leakage and slowing recoveries.
- Supporting evidence: [SN-118](#sn-118), [SN-040](#sn-040).
- Influence on Phase 1 scope: Phase 1 workflow design must include callback tracking, ownership, and escalation rules to prevent stalled cases and handoff failures.

### Note
JTBD-001 is high priority but depends on JTBD-002, JTBD-005, and JTBD-007 being addressed first; customer-facing transparency cannot deliver value until contact history is unified, activity data is trusted, and callback ownership is enforced.

## Ranking method used
Each JTBD was scored High, Medium, or Low against frequency of evidence, business impact, and relevance to the portal. Overall priority is High when at least two criteria are High, Medium otherwise, and Low only where the pattern is mostly Low.

## Baseline measurement approach
Not yet started. Before any Phase 1 benefit (including JTBD-002, JTBD-005, and JTBD-006) can be quantified in pounds, we need a measured current-state baseline, not stakeholder estimates:
- Agent time spent per duplicate-check / contact-history lookup (time-and-motion sample across agents).
- Actual follow-up loss rate from system/audit logs, replacing Catherine Frost's 20% estimate (SN-040) with a measured figure.
- Current forecast variance between finance projections and actual recovered revenue.
- Current cost of workarounds, sourced from time-tracking rather than anecdote (per Christopher Richards, SN-046).

Until this baseline is captured, savings claims in the ROI model should be labelled as estimated/hypothetical rather than measured.


