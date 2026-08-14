# Automation Opportunity ROI Model

All relevant spreadsheet tabs are included [here](https://docs.google.com/spreadsheets/d/1TtRO32l0aujceaWh25GpXyJ1WZkyxB2c0_85bXCStKY/edit?usp=sharing)

This spreadsheet includes the following tables:
- **Assumptions**: a list of assumptions used in the ROI model, including their source and confidence level.
- **Baseline Metrics**: a list of baseline metrics used in the ROI model, including their source and confidence level.
- **Opportunities**: a list of automation opportunities, including their estimated benefits, costs, confidence level, and priority.
- **ROI Summary**: a summary of the estimated ROI for each opportunity, including the total estimated benefits, costs, ROI percentage, effort level and confidence level.
- **Scenario Analysis**: a scenario analysis of the ROI model, showing how changes in key assumptions affect the estimated ROI.


## Key Baseline Metrics and Assumptions

To ensure complete transparency and credibility, all financial modeling cleanly separates observed system facts, operational estimates, and formula logic.

### Baseline Metrics

| Metric ID | Metric Name | Value | Unit | Source & Confidence | Operational Rationale |
| :---: | :--- | :---: | :---: | :--- | :--- |
| **B-01** | Total Delinquent Accounts | **100,000** | count | Data Extract (High)[cite: 1] | Enterprise population managed by 50+ agents[cite: 1, 10] *(Sample extract = 3,246)*[cite: 1]. |
| **B-02** | Monthly Straightforward Volume | **38,000** | cases/mo | Analysis (Medium)[cite: 1] | Derived as 100,000 × 38% straightforward case share[cite: 1, 5]. |
| **B-03** | Avg. Case Handling Time | **18.0** | minutes | Ops Estimate (Medium)[cite: 1] | Baseline handling time for straightforward cases (`FA-04`)[cite: 1]. |
| **B-04** | Admin Hours Lost to Reconciliation | **22.0** | hours/day | Analysis (Medium)[cite: 1] | Capacity lost daily across agents checking multiple sheets[cite: 1, 10]. |
| **B-05** | Missed Follow-Up Rate | **0.14** | ratio | Data Analysis (Medium)[cite: 1] | Indicative missed follow-up rate from tracker sample (`FA-06`)[cite: 1]. |

### Assumptions



---

### Opportunities 

| Opp ID | Opportunity Name | Complexity & Build Cost | Annual Hours Saved | Annual Hard Savings (£) | Annual Revenue Uplift (£) | Total Annual Benefit (£) | Net Benefit (£) | 12M ROI (%) | Payback Period |
| :---: | :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **OP-01** | **Self-Serve Account Summary** | Low (£45,000)[cite: 1] | 60,800 hrs | £1,337,600 | £0 | **£1,337,600** | **£1,292,600** | **2,872.4%** | **0.4 mos (12 days)**[cite: 1, 5] |
| **OP-02** | **Digital Promise-to-Pay Capture** | Low (£45,000)[cite: 1] | 22,800 hrs | £501,600 | £2,400,000[cite: 1] | **£2,901,600** | **£2,856,600** | **6,348.0%** | **0.2 mos (6 days)**[cite: 1, 5] |
| **OP-03** | **Eligible Payment-Plan Selection** | Medium (£85,000)[cite: 1] | 38,000 hrs | £836,000 | £3,840,000[cite: 1] | **£4,676,000** | **£4,591,000** | **5,401.2%** | **0.2 mos (6 days)**[cite: 1, 5] |
| **OP-04** | **Contact Detail Update Request** | Low (£45,000)[cite: 1] | 15,200 hrs | £334,400 | £0 | **£334,400** | **£289,400** | **643.1%** | **1.6 mos (48 days)**[cite: 1, 5] |
| **OP-05** | **Rules-Based Case Routing** | Medium (£85,000)[cite: 1] | 30,400 hrs | £668,800 | £0 | **£668,800** | **£583,800** | **1.5 mos (45 days)**[cite: 1, 5] |
| **TOTAL** | **Full Enterprise Portfolio** | **£305,000**[cite: 1] | **167,200 hrs** | **£3,678,400** | **£6,240,000**[cite: 1] | **£9,918,400** | **£9,613,400** | **3,151.9%** | **0.37 months**[cite: 1, 5] |

---

**Implementation cost baseline:**
* **Low Complexity** = £45,000
* **Medium Complexity** = £85,000

**Additional Information:**
* **Annual Hours Saved** = (Monthly Case Volume (38,000) × Mins Saved × 12) / 60[cite: 5]
* **Annual Hard Savings** = Annual Hours Saved × £22.00/hr[cite: 1, 5]
* OP-02: Uses 2.5% uplift (FA-08) applied to annual recovery baseline (£8,000,000 x12 x 0.025 = £2,400,000).
* OP-03: Uses 4.0% uplift (FA-07) applied to annual recovery baseline (£8,000,000 x 12 x 0.040 = £3,840,000)

---

## ROI Summary

Below is the consolidated **ROI Summary** ranking all five initiatives by financial performance, effort, data confidence, and strategic recommendation:

| Opp ID | Opportunity Name | Total Benefit (£) | Net Benefit (£) | 12M ROI (%) | Payback (Mos) | Effort Score | Confidence | Recommendation Note |
| :---: | :--- | :---: | :---: | :---: | :---: | :---: | :---: | :--- |
| **OP-01** | **Self-Serve Account Summary** | £1,337,600[cite: 1] | £1,292,600[cite: 1] | 2,872.4%[cite: 1] | 0.4 mos[cite: 1] | Low | High | **Phase 1 Rank #1.** Core self-service view delivering £1.29M net hard savings[cite: 1, 5]. |
| **OP-02** | **Digital Promise-to-Pay Capture** | £2,901,600[cite: 1] | £2,856,600[cite: 1] | 6,348.0%[cite: 1] | 0.2 mos[cite: 1] | Low | Medium | **Phase 1 Rank #2.** Direct solution for callback SLA enforcement and follow-up leakage[cite: 1, 5, 8]. |
| **OP-05** | **Rules-Based Routing** | £668,800[cite: 1] | £583,800[cite: 1] | 686.8%[cite: 1] | 1.5 mos[cite: 1] | Medium | Medium | **Phase 1 Rank #3.** Core enabler protecting agent capacity and enforcing vulnerability boundaries[cite: 4, 5, 7]. |
| **OP-03** | **Eligible Payment-Plan Selection** | £4,676,000[cite: 1] | £4,591,000[cite: 1] | 5,401.2%[cite: 1] | 0.2 mos[cite: 1] | Medium | Medium | **Phase 2 Rank #4.** High upside candidate; defer until core portal stability is proven[cite: 4, 5, 10]. |
| **OP-04** | **Contact Detail Update Request** | £334,400[cite: 1] | £289,400[cite: 1] | 643.1%[cite: 1] | 1.6 mos[cite: 1] | Low | High | **Phase 2 Rank #5.** Secondary feature; retain in product backlog[cite: 5]. |

---

## Scenario Comparison 