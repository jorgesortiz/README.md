# Feature Prioritization — SpendingHabits.io

**Author:** Jorge S. Ortiz  
**Last updated:** Q1 2025  
**Framework:** MoSCoW (Must have / Should have / Could have / Won't have)  

---

## What is MoSCoW?

A prioritization framework that forces honest decisions about what 
actually ships versus what sounds good in a meeting.

- **Must have** — Non-negotiable. Product does not launch without this.
- **Should have** — High value, not launch-blocking. Ships in early 
  releases.
- **Could have** — Nice to have. Ships if capacity allows.
- **Won't have** — Explicitly out of scope for this phase. Documented 
  to prevent scope creep.

---

## Prioritization principles

Every feature decision was guided by three questions:

1. Does this directly solve a core pain point for Brianna 
   (our primary persona)?
2. Does this support the credit union B2B2C partnership model?
3. Does this build the habit loop that drives retention?

---

## Must Have — Launch Blockers

These features define the minimum viable product. Without them, 
the product cannot launch.

| # | Feature | User story | Persona | Rationale |
|---|---|---|---|---|
| 1 | Bank & credit card sync | As a user, I want to connect my accounts so my transactions are tracked automatically | Brianna, Alex | Core value prop — manual entry kills retention |
| 2 | Spending dashboard | As a user, I want to see a clear visual summary of where my money is going | Brianna | Primary reason users download the app |
| 3 | Spending categories | As a user, I want my transactions automatically categorized so I don't have to tag them manually | Brianna | Required for dashboard to be meaningful |
| 4 | Budget creation | As a user, I want to set a monthly budget so I have a target to track against | Brianna, Alex | Core budgeting function |
| 5 | Bill change alerts | As a user, I want to be notified when a recurring bill increases so I can catch unexpected charges | Brianna | Highest-value alert type — drives daily engagement |
| 6 | Overspending alerts | As a user, I want an alert when I'm approaching or over my budget in a category | Brianna | Core habit loop trigger |
| 7 | Spending habit score | As a user, I want a simple score that tells me how my financial habits are trending | Brianna | Differentiator — single metric drives motivation |
| 8 | Secure authentication | As a user, I want MFA so my financial data is protected | All | Non-negotiable for trust and compliance |
| 9 | Bank-level encryption | As a user, I want to know my data is encrypted and secure | All | SOC 2 and ISO 27001 requirement |
| 10 | Mobile-responsive UI | As a user, I want to access the platform on my phone without friction | Brianna | Primary usage channel for B2C persona |

---

## Should Have — Early Releases

High-value features that ship in the first 1–3 releases after launch.

| # | Feature | User story | Persona | Rationale |
|---|---|---|---|---|
| 11 | Month-over-month spending trends | As a user, I want to see how my spending compares to last month | Alex | Drives deeper engagement for power users |
| 12 | Subscription tracker | As a user, I want a list of all my active subscriptions and their costs | Brianna | Directly solves the "forgotten subscription" pain point |
| 13 | Custom budget categories | As a user, I want to create my own spending categories to match my lifestyle | Alex | Increases relevance for power users |
| 14 | Personalized insights feed | As a user, I want tailored tips based on my actual spending patterns | Brianna, Alex | Core personalization feature — increases perceived value |
| 15 | Credit union white-label | As a credit union, I want to offer SpendingHabits under our brand | Chris (CU Partner) | Required for B2B2C revenue channel |
| 16 | Credit union admin dashboard | As a credit union admin, I want to see member adoption and engagement metrics | Chris | Required for partner renewals and ROI reporting |
| 17 | Push notifications | As a user, I want to receive alerts on my phone so I act on them immediately | Brianna | Alerts only drive retention if users see them |
| 18 | Onboarding flow (< 3 min) | As a new user, I want to be set up and seeing my data in under 3 minutes | Brianna | Onboarding length is the #1 predictor of D7 retention |

---

## Could Have — Future Releases

Lower priority features that add value but are not critical to 
core retention or the B2B2C model.

| # | Feature | User story | Persona | Rationale |
|---|---|---|---|---|
| 19 | Savings goal tracker | As a user, I want to set a savings goal and track my progress | Brianna, Alex | Expands product scope beyond spending into saving |
| 20 | Net worth snapshot | As a user, I want to see my assets and liabilities in one view | Alex | Power user feature — not core to primary persona |
| 21 | Data export (CSV) | As a user, I want to export my transaction history for my own records | Alex | Valuable for power users, low retention impact |
| 22 | Spending forecast | As a user, I want a projection of my spending for the rest of the month | Alex | Requires ML modeling — high effort, medium impact |
| 23 | Referral program | As a user, I want to invite friends and earn a reward | Brianna | Growth lever — relevant after product-market fit |
| 24 | In-app financial tips library | As a user, I want access to financial education content inside the app | Brianna | Adds value but not core to retention loop |
| 25 | Dark mode | As a user, I want a dark mode option for the interface | All | UX enhancement — low priority vs. core features |

---

## Won't Have — Explicitly Out of Scope (Phase 1)

These features are documented here to prevent scope creep. They 
may be revisited in future phases.

| # | Feature | Why it's out of scope |
|---|---|---|
| 26 | Investment portfolio tracking | Different user need, different data sources — would dilute core focus |
| 27 | Credit score monitoring | Requires credit bureau integration — high compliance complexity for Phase 1 |
| 28 | Tax preparation tools | Outside core use case — better served by dedicated tax products |
| 29 | Bill payment functionality | Requires banking license or partner — significant regulatory and legal scope |
| 30 | Peer spending comparisons | Privacy risk — requires significant user trust before this feature lands well |
| 31 | Automated savings transfers | Requires deeper banking integration — Phase 3 consideration |
| 32 | Cryptocurrency tracking | Not aligned with core persona's needs or credit union use case |

---

## Feature map by persona

| Feature | Brianna (B2C) | Alex (Power) | Danielle (CU Member) | Chris (CU Partner) |
|---|---|---|---|---|
| Bank sync | ✓ | ✓ | ✓ | — |
| Spending dashboard | ✓ | ✓ | ✓ | — |
| Bill change alerts | ✓ | ✓ | ✓ | — |
| Habit score | ✓ | ✓ | ✓ | — |
| Month-over-month trends | — | ✓ | — | — |
| Custom categories | — | ✓ | — | — |
| White-label | — | — | ✓ | ✓ |
| Admin dashboard | — | — | — | ✓ |
| Push notifications | ✓ | ✓ | ✓ | — |
| Savings goal tracker | ✓ | ✓ | ✓ | — |

---

## Prioritization summary

| Priority | Feature count | Focus |
|---|---|---|
| Must have | 10 | Core habit loop + security + B2C launch |
| Should have | 8 | Retention, personalization + B2B2C channel |
| Could have | 7 | Power users + growth levers |
| Won't have | 7 | Scope protection for Phase 1 |

---

*Jorge S. Ortiz — Product Manager | Chicago, IL*  
*[LinkedIn](https://www.linkedin.com/in/jorge-s-ortiz/) |*  
