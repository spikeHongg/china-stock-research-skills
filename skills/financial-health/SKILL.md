---
name: financial-health
description: Evaluate the financial health of an A-share company through earnings quality, cash conversion, working capital, leverage, and balance-sheet risk. Use this skill when revenue and profit trends diverge from cash flow, when debt and capex matter, or when impairment and receivable quality are major concerns. All outputs must include accessible source links.
---

# Financial Health

Diagnose whether the company's accounting profit is supported by real cash and a resilient balance sheet.

## Non-Negotiable Rules

- Tie every ratio back to a public filing.
- State the reporting period and whether figures are audited or unaudited when known.
- Separate accounting facts from analytical judgment.
- Do not produce a target price here.
- Default every intermediate and final output to Simplified Chinese unless the user explicitly requests another language.

## Read First

- `skills/shared/references/source-registry.md`
- `skills/shared/references/citation-standard.md`
- `skills/shared/references/financial-kpi-dictionary.md`
- `skills/shared/references/analysis-pattern-selector.md`
- `skills/shared/references/language-output-standard.md`
- `skills/financial-health/references/red-flag-checklist.md`
- If the company is in an asset-heavy ramp, also load `skills/shared/references/asset-heavy-ramp-overlay.md`.
- If the company is an IDC or AI-compute asset-ramp case, `skills/shared/references/idc-heavy-asset-transition-overlay.md` and `skills/financial-health/references/idc-balance-sheet-stress-guide.md` are optional example overlays.

## When to Use

- Revenue is rising but profit or cash flow is weak.
- Working capital is expanding faster than sales.
- Debt, finance cost, guarantees, or capex may threaten the balance sheet.

## Workflow

1. Pull the latest annual, interim, and quarterly reports.
2. Build a three-statement view: income statement, cash flow, balance sheet.
3. Focus on cash conversion, receivables, contract assets, inventory, capex, debt, finance cost, and impairment.
4. Compare current stress points with management explanation.
5. Score liquidity, leverage, and earnings quality.

## Required Output

- `事实`: key line items, ratio set, debt schedule, impairment, working-capital trend
- `解读`: main structural problem, risk transmission path, likely breakpoints
- `待验证问题`: hidden guarantees, collection pace, refinancing schedule, off-balance-sheet items
- `Health Scorecard`: earnings quality, cash conversion, liquidity, leverage, asset quality

## Boundaries

- Do not restate the full industry structure.
- Do not select valuation methods here.
- Do not make a portfolio-allocation call.
