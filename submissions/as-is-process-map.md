# Phase 3 - As-Is Process Map

## As-Is Process Map
Link to the As-Is process map: [submissions/as-is-process-map.png](../submissions/as-is-process-map.png)

## Current Process Experience (Summary)

### Customer
Confused and frustrated-contacted multiple times about the same debt with inconsistent information, no control, and no transparency.

### Agent
Exhausted-wasting time checking if work was already done, hunting for information, and managing manual workarounds instead of resolving cases.

### Manager
Blind—no real-time visibility; dependent on manual reconciliation that produces outdated or untrustworthy data for reporting and decision-making.

---

## Automation Suitability Analysis

### Steps Meeting Automation Criteria
*(High-volume, repeatable, rules-driven, lower-risk)*

| Step | Rationale | Current Pain |
|------|-----------|--------------|
| **Account enters delinquency queue** | Automatic system trigger; no judgment required | None—system-driven |
| **Check legacy account status** | Lookup-only; rules-driven retrieval | Duplicate checks; time-wasted |
| **Log/record activity** | Systematic data capture; templated outcomes | Manual note-taking; inconsistent |
| **Send initial contact (email/SMS/letter)** | High-volume; templatable content; scheduled distribution | Repeated contact; no deduplication |
| **Send payment reminders** | Time-based triggers; high-volume; repeatable | Missed follow-ups (20% loss); manual scheduling |
| **Send payment portal links** | High-volume; rules-driven eligibility; templatable | Customers unaware of self-service options |
| **Check payment status** | Lookup-only; rules-driven thresholds | Manual cross-checking; data fragmentation |
| **Reconcile activity across systems** | Repeatable; rules-based data sync; high-volume | Spreadsheet version conflicts; manager reconciliation burden |

---

## Automation Opportunities (Ranked by Impact)

### OPP-001: Unified Activity Logging & Deduplication Engine
- **What:** Automatically capture all agent interactions and system events in a single source of truth; flag duplicate contact attempts across channels in real-time
- **Why:** Eliminates 9 duplicate checks identified in activity tracker; stops redundant customer contact; reduces agent time spent proving activity
- **Evidence:** [SN-038](../data/stakeholder_interview_notes.csv), [SN-011](../data/stakeholder_interview_notes.csv); ACT-00003, ACT-00007, ACT-00014, ACT-00021, ACT-00025, ACT-00029, ACT-00040, ACT-00042, ACT-00048 show duplicate_check_flag=Y
- **Risk Level:** Low (read-only flagging initially)

### OPP-002: Automated Promise-to-Pay Tracking & Enforcement
- **What:** Automatically record promised callback dates, set system-enforced reminders, and escalate automatically if date is missed
- **Why:** Stops cases stuck in 'pending callback' indefinitely; eliminates manual tracking of promised dates; creates enforced SLAs
- **Evidence:** [SN-007](../data/stakeholder_interview_notes.csv), [SN-053](../data/stakeholder_interview_notes.csv); recovery_activity_tracker.csv shows `promise_to_pay` and `promise_due` statuses with vague next actions
- **Risk Level:** Low-Medium (automated enforcement after manual entry)

### OPP-003: Intelligent Contact Scheduling & Channel Selection
- **What:** Automatically determine optimal contact timing, frequency, and channel (SMS, email, letter) based on account history and customer response patterns
- **Why:** Prevents 20% follow-up loss between shifts; optimizes contact time; reduces agent time spent scheduling
- **Evidence:** [SN-040](../data/stakeholder_interview_notes.csv) reports 20% follow-ups lost between shifts; [SN-033](../data/stakeholder_interview_notes.csv) notes timing impact on recovery rates
- **Risk Level:** Low (initial rules-driven; rules can be refined based on outcomes)

### OPP-004: Automated Spreadsheet-to-Database Synchronization
- **What:** Continuously sync activity and status changes from spreadsheet workarounds back to master database in real-time
- **Why:** Eliminates manual reconciliation effort; stops version conflicts; gives managers live data instead of stale reports
- **Evidence:** [SN-008](../data/stakeholder_interview_notes.csv), [SN-025](../data/stakeholder_interview_notes.csv), [SN-063](../data/stakeholder_interview_notes.csv); spreadsheet_reconcile appears 8 times in activity tracker
- **Risk Level:** Medium (data integrity risk if sync rules are incorrect)

### OPP-005: Self-Service Portal Eligibility & Auto-Invite
- **What:** Automatically identify accounts eligible for self-service based on rules (early stage, low risk, simple case type); send targeted portal invites via customer preferred channel
- **Why:** High-volume opportunity; customers willing to self-serve ([SN-005](../data/stakeholder_interview_notes.csv)); reduces agent contact attempts; improves recovery rates
- **Evidence:** [SN-017](../data/stakeholder_interview_notes.csv) shows customers don't know online payment exists; smart_recovery_portal_events.csv shows portal usage for self-eligible cases
- **Risk Level:** Low-Medium (requires clear eligibility rules and customer consent)

### OPP-006: Automated Activity Summary for Manager Reporting
- **What:** Auto-generate daily/weekly manager dashboards showing case status, follow-up compliance, and outcomes without manual reconciliation
- **Why:** Stops manager reliance on manual reconciliation; provides real-time visibility; enables data-driven decisions
- **Evidence:** [SN-048](../data/stakeholder_interview_notes.csv), [SN-012](../data/stakeholder_interview_notes.csv), [SN-070](../data/stakeholder_interview_notes.csv); fragments across phone, legacy_db, email, spreadsheet in activity tracker
- **Risk Level:** Low (reporting-only; no operational changes)

---

### Steps to Keep Agent-Led
*(High-risk, specialist-controlled, judgment-heavy)*

- Promise-to-pay negotiations (customer circumstances, risk assessment)
- Hardship/vulnerability determinations (regulatory, human judgment)
- Dispute resolution (judgment-heavy, specialist review)
- Escalation decisions (risk-based, complex rules)
