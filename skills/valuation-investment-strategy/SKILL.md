---
name: valuation-investment-strategy
description: Convert a source-backed A-share research view into valuation scenarios and an investment plan. Use this skill after strategy, business, financial, industry, and risk work is complete. Choose methods that fit the business model and explain assumptions with accessible source links.
---

# Valuation Investment Strategy

Build scenario-based valuation only after the factual base is complete.

## Non-Negotiable Rules

- Do not invent inputs when public evidence is missing.
- Tie every key assumption to a public source or a clearly labeled analytical assumption.
- Use scenario analysis instead of false precision.
- Keep facts separate from judgment and trading plan.
- Default every intermediate and final output to Simplified Chinese unless the user explicitly requests another language.

## Read First

- `skills/shared/references/citation-standard.md`
- `skills/shared/references/research-output-template.md`
- `skills/shared/references/analysis-pattern-selector.md`
- `skills/shared/references/language-output-standard.md`
- `skills/shared/templates/valuation-scenario-table.md`
- `skills/valuation-investment-strategy/references/method-selection.md`
- If the company is in a business-model transition or asset-heavy ramp, also load the matching shared overlay.
- If the company is an IDC or AI-compute transition case, `skills/shared/references/idc-heavy-asset-transition-overlay.md` and `skills/valuation-investment-strategy/references/idc-valuation-overlays.md` are optional example overlays.

## When to Use

- A full company view already exists and now needs a valuation frame.
- The company is in transition and simple PE is not enough.
- The report needs bear, base, and bull cases with explicit assumptions.

## Workflow

1. Pull outputs from the previous five skills.
2. Select the right method: peer multiple, SOTP, EV/EBITDA, PB, DCF, or asset-based.
3. Define a scenario table with revenue, margin, capex, utilization, and balance-sheet assumptions.
4. Link every assumption to the supporting source or mark it as an analytical estimate.
5. Produce a value range, thesis checkpoints, and invalidation triggers.

## Required Output

- `事实`: valuation-relevant facts, peer set, asset base, financing constraints
- `解读`: which method is most suitable and why
- `待验证问题`: missing occupancy, margin, capex, or disposal assumptions
- `Scenario Table`: bear, base, bull with linked assumptions
- `Investment Plan`: build condition, stop condition, and thesis-confirmation milestones

## Boundaries

- Do not rebuild the raw company fact base from scratch.
- Do not present unsupported precision such as exact fair value without ranges.
- Do not ignore risk and balance-sheet constraints.
