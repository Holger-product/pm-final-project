# Hypothesis and metrics: Back in Flow

**Case:** Riverty BU Collection, A Fair Way Forward
**Module:** 3, data-backed product hypothesis
**Persona:** The quick closer (Mara)

> Sample data, illustrative, not Riverty research. All quotes, tickets and figures come from the fictional cohort 2 data pack. Estimates and calculations of my own are labeled as such.

## Hypothesis

Based on consumers like N-02 who pick the plan that "looked like the right answer" and miss the second payment, and missed payments rising from 15.6% to 18.4% after the plan screen put the 6-month plan first (19.0% by Month 6), I believe that **showing affordability fit and missed-payment consequences before confirmation** for **quick closers with variable income** will result in **more plans being kept**, as measured by a drop in **missed payments within 60 days from 19.0% to 15.5% or lower**. I will protect the **agreement rate at 44% or higher** and will make a go/no-go decision after **6 weeks of enrollment and 60 days of observation**.

## Starting point from Modules 1 and 2

| Field | Content |
|---|---|
| Role | Consumer with one or more open claims and variable shift income who opens the portal on her phone after a reminder and wants it done fast. |
| Goal | Agree to a monthly plan she can actually keep, so she can stop worrying and get on with her life. |
| Friction | Picks the shortest plan because it looks right, or lets the chat approve one in a minute, without knowing what happens after a missed payment. Misses the second payment. |
| Workaround | Guesses her income and takes the fastest path to a yes. When the plan breaks, she calls an agent who asks again for everything she entered online. |
| Problem Hook (M1) | We must solve a north star that rewards broken plans, with SSR rising while one in five new plans misses a payment within 60 days, by addressing consumers who are pushed to agree quickly instead of agreeing to a plan they understand and can actually keep. |
| Value Proposition (M1) | For consumers with one or more open claims and irregular income, we will show exactly what they owe across all claims and what happens if something goes wrong, before they commit, so they choose a plan they can keep. |

## Evidence reconciliation

### 1. Where the experience drops (funnel.csv)

**Verdict: nuance, with one partial contradiction.**

| Step | People | % of previous step |
|---|---|---|
| Consumers receiving outreach | 100,000 | 100.0% |
| Entered portal | 38,000 | 38.0% |
| Started instalment journey | 8,360 | 22.0% |
| Reached affordability questions | 7,364 | 88.1% |
| Reached income document step | 5,943 | 80.7% |
| Reached plan review | 4,630 | 77.9% |
| Agreement created | 3,846 | 83.1% |
| No missed payment within 60 days | 3,115 | 81.0% |

- Largest loss inside the journey: document step to plan review, 1,313 people. T-201 reports 853 journeys where the document never arrived, likely a large share, though the pack doesn't confirm the overlap.
- The commitment moment is not the leak: 83.1% agree at plan review. The leak comes after agreement: 731 plans break within 60 days. This confirms the quick closer pattern.
- Contradiction in volume: the largest loss happens before the journey starts (38,000 to 8,360). This hypothesis does not address it.
- **Metric to request:** exit reasons or page behavior between portal entry and journey start.

### 2. What changed over time (monthly_trend.csv)

**Verdict: confirms the core of the hook.**

| Month | Agreement rate | Agent contact 7d | Missed payment 60d | SSR | First plan option |
|---|---|---|---|---|---|
| 1 | 43.1% | 33.4% | 15.2% | 31.1% | 12 months |
| 2 | 43.8% | 33.0% | 15.9% | 31.8% | 12 months |
| 3 | 44.2% | 32.6% | 15.6% | 32.3% | 12 months |
| 4 | 45.6% | 31.9% | 18.4% | 33.8% | 6 months |
| 5 | 46.3% | 31.4% | 18.8% | 34.4% | 6 months |
| 6 | 46.0% | 31.0% | 19.0% | 34.7% | 6 months |

- Showing the 6-month plan first lifted agreement rate and SSR while missed payments jumped. The north star improved while outcomes got worse.
- Nuance: agent contact fell steadily before Month 4 as well, so the phone workaround is not growing. The pain shifted from calling to breaking.
- **Metric to request:** maturity date of each month's 60-day cohort, since Months 5 and 6 may not be fully observed.

### 3. Which users feel it (segments.csv)

**Verdict: confirms the persona, with nuance.**

| Segment | Agreement rate | Agent contact 7d | Missed payment 60d |
|---|---|---|---|
| Variable or shift income | 41.6% | 32.7% | 22.5% |
| Fixed salary | 48.1% | 30.2% | 17.4% |
| One open claim | 52.1% | 25.6% | 18.1% |
| Two open claims | 37.7% | 40.0% | 21.4% |
| Three or more open claims | 27.6% | 43.0% | 21.2% |
| Used chat assistant | 53.3% | 27.1% | 21.6% |
| Did not use chat | 44.4% | 31.9% | 18.3% |

- Variable earners carry the highest missed payment rate: the quick closer.
- Multi-claim consumers show low agreement and high agent contact, with median instalments of €88.73 (two claims) and €114.84 (three or more) vs. €58.72 (one claim). That fits the cautious checker plus an affordability issue.
- Chat users confirm the speed trap: more agreements, more broken plans. This is a correlation, not proof of cause.
- Surprise: purchased and client portfolios perform almost identically (missed payments 19.4% vs. 18.8%), despite T-203.
- **Metric to request:** cross-tab of income pattern by number of claims, since Mara sits in both groups.

## Hypothesis components

| Component | Definition |
|---|---|
| Qualitative evidence | "I picked the plan with the lowest number of months because it looked like the right answer. The amount was too high and I missed the second payment." (N-02). Backed by N-05: the chat approved a plan in a minute without explaining late payments. |
| Quantitative evidence | Missed payments within 60 days rose from 15.6% to 18.4% after the plan screen change, reaching 19.0% (731 of 3,846 agreements) by Month 6. Variable earners miss most at 22.5%. |
| Problem | Consumers commit without checking whether the amount fits their real income or understanding what happens after a missed payment, so the plans counted as resolved are the ones that break. |
| Strategic outcome | More consumers choose a plan that fits and keep paying. Revenue: cash actually recovered over the plan's lifetime. Retention: plans kept to the end. Churn: fewer broken plans returning to agents. Also protects client retention (N-10). |
| Primary success metric | Missed payments within 60 days as a share of agreements. Baseline 19.0%, target 15.5% or lower (pre-change level). Earlier signal to request: first instalment paid on time. |
| Guardrail metric | Agreement rate must stay at 44% or higher. Secondary: agent contact within 7 days must not rise above 31%. |
| Decision window | A/B test across all journey starters: 6 weeks enrollment, then 60 days observation, decision about 3.5 months after launch. |

## Decision rules

- **Go:** missed payments at least 2 percentage points lower than control, agreement rate at 44% or higher.
- **Early kill check after 30 days:** agreement rate below 42% means stop and rework.
- **Sample size (my estimate):** detecting 19.0% vs. 15.5% needs about 1,800 agreements per variant, reached in roughly 4 to 6 weeks at about 3,800 agreements per month.

## Open questions

1. Why do 78% of portal visitors never start a journey?
2. How much of the document-step loss is caused by the T-201 upload bug?
3. Are the 60-day figures for Months 5 and 6 fully mature?
4. How do variable income and multiple claims interact?
5. Does the chat cause broken plans, or do riskier consumers choose the chat?

## Key learning

My Module 1 hook said the north star rewards broken plans. The data confirmed that and narrowed it: the leak isn't at commitment (83% agree at plan review) but after it, and it's strongest for variable earners, so my hypothesis targets plans kept, not plans created.
