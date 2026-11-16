# A/B Experiment Brief, Riverty BU Collection, A Fair Way Forward

## Parameters
| Parameter | Decision |
|---|---|
| Feature under test | Plan Fit Check |
| Persona | quick closers with variable shift income |
| Expected outcome | more plans that fit a low month and are kept |
| Primary success metric | missed payments within 60 days (share of new agreements) |
| Baseline rate | 19.0% (3,846 new agreements per month) |
| Guardrail metric | the agreement rate on started journeys |
| Guardrail boundary | a level below 45% |
| Second guardrail | Kept plans per journey starter must not be lower than control (baseline 37.3%), which catches a result produced by filtering people out instead of better plans. Agent contact within 7 days must stay at 33% or lower (baseline 31.0%). |
| Minimum Detectable Effect | 3 percentage points |
| Sample size per arm | 2.518 |
| Traffic split | 50 / 50, randomized per consumer at journey start |
| Test duration | 6 weeks of enrollment plus 60 days of observation |
| Significance threshold | p < 0.05 |

## Control vs. Variant
- **Control (A):** Today’s journey: no explanation of how income answers are used, the 6-month plan shown first, no fit labels or reasons, and confirmation possible without seeing what happens after a missed payment. This is where the quick closer picks the plan that “looked like the right answer” (N-02) and where missed payments rose from 15.6% to 18.4% after the plan screen change, reaching 19.0% by Month 6.
- **Variant (B):** Plan Fit Check, tested as one bundled feature, with the result attributed to the feature as a whole. Screen 1, “Your Monthly Budget”: normal month, low month and fixed costs, a “why we ask” note under each (this includes the income explainer B2), and an “about the same every month” option. Screen 2, “Plans That Fit You”: the same plan lengths as control, labeled Fits (up to 40% of the remaining low-month budget), Tight (40% to 70%) or Risky (above 70%), each with a one-line reason, best fit first, nothing preselected. Confirmation stays locked until “What if I miss a payment?” has been opened for the selected plan, and resets when the plan changes. Risky plans trigger a second confirmation. Screen 3, “Your Plan Is Set Up”: amount, number of payments, first due date and missed-payment rules. Known limit: the variant also removes the 6-month-first ordering, which alone moved missed payments by about 3 points in Month 4, so the test can’t separate ordering from the fit check.
- **Held constant (isolation check):** Outreach letters, emails and SMS. Eligibility rules and qualifying claims. Claim amounts, plan lengths, fees and interest. The chat assistant, available the same way in both arms. Reminder timing, including any fix for T-207, shipped to both arms or neither. The mobile upload fix (B5) ships to both arms before the test. The income explainer (B2) is part of the variant only and doesn’t ship separately until after the test. Agent scripts and the agent screen. Portal version apart from the variant screens. Pre-registered diagnostics, not decision metrics: share of confirmations on Risky plans, agent contacts about missed payments, and a directional read for shift workers only.

## Hypothesis
> I believe that Plan Fit Check for quick closers with variable shift income will result in more plans that fit a low month and are kept, as measured by a 3 percentage points change in missed payments within 60 days (share of new agreements) within 6 weeks of enrollment plus 60 days of observation. We will protect the agreement rate on started journeys throughout the test.

## Shipping criteria
We will SHIP if missed payments within 60 days drop by at least 3 percentage points at p < 0.05, the agreement rate stays at 45% or higher, kept plans per starter are not lower than control, and agent contact within 7 days stays at 33% or lower. We will ITERATE if missed payments drop significantly but by less than 3 points, or drop by 3 points or more without reaching significance; we do not extend the test, we redesign and retest. We will KILL if missed payments show no improvement or rise, or if the agreement rate falls below 45% or kept plans per starter fall below control, because then the result comes from filtering people out, not from better plans. The read date is fixed at the end of the 60-day observation window, about 15 weeks after launch. Guardrails are checked weekly for harm only, and the test stops early if the variant’s agreement rate falls below 42%.
