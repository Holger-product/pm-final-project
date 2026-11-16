# GTM Launch Plan, Riverty BU Collection, A Fair Way Forward

| Field | Value |
|---|---|
| Feature | Plan Fit Check (B3): affordability input, plans labeled Fits, Tight or Risky with a reason, best fit first, and confirmation locked until “What if I miss a payment?” has been opened for the selected plan. |
| Goal | Conversion |
| Launch tier | M, Targeted |

## Goal & Audience
- **Goal:** Conversion, The feature lives inside the existing journey, and consumers reach it through outreach that already exists, so awareness isn’t the problem. The goal is converting journey starters into plans that are actually kept, which is also what the M5 test measures.
- **Target audience:** Primary: consumers in the German pilot who start an instalment journey, 8,360 per month (gtm_audience.csv), with quick closers on variable or shift income as the focus. Assumption: the data pack’s monthly volume represents the German pilot segment, since the brief leaves it open. Secondary: about 10 collection agents in the pilot team (assumption, based on roughly 500 agent hours a month of journey-related contacts), client account managers, and legal and compliance, because they have to explain, report and approve what consumers see.

## Launch Tier
- **M, Targeted**, One journey in one market, about 8,360 starters a month. No new revenue line, but recovery over the plan’s lifetime and client reporting are directly affected, with about 115 fewer broken plans a month at the MDE. Silence is risky on the internal and client side: agents who can’t explain a Risky label create more calls, and clients who see agreement numbers shift without context complain about their reporting (N-10). For consumers this is a release they meet inside the journey, with no marketing, since marketing to people in debt would be inappropriate. For agents, account managers and compliance it’s a launch.

## Channels
1. **Owned: The portal journey itself, where the quick closer already is after the reminder, so the feature reaches her at the moment of misery without any extra message.**
2. **Owned: The existing outreach letters, emails and SMS, with one added line after the test: “See which plan fits your budget before you agree.” Unchanged during the A/B test to keep the arms isolated.**
3. **Owned: Agent team briefings and the agent workspace, plus client account manager reviews for clients, reaching each group through routines that already exist. No paid channels, because paid media aimed at consumers in debt would conflict with the fairness guardrail.**

## Enablement & Assets
Agents: a one-page explainer of how Fits, Tight and Risky are calculated, an FAQ for “why was my plan labeled Risky?” and “what happens if I miss a payment?”, and a 30-minute briefing. Client account managers: a one-pager on test design, metrics and guardrails, so clients can read changes in their reporting. Legal and compliance: the final missed-payment text replacing the prototype placeholder, and documentation of how labels are calculated, so recommendations are explainable (N-12). AI drafts the FAQs, one-pagers and result summaries, always reviewed by a person. AI is not used for the final legal text, for any decision about an individual consumer without human review, or for client conversations.

## Ownership, Budget & Timeline
- **Ownership & budget:** Holger (Senior PM) owns the launch plan, the A/B test and post-launch metrics. [Name], legal counsel for collections Germany, owns the missed-payment text and explainability documentation. [Name], pilot team lead, owns the agent briefing and FAQ. [Name], client account manager, owns the client one-pager and client conversations. [Name], product analyst, owns instrumentation and the test read. No media spend. Costs extra: legal review time, about 10 agent hours for briefings, and analytics work for two metrics not yet tracked, kept plans per starter and first instalment paid on time. Asset gap: no approved missed-payment wording exists yet, and the variant can’t launch without it.
- **Timeline:** Before Phase 1 (4 weeks): legal text approved, instrumentation live, upload fix (B5) shipped to everyone, agents briefed, client account managers informed. Phase 1, beta (weeks 1 to 15): the A/B test, 6 weeks of enrollment plus 60 days of observation, with weekly guardrail checks. Phase 2, launch moment (week 16, only after SHIP): Plan Fit Check for 100% of the German pilot, the outreach line added, agents and account managers live with results. Phase 3, post-launch (weeks 16 to 28): monitor kept plans and agent contacts, start the pay day date test (B6), and assess extension to purchased portfolios and other markets.

## Success Metrics
- **Metrics:** Missed payments within 60 days from 19.0% to 16.0% or lower. Kept plans per journey starter at least at the baseline of 37.3%, aiming higher. Agreement rate on started journeys at 45% or higher.
- **Bad signal to watch for:** Missed payments fall while the agreement rate falls too, meaning people are filtered out rather than helped. A high share of Risky plans confirmed anyway, meaning consumers don’t trust or understand the labels. More agent calls asking “why is my plan Risky?”, meaning the explainer copy isn’t landing.
- **Likely post-launch decision:** Iterate, triggered by a positive result below 3 points or a high rate of Risky confirmations. Double-down if the test hits SHIP: roll out to the full pilot, add the pay day date test, and extend to purchased portfolios. Deprioritize if the filtering pattern appears.
