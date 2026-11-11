# PRD & Prototype Sprint (Module 4)

## Pick & scope with MoSCoW
- **The “Now” feature I’m scoping (name + one-line core description):** Plan Fit Check (B3): before choosing a plan, the consumer enters a typical monthly income and fixed costs, sees which plans fit, and reads what happens after a missed payment before confirming.
- **My finalized Must-Haves (after overriding the AI):** Short affordability input (income in a normal month, income in a low month, fixed costs) with a plain “why we ask” note.
Plan options labeled Fits, Tight or Risky against the remaining budget, best fit first.
Missed-payment consequences shown for the selected plan before confirmation.
A one-line reason for every label.
A confirmation summary with amount, number of payments, first due date and missed-payment rules.
- **What I demoted from Must → Should/Won’t, and why:** Pay day date (B6) to Won’t Have: it’s a separate test, and including it would blur the read on B3. Document upload to Won’t Have: B5 is fixed separately, and the prototype doesn’t need it. Saving answers when going back (T-204) to Should Have: important for the live product, not needed to prove the core idea.

## Generate your Simplified PRD
- **One thing my PRD makes explicit that a vague brief would have missed:** That confirmation is gated: the consumer can’t commit until she has seen what happens after a missed payment. A vague brief like “add an affordability check” would have built the calculator and skipped the moment where Mara actually fails.

## Prompt-to-prototype sprint
- **Where did the prototype reveal a gap in my PRD logic? (what I had to update):** Three gaps. First, the gate: the PRD said confirm stays disabled until the consequences have been opened, but not what happens when she switches plans afterwards. I decided the gate resets per plan, so she always sees the consequences for the plan she actually confirms. Second, the low-month field: the PRD made it required, which is pointless for people with a fixed salary, so I added an “about the same every month” option. Third, the PRD never defined fees, interest or the first due date, so the prototype assumes no fees and a first payment 14 days out, and the missed-payment text is placeholder copy “to be confirmed by Legal.”
- **My prototype: save Claude's HTML as prototype.html in 04-roadmap/, open it in your browser, and add a screenshot:** https://github.com/Holger-product/pm-final-project/blob/main/04-roadmap/prototype.jpg
