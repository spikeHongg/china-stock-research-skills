---
name: business-decomposition-order-quality
description: Break down an A-share company's business model into segments, customers, products, regions, projects, and order pipeline quality. Use this skill when testing whether reported growth is supported by real delivery, healthy customers, and cash collection. All outputs must include accessible source links.
---

# Business Decomposition Order Quality

Dissect the company's growth engine and test the quality of its orders.

## Non-Negotiable Rules

- Attach an accessible source link to every major contract, order, customer, region, and product claim.
- Distinguish signed orders, in-hand backlog, delivered revenue, and collected cash.
- Mark unsupported customer or pricing claims as open questions.
- Do not do final valuation here.
- Default every intermediate and final output to Simplified Chinese unless the user explicitly requests another language.

## Read First

- `skills/shared/references/source-registry.md`
- `skills/shared/references/citation-standard.md`
- `skills/shared/references/financial-kpi-dictionary.md`
- `skills/shared/references/analysis-pattern-selector.md`
- `skills/shared/references/language-output-standard.md`
- `skills/business-decomposition-order-quality/references/order-quality-checklist.md`
- If the company is project or order-driven, also load `skills/shared/references/project-order-business-overlay.md`.
- If the company is an IDC or AI-compute project case, `skills/shared/references/idc-heavy-asset-transition-overlay.md` and `skills/business-decomposition-order-quality/references/idc-order-ledger-guide.md` are optional example overlays.

## When to Use

- Analyze contract-driven or project-driven growth.
- Test whether a new growth business is high quality or just high headline revenue.
- Review customer concentration, order cancellation, delayed execution, and region mix.

## Workflow

1. Collect all major order announcements and recent reports.
2. Build a table of products, projects, customers, regions, contract value, term, delivery stage, and revenue-recognition method.
3. Compare order growth with revenue growth, gross margin, receivables, contract assets, and cash collection.
4. Review project changes, cancellations, and contract revisions for signal value.
5. Summarize which growth is recurring, which is one-off, and which may not convert.

## Required Output

- `事实`: segment mix, customer mix, project list, order pipeline, revenue-recognition method
- `解读`: order quality, concentration risk, execution risk, delivery visibility
- `待验证问题`: unknown pricing, milestone schedule, payment terms, or customer dependence
- `Pipeline Table`: order amount, stage, expected conversion, source
- Use `skills/shared/templates/idc-project-ledger.md` only for IDC or operator-facing project portfolios.

## Boundaries

- Do not do a full solvency diagnosis.
- Do not build the final industry moat conclusion.
- Do not issue buy/sell recommendations.
