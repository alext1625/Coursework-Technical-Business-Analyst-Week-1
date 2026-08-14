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
| **B-01** | Total Delinquent Accounts | **100,000** | count | Data Extract (High) | Enterprise population managed by 50+ agents *(Sample extract = 3,246)*. |
| **B-02** | Monthly Straightforward Volume | **38,000** | cases/mo | Analysis (Medium) | Derived as 100,000 × 38% straightforward case share. |
| **B-03** | Avg. Case Handling Time | **18.0** | minutes | Ops Estimate (Medium) | Baseline handling time for straightforward cases (`FA-04`). |
| **B-04** | Admin Hours Lost to Reconciliation | **22.0** | hours/day | Analysis (Medium) | Capacity lost daily across agents checking multiple sheets. |
| **B-05** | Missed Follow-Up Rate | **0.14** | ratio | Data Analysis (Medium) | Indicative missed follow-up rate from tracker sample (`FA-06`). |

### Assumptions

| assumption_id | assumption_name | value | unit | source | confidence_level | notes |
| :---: | :--- | :---: | :---: | :--- | :---: | :--- |
| **A-01** | `agent_hourly_cost` | `22` | GBP | Finance workbook | High | Blended agent hourly cost (`FA-01`). |
| **A-02** | `straightforward_case_share` | `0.38` | ratio | Operations estimate | Medium | Proportion of cases suitable for self-service (`FA-03`). |
| **A-03** | `minutes_saved_per_case_balance_view` | `8` | minutes | Operations target | Medium | Reduction from 18 mins current (`FA-04`) to 10 min target (`FA-05`). |
| **A-04** | `minutes_saved_per_case_promise_capture` | `3` | minutes | Scenario assumption | Medium | Estimated handle time saved per digital promise logged (Stakeholder Notes). |
| **A-05** | `recovery_uplift_percent_payment_plan` | `0.04` | ratio | Finance estimate | Low | 4.0% recovery uplift for plan selection (`FA-07`). |
| **A-06** | `recovery_uplift_for_promise_capture` | `0.025` | ratio | Finance estimate | Low | Scenario based (`FA-08`). |
| **A-07** | `implementation_cost_low_complexity` | `45000` | GBP | Product delivery estimate | Medium | Starter figure (`FA-10`). |
| **A-08** | `implementation_cost_medium_complexity` | `85000` | GBP | Product delivery estimate | Medium | Starter figure (`FA-11`). |
| **A-09** | `monthly_recovery_baseline` | `8000000` | GBP | Finance workbook | Medium | Baseline monthly recoveries (`FA-09`). |

---

### Opportunities 

The following table contains 5 distinct automation opportunities across implementation cost, hard operational labor savings, recovery performance uplift, build effort, and assumption confidence.

| Opp ID | Opportunity Name | Complexity & Build Cost | Annual Hours Saved | Annual Hard Savings (£) | Annual Revenue Uplift (£) | Total Annual Benefit (£) | Net Benefit (£) | 12M ROI (%) | Payback Period |
| :---: | :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **OP-01** | **Self-Serve Account Summary** | Low (£45,000) | 60,800 hrs | £1,337,600 | £0 | **£1,337,600** | **£1,292,600** | **2,872.4%** | **0.4 mos (12 days)** |
| **OP-02** | **Digital Promise-to-Pay Capture** | Low (£45,000) | 22,800 hrs | £501,600 | £2,400,000 | **£2,901,600** | **£2,856,600** | **6,348.0%** | **0.2 mos (6 days)** |
| **OP-03** | **Eligible Payment-Plan Selection** | Medium (£85,000) | 38,000 hrs | £836,000 | £3,840,000 | **£4,676,000** | **£4,591,000** | **5,401.2%** | **0.2 mos (6 days)** |
| **OP-04** | **Contact Detail Update Request** | Low (£45,000) | 15,200 hrs | £334,400 | £0 | **£334,400** | **£289,400** | **643.1%** | **1.6 mos (48 days)** |
| **OP-05** | **Rules-Based Case Routing** | Medium (£85,000) | 30,400 hrs | £668,800 | £0 | **£668,800** | **£583,800** | **686.8%** | **1.5 mos (45 days)** |

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
| **OP-01** | **Self-Serve Account Summary** | £1,337,600 | £1,292,600 | 2,872.4% | 0.4 mos | Low | High | **Phase 1 Rank #1.** Core self-service view delivering £1.29M net hard savings. |
| **OP-02** | **Digital Promise-to-Pay Capture** | £2,901,600 | £2,856,600 | 6,348.0% | 0.2 mos | Low | Medium | **Phase 1 Rank #2.** Direct solution for callback SLA enforcement and follow-up leakage. |
| **OP-05** | **Rules-Based Routing** | £668,800 | £583,800 | 686.8% | 1.5 mos | Medium | Medium | **Phase 1 Rank #3.** Core enabler protecting agent capacity and enforcing vulnerability boundaries. |
| **OP-03** | **Eligible Payment-Plan Selection** | £4,676,000 | £4,591,000 | 5,401.2% | 0.2 mos | Medium | Medium | **Phase 2 Rank #4.** High upside candidate; defer until core portal stability is proven. |
| **OP-04** | **Contact Detail Update Request** | £334,400 | £289,400 | 643.1% | 1.6 mos | Low | High | **Phase 2 Rank #5.** Secondary feature; retain in product backlog. |

---

## Scenario Comparison 

**Conservative Scenario (Hard Savings Only @ 80% Efficiency | Zero Revenue Uplift)**  
- Net Benefit: £2,637,720  
- Combined 12M ROI: 864.8%  
- Payback: 1.24 Months 

**Base Case Scenario (Target Time Savings + Standard Estimated Revenue Uplift)**      
- Net Benefit: £9,613,400  
- Combined 12M ROI: 3,151.9% 
- Payback: 0.37 Months        

**Optimistic Scenario (110% Time Savings + 110% Revenue Uplift Outperformance)**      
- Net Benefit: £10,605,240 
- Combined 12M ROI: 3,477.1% 
- Payback: 0.34 Months         

### Scenario Performance Comparison

| Opportunity ID | Cost (£) | Conservative Net Benefit (£) | Conservative Payback | Base Case Net Benefit (£) | Base Case Payback | Optimistic Net Benefit (£) | Optimistic Payback |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **OP-01** | £45,000 | £1,025,080 | 0.50 mos | £1,292,600 | 0.40 mos | £1,426,360 | 0.37 mos |
| **OP-02** | £45,000 | £356,280 | 1.35 mos | £2,856,600 | 0.19 mos | £3,146,760 | 0.17 mos |
| **OP-03** | £85,000 | £583,800 | 1.53 mos | £4,591,000 | 0.22 mos | £5,058,600 | 0.20 mos |
| **OP-04** | £45,000 | £222,520 | 2.02 mos | £289,400 | 1.61 mos | £322,840 | 1.47 mos |
| **OP-05** | £85,000 | £450,040 | 1.91 mos | £583,800 | 1.53 mos | £650,680 | 1.39 mos |

**Finance Defense Logic:** Under the **Conservative Scenario** (testing 80% handling efficiency and assuming **£0 soft revenue uplift**), the portfolio still generates **£2.64M in net hard savings**, paying back the entire £305k capital spend in **1.24 months (under 38 days)**. The business case does not depend on optimistic recovery assumptions to prove a rapid 12-month payback.

---

## Strategic Recommendations & Phase 1 Scope

While **OP-03 (Payment Plan Selection)** offers the highest raw total return (£4.68M), raw ROI alone does not dictate Phase 1 priority. I recommend balancing value against build feasibility, operational risk, and stakeholder needs.

### Recommended Phase 1 Implementation Scope (£175,000 Total Capital Spend)


***MUST-HAVE PHASE 1 CORE (£175,000 Investment)***
1. OP-01: Self-Serve Account Summary (£45k Build)
    - Core UI component providing balance transparency & account lookup.
    - Delivers £1.29M in net hard labor savings with a 12-day payback.

2. OP-02: Digital Promise-to-Pay Capture (£45k Build)
    - Replaces manual note-taking and enforces callback SLA timers.
    - Solves Amina's primary pain point (SN-118) and delivers £2.86M net benefit.

3. OP-05: Rules-Based Case Routing (£85k Build)
    - Core screening engine protecting specialist agent queues.
    - Satisfies Gareth's boundary requirement by filtering out hardship/dispute cases.

### Justification for Deferring OP-03 & OP-04 to Phase 2

1. **Prerequisite Dependencies:** Customers cannot safely execute legally binding debt payment schedules (**OP-03**) until identity verification (**OP-01**) and automated risk screening (**OP-05**) are established in production.
2. **Integration Complexity:** OP-03 requires building dynamic interest recalculation rules and integrating third-party payment gateways (£85k medium build). Deferring OP-03 prevents delivery bottlenecks for **Product Manager Priya Nair** during initial portal rollout.
3. **Compliance Risk Shield:** Launching OP-03 without OP-05's routing rules risks allowing vulnerable customers to auto-commit to unviable payment schedules, creating regulatory compliance exposure.

---
