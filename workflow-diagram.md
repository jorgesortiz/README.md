# Workflow Diagram — Real-Time Fraud Alert & Review System

**Product name:** Real-Time Fraud Alert & Review System  
**Author:** Jorge S. Ortiz  
**Last updated:** Q1 2025  

---

## Overview

This document maps the end-to-end workflow of the fraud detection 
platform — from the moment a transaction occurs to the final logged 
decision. It covers three flows:

1. **Core alert flow** — how a transaction becomes an alert
2. **Analyst review flow** — how an analyst actions an alert
3. **Compliance & audit flow** — how decisions are logged and exported

---

## Flow 1 — Core Alert Flow

How a transaction becomes an alert in the analyst dashboard.
```
[Customer initiates transaction]
          |
          v
[Transaction data sent to processing system]
          |
          v
[ML risk scoring model evaluates transaction]
          |
     +----|----+
     |         |
[Risk score   [Risk score
 BELOW         AT OR ABOVE
 threshold]    threshold]
     |         |
     v         v
[Transaction  [Alert generated with:
 proceeds      - Transaction ID
 normally]     - Account ID
               - Risk score
               - Risk reason
               - Timestamp]
               |
               v
          [Alert delivered to analyst
           dashboard within 30 seconds]
```

---

## Flow 2 — Analyst Review Flow

How an analyst reviews and actions an alert.
```
[Alert appears in dashboard queue]
          |
          v
[Analyst opens alert — sees:
  - Transaction details
  - Account history
  - Risk score & reason
  - Similar past alerts]
          |
          v
[Analyst makes a decision]
          |
     +---------+---------+---------+
     |         |         |         |
[Confirm   [False     [Escalate] [Needs
 Fraud]     Positive]             Review]
     |         |         |         |
     v         v         v         v
[Case      [Alert     [Alert     [Alert
 opened     closed,    routed     flagged,
 in case    feedback   to senior  stays in
 mgmt       logged     analyst]   queue]
 system]    for ML
            retraining]
     |         |         |         |
     +---------+---------+---------+
                    |
                    v
     [Decision logged to audit trail:
       - Alert ID
       - Analyst ID
       - Decision type
       - Timestamp
       - Feedback (if false positive)]
```

---

## Flow 3 — Compliance & Audit Flow

How compliance officers access and export decision records.
```
[All analyst decisions written to
 immutable audit log in real time]
          |
          v
[Compliance officer logs into
 admin panel]
          |
          v
[Officer applies filters:
  - Date range
  - Analyst
  - Alert type
  - Disposition (Confirmed / FP / Escalated)]
          |
          v
[System generates filtered report]
          |
     +----|----+
     |         |
[View in    [Export
 dashboard]  as CSV]
     |         |
     v         v
[Officer    [File downloaded,
 reviews     ready for
 on screen]  regulatory
             submission]
```

---

## Flow 4 — ML Feedback Loop

How analyst decisions improve the risk model over time.
```
[Analyst marks alert as False Positive
 and submits feedback]
          |
          v
[Feedback stored in structured
 format in feedback database]
          |
          v
[Engineering pulls feedback data
 via API on retrain schedule
 (target: every 14 days)]
          |
          v
[ML model retrained on new
 analyst decision data]
          |
          v
[Updated model deployed —
 false positive rate reviewed
 against previous baseline]
          |
          v
[PM reviews metric impact,
 documents in sprint retro]
```

---

## End-to-end summary
```
TRANSACTION
    |
    v
ML SCORING
    |
    v
ALERT GENERATED
    |
    v
ANALYST REVIEWS
    |
    v
DECISION LOGGED -----> AUDIT TRAIL -----> COMPLIANCE EXPORT
    |
    v
FEEDBACK CAPTURED
    |
    v
MODEL RETRAINS
    |
    v
ALERT QUALITY IMPROVES
```

---

## Key decision rules

| Decision | Trigger | Next step |
|---|---|---|
| Alert generated | Risk score at or above threshold | Sent to analyst dashboard |
| Auto-deprioritized | Risk score in lowest 10% of threshold range | Moves to bottom of queue |
| Escalated | Analyst flags as high complexity | Routed to senior analyst |
| False positive logged | Analyst dismisses with feedback | Sent to ML feedback database |
| Audit record created | Any analyst action taken | Written immediately, immutable |
| Compliance export | Officer requests report | Generated within 60 seconds |

---

## System boundaries

| System | Owner | Role in workflow |
|---|---|---|
| Transaction processing system | Client / Partner | Source of transaction data |
| ML risk scoring model | Data Science | Generates risk scores |
| Alert dashboard | Product / Engineering | Analyst-facing review interface |
| Case management system | Operations | Receives confirmed fraud cases |
| Audit log database | Engineering | Stores all decisions immutably |
| Compliance admin panel | Product / Engineering | Officer reporting and config |
| Feedback API | Engineering | Sends analyst feedback to ML pipeline |

---

*Jorge S. Ortiz — Product Manager | Chicago, IL*  
*github.com/jorgesortiz*
