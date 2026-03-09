---
name: risk-warning-catalysts
description: Build a source-backed monitoring system for risk signals and catalysts in an A-share company. Use this skill when turning static research into an update process covering orders, financing, governance, policy, operations, and sentiment. All outputs must include accessible source links.
---

# Risk Warning Catalysts

Convert research into a live monitoring framework.

## Non-Negotiable Rules

- Every risk and catalyst must point to a public source and a monitorable trigger.
- Distinguish confirmed events from watch items.
- Use thresholds where possible, not vague language.
- Do not turn monitoring points into valuation conclusions here.
- Default every intermediate and final output to Simplified Chinese unless the user explicitly requests another language.

## Read First

- `skills/shared/references/source-registry.md`
- `skills/shared/references/citation-standard.md`
- `skills/shared/references/analysis-pattern-selector.md`
- `skills/shared/references/language-output-standard.md`
- `skills/shared/templates/catalyst-calendar.md`
- `skills/risk-warning-catalysts/references/monitoring-dashboard.md`
- If the company is project-driven or asset-ramp sensitive, also load the matching shared overlay.
- If the company is an IDC or AI-compute case, `skills/shared/references/idc-heavy-asset-transition-overlay.md` and `skills/risk-warning-catalysts/references/idc-monitoring-indicators.md` are optional example overlays.

## When to Use

- Build a watchlist after a deep-dive report.
- Track whether the thesis is improving or deteriorating.
- Prepare a monthly or event-driven update process.

## Workflow

1. Pull the latest announcements and identify what changed since the last report.
2. Map risks by category: execution, finance, governance, policy, customer, technology, litigation.
3. Map catalysts by category: orders, policy, financing, asset disposals, utilization, margin improvement.
4. Attach a threshold, expected evidence source, and review frequency to each item.
5. Build a monthly dashboard and catalyst calendar.

## Required Output

- `事实`: confirmed risks, confirmed catalysts, last update status
- `解读`: which factors matter most to the thesis and why
- `待验证问题`: which missing data points could change the signal
- `Dashboard`: metric, threshold, latest value, source, next check date

## Boundaries

- Do not restate the full strategy review.
- Do not recalculate all financial ratios unless needed for a monitor.
- Do not produce target price or position sizing.
