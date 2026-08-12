# Stakeholder Evidence Table

Source: [data/stakeholder_interview_notes.csv](../data/stakeholder_interview_notes.csv)

Selection approach:
- Primary-theme assignment only (no duplicate quote across themes).
- 2-3 strongest quotes per theme, prioritising specificity, impact clarity, and stakeholder variety.
- Confidence levels reflect whether a claim is quantifiable and verifiable against system or process data, not the seniority of the stakeholder who raised it.

Confidence rubric:
- High: describes a directly observable system, process, or data-governance fact that could be confirmed by inspecting records or workflows.
- Medium: a plausible operational claim based on individual estimate, attribution, or perception, without independent measurement.
- Low: a single opinion or anecdote with no corroboration and no practical way to verify.

| stakeholder | quote or observation | theme | business impact | confidence level |
|---|---|---|---|---|
| Daniel Okoye (Finance & Compliance Director) | Every status update in the old system requires manual re-keying into the spreadsheet. | duplicated work | High-volume duplicate admin effort reduces productive case-handling time and increases data-entry error risk. | High |
| Mr Martyn Akhtar (Operations Analyst) | I cannot tell which customers have already been contacted this month without manually checking three different sheets. | duplicated work | Agents spend time reconciling records instead of contacting customers, which lowers throughput and slows recoveries. | High |
| Christopher Richards (Collections Agent) | Every month the finance team has to reconcile our activity count with the database, and they never match. | duplicated work | Reconciliation overhead delays reporting cycles and undermines operational control across teams. | High |
| Catherine Frost (Data Analyst) | We lose at least 20% of follow-ups because they fall between shifts and no one owns the handoff. | delayed or missed follow-up | Direct follow-up leakage leads to missed recovery opportunities and avoidable ageing of debt cases. The 20% figure is a stakeholder estimate, not yet confirmed against system data. | Medium |
| Lawrence Bennett (Finance Analyst) | We have cases sitting in 'awaiting callback' status for months because the promised date was never recorded. | delayed or missed follow-up | Cases stall in queue, increasing cycle time and reducing the chance of successful timely recovery. | High |
| Amina Rahman (Head of Debt Recovery Operations) | Cases get stuck in 'pending callback' status indefinitely because the callback date is never enforced. | delayed or missed follow-up | Weak callback governance creates systemic backlog and inconsistent customer contact performance. | High |
| Mr Dale Jackson (Collections Agent) | The activity log does not distinguish between actual contact and failed contact attempts. | poor account-status visibility | Teams cannot accurately assess progress, causing mis-prioritisation and weak performance management. | High |
| Katherine Taylor-Evans (Finance Analyst) | No one has visibility of what is actually in the pipeline or how long cases typically take. | poor account-status visibility | Lack of pipeline visibility blocks forecasting, capacity planning, and reliable service-level management. | High |
| Dr Louis Sinclair (Service Design Lead) | Different agents use different status codes, which makes reporting meaningless. | poor account-status visibility | Inconsistent status taxonomy makes cross-team reporting unreliable and weakens decision quality. | High |
| Amina Rahman (Compliance Liaison) | Customers respond well when they have control and transparency about what they owe. | customer friction | Poor transparency reduces engagement; clearer self-service and communication can improve payment conversion. | Medium |
| Robert Quinn (Process Improvement Lead) | Customers get transferred between departments and have to repeat their entire situation each time. | customer friction | Repetition across touchpoints increases handle time and complaint risk while damaging trust. | Medium |
| Daniel Farmer (Finance Analyst) | We lose customers because the recovery process is so slow they lose faith we will ever resolve it. | customer friction | Slow recovery journeys increase attrition risk and reduce lifetime value alongside immediate recovery losses; causal link is asserted, not measured. | Medium |
| Ms Andrea Lamb (Collections Agent) | The data quality is so poor that we stopped running management reports altogether. | lack of confidence in the numbers | Missing trusted reporting removes the baseline needed for performance steering and investment decisions. | High |
| Daniel Farmer (Finance Analyst) | The finance team cannot forecast recovery revenue because they do not trust the activity data. | lack of confidence in the numbers | Revenue forecasting becomes unreliable, increasing planning risk and reducing confidence in financial cases. | High |
| Christopher Richards (Collections Agent) | No one can tell me how much the current workarounds are costing us because the cost is hidden. | lack of confidence in the numbers | Hidden operational cost prevents robust business cases and delays prioritisation of corrective investment. | High |
| Thomas Wright (Operations Manager) | Agents are afraid to try new things because they were burned by the last system update. | change resistance or distrust | Low trust in change reduces adoption, extending value realisation timelines and change delivery risk; sentiment is unverified without survey data. | Medium |
| Christopher Richards-Smith (Collections Agent) | Agents are afraid of the portal because they think it will take away their job, not because it won't work. | change resistance or distrust | Perceived job-threat narrative can suppress engagement and create active resistance to rollout; sentiment is unverified without survey data. | Medium |
| Simon Burns (Compliance Liaison) | We need to measure whether this is better before we commit to rolling it out. | change resistance or distrust | Without clear proof-of-value, governance friction can delay approvals and stall implementation. | Medium |


### Note
Direct customer evidence is limited in this dataset, so the table focuses on internal stakeholder observations. The quotes reflect operational pain points and perceived customer impacts, which can be used to infer customer experience issues.

### Confidence caveat
Several figures and sentiments in this table (for example Catherine Frost's 20% follow-up loss, and the change-resistance quotes) are individual estimates or perceptions rather than confirmed system measurements. These should be validated against a measured baseline before being used in financial modelling or board-level reporting.