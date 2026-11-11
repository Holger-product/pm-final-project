# Feature Roadmap, Module 4 · BU Collection

**Scenario:** Riverty BU Collection, A Fair Way Forward

**Team:** [your assumed team size]

## Strategic anchors
- **Persona:** The quick closer: a consumer with variable shift income and one or more claims who wants it done fast and commits without checking fit or consequences.
- **Primary metric:** Missed payments within 60 days as a share of agreements: from 19.0% to 15.5% or lower.
- **Moment of misery:** She picks the shortest plan because it looks like the right answer, or lets the chat approve one in a minute, then misses the second payment.
- **Guardrail:** Agreement rate at 44% or higher (secondary: agent contact within 7 days not above 31%).

## Scoring
| Feature | Value | Effort | Quadrant | Decision | Rationale |
|---|---|---|---|---|---|
| B1 One plan for several open claims | 4 | 5 | Major Project | Next | Multi-claim agreement is only 37.7% (2 claims) and 27.6% (3+), but combining claims across clients needs legal and client alignment. |
| B2 Plain explainer for why income is asked | 3 | 1 | Fill-In | Now | Cheap trust fix for N-06 and T-206; lifts completion more than kept plans, so Value stays at 3. |
| B3 Affordability check before the plan options | 5 | 3 | Major Project | Now | The core of the hypothesis: plans that fit real income, aimed at variable earners missing 22.5%. Scope includes showing missed-payment consequences before confirmation. |
| B4 Handoff summary for the agent | 3 | 3 | Time Sinker | Next | Removes repeated checks (N-08, T-205) and protects the agent contact guardrail, but doesn’t move missed payments directly. |
| B5 Mobile photo upload, or skip document under a set amount | 3 | 2 | Fill-In | Now | Fix the upload bug now (853 documents never arrived). Hold the “skip document” part until B3 is live, so no one gets a plan without an affordability check. |
| B6 Pick a payment date that matches pay day | 4 | 2 | Quick Win | Next | Strong fit for shift earners, but launching it with B3 would blur the test. Run it as a second test after the first read. |
| B7 Show the shortest plan first to raise recovery | 1 | 1 | Fill-In | Cut | Month 4 already showed that moving a shorter plan up raised missed payments from 15.6% to 18.4%. This would make the problem worse and conflicts with the fairness guardrail. |
| B8 Chat assistant on every portal page | 2 | 3 | Time Sinker | Cut | Chat users miss more payments (21.6% vs. 18.3%), and “every page” is placement, not a solution. Revisit as a chat at plan review that explains consequences. |

## Roadmap
### NOW, this sprint
- **B2 Plain explainer for why income is asked**, Cheap trust fix for N-06 and T-206; lifts completion more than kept plans, so Value stays at 3.
- **B3 Affordability check before the plan options**, The core of the hypothesis: plans that fit real income, aimed at variable earners missing 22.5%. Scope includes showing missed-payment consequences before confirmation.
- **B5 Mobile photo upload, or skip document under a set amount**, Fix the upload bug now (853 documents never arrived). Hold the “skip document” part until B3 is live, so no one gets a plan without an affordability check.

### NEXT, the following sprints
- **B1 One plan for several open claims**, Multi-claim agreement is only 37.7% (2 claims) and 27.6% (3+), but combining claims across clients needs legal and client alignment.
- **B4 Handoff summary for the agent**, Removes repeated checks (N-08, T-205) and protects the agent contact guardrail, but doesn’t move missed payments directly.
- **B6 Pick a payment date that matches pay day**, Strong fit for shift earners, but launching it with B3 would blur the test. Run it as a second test after the first read.

### LATER, backlog
- _(none)_

### ✂ Cut List
- **B7 Show the shortest plan first to raise recovery**, Month 4 already showed that moving a shorter plan up raised missed payments from 15.6% to 18.4%. This would make the problem worse and conflicts with the fairness guardrail.
- **B8 Chat assistant on every portal page**, Chat users miss more payments (21.6% vs. 18.3%), and “every page” is placement, not a solution. Revisit as a chat at plan review that explains consequences.
