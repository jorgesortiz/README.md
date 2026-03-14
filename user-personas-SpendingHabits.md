# User Personas — SpendingHabits.io

**Author:** Jorge S. Ortiz  
**Last updated:** Q1 2025  

---

## How to use this document

These personas were developed through user interviews, behavioral 
analytics, and market research during the discovery phase. They 
inform feature prioritization, UX decisions, and messaging across 
the product.

---

## Persona 1 — The Overwhelmed Spender (B2C Primary)

**Name:** Brianna L.  
**Age:** 28  
**Occupation:** Marketing Coordinator  
**Income:** $52,000/year  
**Location:** Chicago, IL  

### Who she is
Brianna earns a steady income but never quite knows where her money 
goes by the end of the month. She has 4 streaming subscriptions, 
a gym membership she rarely uses, and three credit cards she 
rotates between. She's tried Mint and YNAB but abandoned both 
within two weeks — too complicated, too much manual work.

### Goals
- Understand where her money is actually going without spending 
  hours categorizing transactions
- Get alerts before she overspends — not after
- Feel in control of her finances without feeling judged or 
  overwhelmed

### Pain points
- Doesn't know her subscriptions have crept up until she checks 
  her bank statement at the end of the month
- Tried budgeting apps before but quit because setup was too complex
- Generic financial advice doesn't feel relevant to her life
- Feels guilty about spending, not empowered to change it

### Behaviors
- Checks her phone 40+ times a day but rarely opens her banking app
- Responds well to friendly, encouraging notifications
- Prefers visual summaries over tables and numbers
- Willing to pay $5–10/month for something that genuinely helps

### What success looks like for Brianna
> "I want to open the app, see exactly where I stand, get a heads 
> up when something's off, and actually feel good about my money 
> for once."

### Design implications
- Onboarding must be under 3 minutes — bank sync, not manual entry
- Dashboard must lead with a single score or visual, not a wall 
  of numbers
- Alerts must be timely, specific, and friendly in tone
- Celebrate wins — when she stays under budget, tell her

---

## Persona 2 — The Budget-Conscious Optimizer (B2C Secondary)

**Name:** Alex R.  
**Age:** 34  
**Occupation:** Project Manager  
**Income:** $78,000/year  
**Location:** Austin, TX  

### Who he is
Alex is financially aware and already tracks his spending — but 
manually, in a spreadsheet. He knows his numbers but wants a 
smarter, automated way to surface patterns he might be missing. 
He's not looking for basic budgeting; he wants actionable insights 
that go deeper than pie charts.

### Goals
- Automate the tracking he currently does manually
- Identify spending patterns he hasn't noticed himself
- Optimize his budget month over month with data, not guesswork

### Pain points
- Manual spreadsheet tracking is time-consuming and error-prone
- Existing apps show him data but don't tell him what to do with it
- Wants more granular insights than most apps provide

### Behaviors
- Power user — will explore all features if they add value
- Reads personal finance content regularly
- Willing to pay $10–15/month for a tool that saves him time
- Likely to refer friends if he finds genuine value

### What success looks like for Alex
> "Show me what I'm missing and save me the two hours I spend 
> every month updating my spreadsheet."

### Design implications
- Offer deeper analytics — trends over time, category comparisons, 
  month-over-month deltas
- Allow custom budget categories and thresholds
- Surface non-obvious insights — "your food delivery spend is up 
  40% vs. last quarter"
- Build in export functionality for users who want their data

---

## Persona 3 — The Credit Union Member (B2B2C)

**Name:** Danielle M.  
**Age:** 42  
**Occupation:** Nurse  
**Income:** $68,000/year  
**Location:** Milwaukee, WI  

### Who she is
Danielle has been a member of her local credit union for 15 years. 
She trusts them with her money but uses a big bank's app for day-
to-day financial tracking because her credit union's digital tools 
are outdated. She would prefer to manage everything in one place 
through an institution she already trusts.

### Goals
- Manage her finances through her credit union — not a third-party 
  app she found on the App Store
- Understand her spending without switching between multiple apps
- Feel supported by her financial institution, not just served by it

### Pain points
- Credit union's existing tools are basic — no insights, no alerts
- Doesn't trust random fintech apps with her banking credentials
- Wants the personal touch of a credit union with the UX of a 
  modern app

### Behaviors
- High trust in her credit union — will adopt tools they recommend
- Less likely to download a random fintech app but will use one 
  her credit union provides
- Wants simplicity over advanced features
- Values security and privacy highly

### What success looks like for Danielle
> "If my credit union offers it and it helps me understand my 
> spending, I'll use it. I already trust them with everything else."

### Design implications
- White-label capability — platform must support credit union 
  branding
- Security messaging must be prominent — members need to know 
  their data is safe
- Onboarding must be seamless with existing credit union account 
  credentials
- Keep UX simple — this persona is not a power user

---

## Persona 4 — The Credit Union Partner (B2B Decision Maker)

**Name:** Chris T.  
**Age:** 51  
**Title:** VP of Member Experience  
**Organization:** Mid-size credit union, 45,000 members  
**Location:** Chicago, IL  

### Who he is
Chris is responsible for member engagement and digital product 
strategy at his credit union. He knows members are using fintech 
apps instead of the credit union's tools — and he wants to fix 
that. He's evaluated several vendors but hasn't found one that 
fits the credit union model and can move fast.

### Goals
- Offer members a modern financial wellness tool without building 
  one from scratch
- Increase member engagement with the credit union's digital 
  ecosystem
- Demonstrate ROI to leadership within 12 months of launch

### Pain points
- Building in-house is too slow and expensive
- Most fintech tools aren't designed for the credit union 
  relationship model
- Compliance and security reviews slow down vendor evaluations
- Members are disengaging from credit union digital tools

### What success looks like for Chris
> "I need something I can put in front of our members in 6 months 
> that makes them feel like we're investing in their financial 
> health — not just their accounts."

### Design implications
- White-label and co-branding must be a core capability, not an 
  add-on
- Security certifications (SOC 2 Type II, ISO 27001) must be 
  documented and shareable for compliance review
- Reporting dashboard for credit union admins — member engagement 
  metrics, adoption rates
- Implementation timeline must be fast — 90 days or less to deploy

---

## Persona comparison

| Dimension | Brianna (B2C) | Alex (B2C Power) | Danielle (CU Member) | Chris (CU Partner) |
|---|---|---|---|---|
| Primary motivation | Clarity & control | Optimization | Trust & convenience | Member engagement |
| Tech savviness | Low–Medium | High | Low–Medium | Medium |
| Willingness to pay | $5–10/mo | $10–15/mo | Via CU membership | B2B contract |
| Key feature need | Simple alerts & score | Deep analytics | White-label, simple UX | Admin dashboard, compliance docs |
| Biggest risk if we fail them | Churns within 30 days | Switches to competitor | Never adopts | Doesn't renew contract |
| Involvement in UAT | Medium | High | Low | High |

---

*Jorge S. Ortiz — Product Manager | Chicago, IL*  
*[LinkedIn](https://www.linkedin.com/in/jorge-s-ortiz/) | 
[Portfolio](https://jorgesortiz.notion.site/Jorge-S-Ortiz-2458c3cb325a80cbae1bfd8a6fe293fc)*
