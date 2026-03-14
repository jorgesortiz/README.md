# KPIs & Success Metrics — Real-Time Fraud Detection Platform

**Product name:** Real-Time Fraud Alert & Review System  
**Author:** Jorge S. Ortiz  
**Last updated:** Q1 2025  

---

## Why this document exists

Features ship. Metrics tell you if they worked. This document defines 
how success is measured for the fraud detection platform — before 
launch, at launch, and over time. Every metric is tied to a user 
persona, a business goal, or a compliance requirement.

---

## North Star Metric

**Fraud prevented per dollar of operational cost**

This metric captures the core trade-off of the platform: maximizing 
fraud prevention while keeping analyst and infrastructure costs 
efficient. It improves when alert quality goes up, false positives 
go down, and analyst throughput increases.

---

## Metrics by category

### 1. Alert Quality

These metrics measure whether the ML model is surfacing the right alerts.

| Metric | Definition | Baseline | Target | Owner |
|---|---|---|---|---|
| False positive rate | % of alerts that are not actual fraud | ~40% (pre-launch estimate) | < 5% | Data Science |
| True positive rate | % of real fraud events that are caught | TBD at launch | > 90% | Data Science |
| Alert precision | Confirmed fraud / total alerts generated | TBD at launch | > 85% | Data Science |
| Model feedback loop velocity | Days between analyst feedback and model retrain | No loop currently | < 14 days | Engineering |

---

### 2. Analyst Efficiency

These metrics measure whether the platform makes fraud analysts 
faster and more effective.

| Metric | Definition | Baseline | Target | Owner |
|---|---|---|---|---|
| Alerts reviewed per analyst per day | Total alerts actioned / analyst headcount | ~90 | +30% (~117) | Product / Operations |
| Mean time to action (MTTA) | Minutes from alert generation to analyst decision | ~18 min | < 2 min | Product / Engineering |
| Alert queue backlog | Alerts older than 30 min awaiting review | Unknown | Zero at end of shift | Operations |
| Analyst satisfaction score | Quarterly survey score (1–10) | Not measured | > 8 / 10 | Product |

---

### 3. Compliance & Audit

These metrics measure whether the platform meets regulatory requirements.

| Metric | Definition | Baseline | Target | Owner |
|---|---|---|---|---|
| Audit trail completeness | % of alerts with a fully logged decision record | ~70% (manual process) | 100% | Compliance / Engineering |
| Audit export time | Minutes to generate a compliance report | ~45 min (manual) | < 5 min | Product |
| Escalation SLA compliance | % of escalated alerts reviewed within required timeframe | Unknown | > 99% | Compliance |
| Regulatory finding rate | Findings per audit related to alert documentation | TBD | Zero | Compliance |

---

### 4. System Performance

These metrics measure whether the platform is reliable and scalable.

| Metric | Definition | Baseline | Target | Owner |
|---|---|---|---|---|
| Alert delivery latency | Seconds from transaction flag to dashboard appearance | N/A (new system) | < 30 seconds | Engineering |
| System uptime | % availability during business hours | N/A (new system) | > 99.9% | Engineering |
| Peak load performance | Alert latency during highest transaction volume period | N/A (new system) | No degradation vs. baseline | Engineering |
| Incident rate | On-call incidents per month related to alert delivery | N/A (new system) | < 2 per month | Engineering |

---

### 5. Business Impact

These metrics measure the platform's contribution to revenue protection 
and operational cost.

| Metric | Definition | Baseline | Target | Owner |
|---|---|---|---|---|
| Fraud prevented ($) | Estimated dollar value of confirmed fraud stopped | TBD at launch | +15% vs. pre-platform baseline | Finance / Product |
| Fraud loss rate | $ of fraud losses / total transaction volume | TBD at launch | Decrease MoM for first 6 months | Finance |
| Cost per alert reviewed | Total operational cost / alerts reviewed | TBD at launch | Decrease QoQ | Finance / Operations |
|
