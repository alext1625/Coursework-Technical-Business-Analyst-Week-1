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

### Scenario Performance Comparison

| Opportunity ID | Cost (£) | Conservative Net Benefit (£) | Conservative Payback | Base Case Net Benefit (£) | Base Case Payback | Optimistic Net Benefit (£) | Optimistic Payback |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **OP-01** | £45,000[cite: 1] | £1,025,080[cite: 1] | 0.50 mos[cite: 1] | £1,292,600[cite: 1] | 0.40 mos[cite: 1] | £1,426,360[cite: 1] | 0.37 mos[cite: 1] |
| **OP-02** | £45,000[cite: 1] | £356,280[cite: 1] | 1.35 mos[cite: 1] | £2,856,600[cite: 1] | 0.19 mos[cite: 1] | £3,146,760[cite: 1] | 0.17 mos[cite: 1] |
| **OP-03** | £85,000[cite: 1] | £583,800[cite: 1] | 1.53 mos[cite: 1] | £4,591,000[cite: 1] | 0.22 mos[cite: 1] | £5,058,600[cite: 1] | 0.20 mos[cite: 1] |
| **OP-04** | £45,000[cite: 1] | £222,520[cite: 1] | 2.02 mos[cite: 1] | £289,400[cite: 1] | 1.61 mos[cite: 1] | £322,840[cite: 1] | 1.47 mos[cite: 1] |
| **OP-05** | £85,000[cite: 1] | £450,040[cite: 1] | 1.91 mos[cite: 1] | £583,800[cite: 1] | 1.53 mos[cite: 1] | £650,680[cite: 1] | 1.39 mos[cite: 1] |
| **TOTAL** | **£305,000**[cite: 1] | **£2,637,720**[cite: 1] | **1.24 mos**[cite: 1] | **£9,613,400**[cite: 1] | **0.37 mos**[cite: 1] | **£10,605,240**[cite: 1] | **0.34 mos**[cite: 1] |

> **Finance Defense Logic:** Under the **Conservative Scenario** (testing 80% handling efficiency and assuming **£0 soft revenue uplift**), the portfolio still generates **£2.64M in net hard savings**, paying back the entire £305k capital spend in **1.24 months (under 38 days)**[cite: 1, 5]. The business case does not depend on optimistic recovery assumptions to prove a rapid 12-month payback[cite: 5, 10].

---

## Strategic Recommendations & Phase 1 Scope

While **OP-03 (Payment Plan Selection)** offers the highest raw total return (£4.68M), raw ROI alone does not dictate Phase 1 priority[cite: 1, 5, 10]. We recommend balancing value against build feasibility, operational risk, and stakeholder needs[cite: 4, 10].

### Recommended Phase 1 Implementation Scope (£175,000 Total Capital Spend)

┌────────────────────────────────────────────────────────────────────────────────────────┐
│ MUST-HAVE PHASE 1 CORE (£175,000 Investment)                                           │
│                                                                                        │
│ 1. OP-01: Self-Serve Account Summary (£45k Build)                                     │
│    • Core UI component providing balance transparency & account lookup.                │
│    • Delivers £1.29M in net hard labor savings with a 12-day payback.                  │
│                                                                                        │
│ 2. OP-02: Digital Promise-to-Pay Capture (£45k Build)                                  │
│    • Replaces manual note-taking and enforces callback SLA timers.                     │
│    • Solves Amina's primary pain point (SN-118) and delivers £2.86M net benefit.       │
│                                                                                        │
│ 3. OP-05: Rules-Based Case Routing (£85k Build)                                       │
│    • Core screening engine protecting specialist agent queues.                         │
│    • Satisfies Gareth's boundary requirement by filtering out hardship/dispute cases.  │
└────────────────────────────────────────────────────────────────────────────────────────┘

### Justification for Deferring OP-03 & OP-04 to Phase 2

1. **Prerequisite Dependencies:** Customers cannot safely execute legally binding debt payment schedules (**OP-03**) until identity verification (**OP-01**) and automated risk screening (**OP-05**) are established in production[cite: 4, 7].
2. **Integration Complexity:** OP-03 requires building dynamic interest recalculation rules and integrating third-party payment gateways (£85k medium build)[cite: 1, 4, 7]. Deferring OP-03 prevents delivery bottlenecks for **Product Manager Priya Nair** during initial portal rollout[cite: 2, 10].
3. **Compliance Risk Shield:** Launching OP-03 without OP-05's routing rules risks allowing vulnerable customers to auto-commit to unviable payment schedules, creating regulatory compliance exposure[cite: 4, 7, 10].

---

## Implications for Phase 2 Backlog & Prototyping

1. **Immediate Backlog Prioritization:**
   * **Sprint 1–2:** Build OP-01 read-only account summary dashboard & user authentication[cite: 2, 4, 7].
   * **Sprint 3–4:** Implement OP-02 promise-to-pay capture form & automated SLA callback trigger[cite: 2, 4, 7].
   * **Sprint 5–6:** Deploy OP-05 backend case screening engine (`risk_flag == 'N'` filtering)[cite: 1, 2, 4, 7].
2. **Phase 2 Scope Hand-off:**
   * Transition **OP-03 (Payment Plan Engine)** and **OP-04 (Contact Detail Updates)** into the Phase 2 product backlog once core portal stability and callback enforcement are validated in production[cite: 2, 4, 5, 10].