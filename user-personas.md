# User Personas — Real-Time Fraud Detection Platform

**Product name:** Real-Time Fraud Alert & Review System  
**Author:** Jorge S. Ortiz  
**Last updated:** Q1 2025  

---

## How to use this document

These personas were developed through stakeholder interviews and 
workflow observation during the discovery phase. They inform feature 
prioritization, UX decisions, and acceptance criteria across the PRD.

---

## Persona 1 — The Fraud Analyst

**Name:** Marcus T.  
**Title:** Fraud Operations Analyst  
**Experience:** 3 years in fraud review  

### Who he is
Marcus works an 8-hour shift reviewing transaction alerts. On a typical 
day he processes 80–120 alerts manually. Most of his time is spent 
switching between three systems: the alert queue, the transaction 
database, and the case management tool.

### Goals
- Clear his alert queue efficiently without missing real fraud
- Spend more time on complex cases, less time on obvious false positives
- Have confidence that his decisions are being recorded correctly

### Pain points
- Alert fatigue — too many low-quality alerts erode focus on real threats
- Context switching — critical transaction data lives in a separate system
- No feedback loop — he never knows if his false positive flags 
  improved anything

### What success looks like for Marcus
> "I want to open one screen, see the alerts that actually matter, 
> action them fast, and know my work is making the system smarter."

### Design implications
- Dashboard must surface risk score and reason *before* the analyst 
  clicks into an alert
- One-click disposition (Confirm / False Positive / Escalate) — 
  minimize keystrokes
- False positive feedback must be simple — a single field, not a form

---

## Persona 2 — The Compliance Officer

**Name:** Diana R.  
**Title:** BSA/AML Compliance Officer  
**Experience:** 8 years in financial services compliance  

### Who she is
Diana is responsible for ensuring the platform meets Bank Secrecy Act 
and AML regulatory requirements. She does not review individual alerts 
day-to-day, but she owns the audit trail and is the first call when 
regulators request documentation.

### Goals
- Maintain a complete, accurate, and exportable audit log at all times
- Adjust risk thresholds and escalation rules without filing an 
  engineering ticket
- Demonstrate to regulators that every alert was reviewed and actioned

### Pain points
- Audit logs are incomplete or require manual reconciliation before 
  reporting
- Any threshold change requires a 2-week engineering sprint
- Regulatory requests arrive with short turnaround and data is hard 
  to pull quickly

### What success looks like for Diana
> "When a regulator asks me for every fraud alert from the last 
> 90 days, I want to export it in under five minutes — clean, 
> complete, and audit-ready."

### Design implications
- Audit log must be immutable — no edits after an action is recorded
- Export must be one click, filterable by date range, analyst, 
  alert type, and disposition
- Threshold configuration must live in a compliance admin panel — 
  no code required

---

## Persona 3 — The Engineering Lead

**Name:** Priya K.  
**Title:** Senior Software Engineer — Data & ML Infrastructure  
**Experience:** 6 years, 2 years on fraud systems  

### Who she is
Priya owns the ML pipeline that generates risk scores and the data 
infrastructure that feeds the alert system. She is not a daily user 
of the analyst dashboard, but she depends on it to produce the 
feedback data her models need to improve.

### Goals
- Get clean, structured analyst feedback to retrain the risk model
- Minimize on-call incidents caused by alert delivery failures
- Build infrastructure that scales without redesign at 2x volume

### Pain points
- Analyst feedback is currently unstructured — free text in a 
  spreadsheet, not usable for model training
- No monitoring on alert delivery latency — she finds out about 
  failures when analysts complain
- System was not designed for scale — performance degrades at peak hours

### What success looks like for Priya
> "Give me a structured feedback API and a latency dashboard and I 
> can make this model meaningfully better every sprint."

### Design implications
- Feedback data must be structured (not free text) and available 
  via API
- Build latency monitoring into the system from day one — not a 
  Phase 2 item
- Alert ingestion architecture must be designed for horizontal 
  scaling

---

## Persona comparison

| Dimension | Marcus (Analyst) | Diana (Compliance) | Priya (Engineering) |
|---|---|---|---|
| Uses the dashboard daily | ✓ | Occasionally | Rarely |
| Cares most about | Speed & accuracy | Auditability | Data quality & scale |
| Biggest risk if we fail them | Fraud slips through | Regulatory violation | Model degrades |
| Key feature dependency | Alert ranking, one-click action | Export, admin controls | Feedback API, latency monitoring |
| Involvement in UAT | High | High | Medium |

---

*Jorge S. Ortiz — Product Manager | Chicago, IL*  
*github.com/jorgesortiz*
