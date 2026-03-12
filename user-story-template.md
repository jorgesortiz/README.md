# User Story Template

**Product name:**
**Author:**
**Last updated:**

---

## What is a user story?

A user story captures a feature from the user's perspective.
It follows this format:

> **As a** [type of user],
> **I want to** [perform an action],
> **So that** [I achieve a goal or benefit].

Acceptance criteria define exactly when the story is "done."

---

## User story format

---

### Story [#001] — [Short title]

**As a** [user role]
**I want to** [action]
**So that** [outcome / benefit]

**Priority:** Must have / Should have / Could have / Won't have
**Effort estimate:** Small / Medium / Large
**Status:** Backlog / In progress / In review / Done

**Acceptance criteria:**
- [ ] Given [context], when [action], then [expected result]
- [ ] Given [context], when [action], then [expected result]
- [ ] Given [context], when [action], then [expected result]

**Notes / edge cases:**
-

---

### Story [#002] — [Short title]

**As a** [user role]
**I want to** [action]
**So that** [outcome / benefit]

**Priority:** Must have / Should have / Could have / Won't have
**Effort estimate:** Small / Medium / Large
**Status:** Backlog / In progress / In review / Done

**Acceptance criteria:**
- [ ] Given [context], when [action], then [expected result]
- [ ] Given [context], when [action], then [expected result]
- [ ] Given [context], when [action], then [expected result]

**Notes / edge cases:**
-

---

## Real example — fraud detection

### Story [#001] — Real-time fraud alert

**As a** fraud analyst
**I want to** receive a real-time alert when a suspicious transaction
is flagged
**So that** I can review and act on it before the transaction clears

**Priority:** Must have
**Effort estimate:** Large
**Status:** In progress

**Acceptance criteria:**
- [ ] Given a transaction exceeds the risk threshold, when the system
  detects it, then an alert appears in the dashboard within 30 seconds
- [ ] Given an alert is triggered, when the analyst opens it, then
  they can see transaction amount, account ID, risk score, and reason
- [ ] Given an alert is reviewed, when the analyst marks it resolved,
  then the status updates and is logged with a timestamp
- [ ] Given a false positive, when the analyst dismisses it, then the
  system records feedback to improve the model

**Notes / edge cases:**
- Must work during peak transaction hours without latency
- Alerts must comply with AML audit trail requirements

---

## Story sizing guide

| Size | Complexity | Typical delivery |
|---|---|---|
| Small | Single UI change or simple logic | 1–2 days |
| Medium | New feature with backend + UI | 3–5 days |
| Large | Multi-system integration or new flow | 1–2 sprints |

---

## Definition of done checklist
- [ ] Acceptance criteria all passing
- [ ] Code reviewed and approved
- [ ] QA tested (including edge cases)
- [ ] Compliance / legal signed off (if applicable)
- [ ] Documentation updated
- [ ] Shipped to staging / production

---
*Template by Jorge S. Ortiz — github.com/jorgesortiz*
