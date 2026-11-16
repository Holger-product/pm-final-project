# Individual insights

**Case:** Riverty BU Collection, A Fair Way Forward
**Product concept:** Back in Flow, Plan Fit Check
**Author:** Holger, Riverty cohort 2

> Sample data, illustrative, not Riverty research. All quotes, tickets and figures come from the fictional cohort 2 data pack.

## Friction points

- **Pace over reflection.** The course format left little room to discuss and challenge conclusions with others. Most of the real work was making sure the AI output stayed honest to the data, rather than producing more of it.
- **Metrics that look right.** The hardest parameter in every module was the metric, because each candidate could be improved in a way that didn't help the consumer.
- **Inputs decide outputs.** In Module 2 the AI synthesis missed the north star trap entirely, simply because the Month 4 data wasn't part of its input. Curating inputs turned out to be as important as reviewing outputs.
- **Building exposed gaps.** The prototype revealed decisions my PRD never made, for example what happens to the consequence check when someone switches plans after opening it.

## The aha moment

The same trap kept reappearing in different forms:

1. **The north star.** SSR counts a plan as resolved when it's created, not when it's kept. Showing the 6 month plan first lifted SSR while missed payments rose from 15.6% to 18.4%.
2. **The chat.** Chat users agree more often (53.3% vs. 44.4%) but also miss more payments (21.6% vs. 18.3%).
3. **My own experiment metric.** Missed payments as a share of agreements could have hit the full target purely by filtering risky consumers out, while staying within a loose agreement rate guardrail.

Every good metric in this case needed a second number to keep it honest. That's why the final experiment protects kept plans per journey starter, a metric that can't be gamed in either direction.

## Key takeaways

1. **In this case, speed and motivation were the trap, and clarity was the value.** Gamified badges and a faster chat would have made the problem worse. What Mara needed was certainty before committing.
2. **AI was strongest at synthesis and execution, weakest at judgment.** It structured evidence and built the prototype quickly, but it didn't notice when a metric could be gamed or when a correlation was presented as a cause. That judgment stayed with me.
3. **Prototyping before handoff pays off.** A working model surfaced logic gaps in minutes that would otherwise have reached design and engineering.

## What I would do next

1. Run the A/B test as specified in `05-experimentation/experimentation-plan.md`.
2. Add a third arm that only reverts the plan ordering, to separate the ordering effect from the fit check itself.
3. Test the pay day date (B6) as a follow-up experiment.
4. Shadow collection agents to find the workarounds no dashboard shows.
5. Request the missing metrics: first instalment paid on time, exit reasons before journey start, and a cross tab of income pattern by number of claims.
