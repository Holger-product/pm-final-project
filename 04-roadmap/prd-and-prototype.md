# Plan Fit Check, Simplified PRD (Riverty BU Collection, A Fair Way Forward)

**Scenario:** Riverty BU Collection, A Fair Way Forward

**Author:** Me · **Status:** Draft · **Target:** High-Fidelity Prototype · **Persona:** The quick closer: a consumer with variable shift income and one or more claims who wants it done fast and commits without checking fit or consequences.

## 1. The Big Picture
- **Vision:** Every consumer leaves the portal with a plan that fits their real income and knows what happens if something goes wrong.
- **Press release:** Starting today, consumers who set up an instalment plan with Riverty no longer have to guess which plan is the “right answer.” Plan Fit Check asks three short questions about a normal month, a low month and fixed costs, explains why, and then shows which plans fit, which are tight, and which are risky, with a clear reason for each.

Before anyone confirms, they see exactly what happens if a payment is missed. For consumers like Mara, who works shifts and used to pick the shortest plan only to miss the second payment, that means agreeing to something she can keep and then getting on with her life.
- **Success metric:** Missed payments within 60 days as a share of agreements, from 19.0% to 15.5% or lower.
- **Guardrail:** Agreement rate at 44% or higher.

## 2. The Details
### User stories
- As a consumer with variable income, I want to enter both a normal and a low month, so that the plans reflect what I can pay when money is tight. Acceptance: the lower value drives the labels, and people with a steady income can mark it as the same every month.
- As a consumer in a hurry, I want to see at a glance which plans fit my budget, so that I don’t pick a plan just because it looks like the right answer. Acceptance: every plan shows a label and a one-line reason, best fit first.
- As a consumer about to commit, I want to know what happens if I miss a payment, so that I’m not surprised later. Acceptance: the confirm button stays disabled until the consequences for the selected plan have been opened.
### Screens to build
- 1. Entry point, “Your Monthly Budget”: three number fields (normal month, low month, fixed costs), a “why we ask” note under each, a “same every month” option, the open amount, and a Show my plans button.
- 2. Feature core, “Plans That Fit You”: plan options (3, 6, 12 and 18 months) with monthly amount, Fits / Tight / Risky label, one-line reason, budget bar, and an expandable “What if I miss a payment?” panel for the selected plan.
- 3. Success, “Your Plan Is Set Up”: summary of monthly amount, number of payments, first due date and fit, missed-payment rules, and a “Talk to an agent” link.
### Functional requirements
- The budget form has no more than three fields and can be completed in under 60 seconds.
- Remaining budget is calculated as the low-month income minus fixed costs.
- Each plan is labeled Fits if the instalment is up to 40% of the remaining budget, Tight from 40% to 70%, and Risky above 70% (prototype thresholds, not policy).
- Plans are sorted best fit first, shortest first within the same label, and no plan is preselected.
- Every label shows a reason, for example “€100 is 33% of what’s left after fixed costs.”
- The confirm button stays disabled until the missed-payment panel has been opened for the currently selected plan. Switching plans resets this.
- Choosing a Risky plan triggers a second confirmation that repeats the reason.
- The confirmation screen shows monthly amount, number of payments, first due date and missed-payment rules.
### Smart behaviors (Situation → Outcome)
- If remaining budget is zero or negative → no plan is labeled Fits, and a “talk to an agent” path is shown.
- If all plans are Risky → the longest plan is listed first, with the agent option highlighted.
- If low-month income is higher than normal-month income → show a gentle prompt to check the numbers, and allow continuing.
- If income is marked as the same every month → the low-month field is filled from the normal month.
- If the consumer switches plans after opening the panel → the confirm button locks again until the new plan’s panel is opened.
- If the consumer selects a Risky plan → show a second confirmation with the reason.
- If the consumer goes back to the budget screen → their answers are kept.
### Technical constraints
- One self-contained HTML file with inline CSS and plain JavaScript. No external APIs, no login, no database, no network calls, no data stored or sent anywhere. The open amount (€1,200) is sample data, plans have no fees or interest, and the first payment is due 14 days after confirmation. The missed-payment text is placeholder copy marked “sample text, to be confirmed by Legal.” Visual style follows the Riverty Classic Design Guidelines (Guidelines V2).

## 3. The Logistics
### Features out
- One plan for several claims (B1), pay day date picker (B6), document upload or skip (B5), chat assistant (B8), agent handoff summary (B4), real payment processing, real credit or affordability checks.
### Edge cases & safety guard
- Empty fields, non-numeric input, negative numbers, values above €20,000 a month, and fixed costs higher than income all show a clear inline message or the agent path instead of a misleading result. The prototype must never preselect the shortest or highest instalment, never present placeholder legal text as real policy, never store or send entered data, and never use shaming or threatening language.
### Decision log
- 1 Risky plans are warned about, not blocked: consumers keep the choice, which respects their autonomy and the fairness guardrail.
- 2 The pay day picker is excluded from this version, so the A/B test isolates the effect of the fit check and the consequence panel.
### Evals
- Accuracy: 100% of plans in ten prepared test cases receive the correct label according to the 40% and 70% thresholds.
- Time on task: median under 2 minutes from first input to confirmation in a hallway test.
- Safety: in 100% of confirmations, the missed-payment panel for the confirmed plan was opened first, and no plan was ever preselected.

## MoSCoW scope
- **Must:** Affordability input with three fields and a “why we ask” note; Option to mark income as about the same every month; Plan labels Fits, Tight, Risky against remaining budget; Best-fitting plan first, no plan preselected; Missed-payment consequences shown before confirmation; One-line reason for every label; Confirmation summary with amount, payments, first due date and missed-payment rules
- **Should:** Answers kept when going back (T-204); Plain hint on how to reach an agent if no plan fits; Second confirmation when a Risky plan is chosen
- **Could:** Visual budget bar per plan; View of all open claims (read-only); Simple language toggle
- **Won't (now):** One plan for several claims (B1); Pay day date picker (B6); Document upload or skip (B5); Chat assistant (B8); Agent handoff summary (B4); Real payment processing or credit checks

