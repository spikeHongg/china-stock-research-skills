---
name: china-stock-research-orchestrator
description: Orchestrate a full China stock research workflow by first identifying the company's analysis patterns, then selecting and sequencing the right core research skills, optional overlays, and final output structure. Use this skill when starting a new stock deep-dive or when a user wants one unified, source-backed research framework instead of isolated module outputs.
---

# China Stock Research Orchestrator

Route an A-share company through the right research workflow before doing deep analysis.

## Non-Negotiable Rules

- Preserve strict separation between `Facts`, `Interpretation`, and `Open Questions`.
- Require every key fact and number to carry an accessible source link.
- Prefer official disclosures, regulators, and public official portals over media and commentary.
- Use this skill to orchestrate the workflow, not to replace the six core modules.
- Default every intermediate and final output to Simplified Chinese unless the user explicitly requests another language.

## Read First

- `skills/shared/references/source-registry.md`
- `skills/shared/references/citation-standard.md`
- `skills/shared/references/company-disclosure-map.md`
- `skills/shared/references/research-output-template.md`
- `skills/shared/references/analysis-pattern-selector.md`
- `skills/shared/references/language-output-standard.md`
- `skills/china-stock-research-orchestrator/references/routing-matrix.md`
- `skills/china-stock-research-orchestrator/references/sector-overlay-escalation-rules.md`
- `skills/china-stock-research-orchestrator/references/final-output-contract.md`

## Required Inputs

- Company name and ticker if available
- Research objective or key question
- As-of date if the user cares about a specific cutoff
- Optional hints about industry, business model, or suspected issues

## When to Use

- Start a fresh A-share stock deep-dive.
- Turn a vague request like "analyze this stock" into a structured workflow.
- Decide which of the six core modules are necessary before going deep.
- Merge module outputs into one consistent research framework.

## Workflow

1. Identify the company's primary and secondary analysis patterns with `skills/shared/references/analysis-pattern-selector.md`.
2. Use `skills/china-stock-research-orchestrator/references/routing-matrix.md` to decide which core modules are mandatory, optional, or skippable.
3. Decide whether a sector overlay is needed using `skills/china-stock-research-orchestrator/references/sector-overlay-escalation-rules.md`.
4. Run the selected modules in the right order, usually `strategy -> business -> financial -> industry -> risk -> valuation`.
5. Require each module to return mergeable `事实`, `解读`, and `待验证问题` blocks in Simplified Chinese.
6. Merge the outputs using `skills/china-stock-research-orchestrator/references/final-output-contract.md`.

## Required Output

- `公司概览与路由决策`: what patterns the company matches and why
- `已选模块`: which core skills are required and why
- `已选 overlays`: which optional overlays are loaded and why
- `研究框架`: merged `事实`, `解读`, `待验证问题`, `监测指标`, and `情景与估值钩子`
- `来源附录`: the source set used and any evidence limitations

## Core Modules Available

- `strategy-business-transition`
- `business-decomposition-order-quality`
- `financial-health`
- `industry-competition-moat`
- `risk-warning-catalysts`
- `valuation-investment-strategy`

## Boundaries

- Do not directly replace deep analysis inside the six core skills.
- Do not invent a pattern match if evidence is weak; mark uncertainty in `Open Questions`.
- Do not produce unsupported target prices or thesis conclusions.
- Do not merge module outputs into a single-layer narrative; keep evidence layering intact.
