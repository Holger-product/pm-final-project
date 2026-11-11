# Roadmap, PRD & Prototype (Module 4)

## Your strategic anchors
- **Persona (M2), who are you solving for?:** The quick closer: a consumer with variable shift income and one or more claims who wants it done fast and commits without checking fit or consequences.
- **Primary success metric (M3), your leading indicator:** Missed payments within 60 days as a share of agreements, from 19.0% to 15.5% or lower. As the earliest signal, first instalment paid on time (to be requested, not in the data pack).
- **Moment of misery (M2), the specific friction blocking the goal:** She picks the shortest plan because it looks like the right answer, or lets the chat approve one in a minute, then misses the second payment.
- **Guardrail metric (M3), what must not drop or break:** Agreement rate at 44% or higher (secondary: agent contact within 7 days not above 31%).

## Scan the backlog & set a human baseline
- **My instinctive “quick wins” before touching the AI (2 to 3 feature IDs + why):** B2, B5 and B6. B2 is a text change that addresses fear of misuse (N-06, T-206). B5 fixes a known mobile bug that loses 853 documents a month (T-201). B6 looks small and fits shift workers, who miss payments most often (22.5%). B7 also looks like a quick win at first glance, which is exactly why it needs checking against the evidence.

## Audit, override & decide
- **Where did you override the AI? (feature + old vs. new score + why):** B7, from a likely Value 4 to 1: “raise recovery” sounds valuable, but Month 4 already showed that moving a shorter plan up raised missed payments from 15.6% to 18.4%. B6, from Now to Next with the same scores: it’s a quick win, but launching it alongside B3 would blur the A/B test. B3, from a likely Value 4 to 5: it directly targets plans that don’t fit real income, the core of my primary metric.
- **Did the AI over-value a Sales/Eng request your M2 interviews don’t support?:** Yes, B7 is a recovery-driven request, and N-02 shows the opposite effect: the consumer chose the shortest plan because it looked right, and broke it. B8 is the engineering-friendly “AI everywhere” idea, while N-05 shows the chat approves fast without explaining consequences.
- **Did it underweight something your M3 cohort/funnel data strongly supports?:** B3. The data shows the leak comes after commitment, not at it: 83.1% agree at plan review, but 731 of 3,846 plans break within 60 days, most often among variable earners. B1 is also easy to underrate, because multi-claim consumers agree far less often (37.7% and 27.6% vs. 52.1%).

## Generate your interactive roadmap
- **My “Now” lane (this sprint), the 2 to 3 quick wins I’ll build first:** B3 affordability check with missed-payment consequences before confirmation, B2 income explainer, and the upload bug fix from B5. B3 is not a strict quick win (Effort 3), but it’s the feature my hypothesis tests, so it belongs in Now.
- **What I cut, and the “no” I’m protecting the scope from:** B7 and B8. The “no” protects against two pressures: getting recovery up fast by nudging people into short plans, and putting AI everywhere because it looks good on the north star. Both lift SSR and break more plans.
- **Prototype/roadmap screenshot link (paste into your deliverables):** Commit the screenshot to 04-roadmap/, for example as roadmap.png, and paste its GitHub link here.
