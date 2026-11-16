# CLAUDE.md: pm-final-project

Context for Claude Code. This repo is the final project of a Product School Product Management certification, built on an assigned Riverty case. Read this file before working on anything in the repo.

## Working rules

- Write everything in English, including code comments and commit messages.
- Do not use dashes as punctuation in any written text (no em dashes, no en dashes). Hyphens inside compound words are fine.
- All case data is fictional practice data. Every deliverable must keep the disclaimer: "Sample data, illustrative, not Riverty research."
- This repo is **public**. Do not add confidential or internal information, customer data, credentials, internal links, or licensed brand files (see Brand rules).
- Do not invent facts, numbers, names or sources. If something is missing, say so.

## The project in one paragraph

Case: Riverty BU Collection, "A Fair Way Forward." Product concept: Back in Flow. The north star, Self-Service Rate (SSR), counts an instalment plan as resolved when it is created, not when it is kept. When the plan screen started showing the 6 month plan first, SSR rose while missed payments within 60 days rose from 15.6% to 18.4% (19.0% by Month 6). The project targets the quick closer, a consumer with variable shift income who commits fast without checking fit or consequences, with a feature called Plan Fit Check (B3).

## Key decisions (use these numbers)

Module 5 decisions override Module 3 where they differ.

| Item | Value |
|---|---|
| Persona | The quick closer (Mara): variable shift income, one or more claims |
| Feature | Plan Fit Check (B3): budget input, plans labeled Fits / Tight / Risky with a reason, best fit first, confirmation locked until missed payment consequences are opened |
| Primary metric | Missed payments within 60 days as a share of new agreements |
| Baseline | 19.0% (3,846 new agreements per month) |
| MDE / target | 3 percentage points, to 16.0% or lower (Module 3 stated 15.5% as the aspiration) |
| Guardrails | Agreement rate on started journeys at 45% or higher; kept plans per journey starter not below control (37.3%); agent contact within 7 days at 33% or lower |
| Test | 50/50 per consumer, 2,518 agreements per arm, 6 weeks enrollment plus 60 days observation, p < 0.05 two sided |
| GTM | Goal conversion, tier M, three owned channels, no paid media |

## Repo map

```
01-product-thinking/problem-hook.md
02-discovery/competitive-and-journey.md
02-discovery/journey-map.md
03-analytics/hypothesis-and-metrics.md
04-roadmap/roadmap-prd-prototype.md
04-roadmap/prd-and-prototype.md
04-roadmap/prototype.html
05-experimentation/experimentation-plan.md
06-launch/gtm-and-dashboard.md
06-launch/individual-insights.md
06-launch/final-presentation.html   (to be created)
README.md
```

Check that each file exists before relying on it. If one is missing, report it instead of recreating its content from memory.

## Current task: final presentation

Generate `06-launch/final-presentation.html` from the master prompt that will be pasted into the session, with these changes:

1. **Keep** the master prompt's deck structure, slide order, content and output instructions (one valid, self contained HTML5 file, inline CSS, keyboard navigation).
2. **Replace** the master prompt's DESIGN SYSTEM section (Product School navy, orange, fonts) with the **Riverty brand**, using the installed Riverty Brand plugin (`rty-aip-brand-plugin:rty-brand-guidance`) for colors, typography, spacing and component rules.
3. **Do not** use the plugin's presentation or deck builder route if it produces a PowerPoint. The deliverable must be a single HTML file.
4. Cross check the content against the repo files. Where the master prompt and the repo disagree, flag it before building.
5. Name the prototype as `04-roadmap/prototype.html`. Do not invent links.

## Brand rules for a public repo

- Do **not** embed licensed font files (for example GT Ultra Median) in the HTML or commit them to the repo. Reference the brand font by name with a fallback stack.
- Do not commit the Riverty logo or other brand asset files unless their use in a public course repo has been confirmed. Until then, use a text label instead of the logo.
- Use only brand tokens from the plugin. Do not derive new colors.

## Optional follow up

`04-roadmap/prototype.html` was styled by hand from the Riverty Classic Design Guidelines (Confluence, Guidelines V2) because the plugin wasn't available in chat. It can be checked and aligned with the plugin's brand bundle, keeping its behavior and logic unchanged.
