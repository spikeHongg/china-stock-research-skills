---
name: strategy-business-transition
description: Analyze an A-share company's strategy, business evolution, and transformation progress. Use this skill when assessing whether a listed company is truly completing a business transition, whether legacy assets still drag results, and which milestones can confirm or falsify management's strategic narrative. All outputs must include accessible source links.
---

# Strategy Business Transition

Analyze how an A-share company moved from its old business model to its current one.

## Non-Negotiable Rules

- Separate `Facts`, `Interpretation`, and `Open Questions`.
- Cite every key statement with an accessible link.
- Prefer official disclosures and regulator sources over media.
- Do not evaluate valuation, trading plan, or detailed order-quality math here.
- Default every intermediate and final output to Simplified Chinese unless the user explicitly requests another language.

## Read First

- `skills/shared/references/source-registry.md`
- `skills/shared/references/citation-standard.md`
- `skills/shared/references/company-disclosure-map.md`
- `skills/shared/references/analysis-pattern-selector.md`
- `skills/shared/references/language-output-standard.md`
- `skills/strategy-business-transition/references/transition-scorecard.md`
- If the company is in a business-model transition, also load `skills/shared/references/business-model-transition-overlay.md`.
- If the company is an IDC or AI-compute transition case, `skills/shared/references/idc-heavy-asset-transition-overlay.md` and `skills/strategy-business-transition/references/idc-transition-markers.md` are optional example overlays.

## When to Use

- Assess a company pivoting from legacy business to a new growth engine.
- Test whether management's transformation narrative is supported by disclosures.
- Identify remaining drag from old assets, old customers, or old liabilities.

## Workflow

1. Pull the prospectus, latest annual report, latest interim report, and recent major announcements.
2. Build a timeline of business-model changes, capital allocation, financing actions, and project milestones.
3. Identify the old business, the new business, and the overlap period.
4. Measure whether revenue, gross profit, assets, and cash flow have migrated with the narrative.
5. Score the transition using the transition scorecard.
6. Output only strategic conclusions and verification points.

## Required Output

- `事实`: business history, segment changes, capital allocation, asset changes, management statements
- `解读`: transition completion level, internal contradictions, likely bottlenecks
- `待验证问题`: what still needs verification and which source should answer it
- `Transition Radar`: capability, customer mix, revenue quality, asset-light progress, cash conversion

## Boundaries

- Do not deep-dive project pipeline execution.
- Do not calculate solvency scorecards here.
- Do not produce target price or entry/exit advice.
