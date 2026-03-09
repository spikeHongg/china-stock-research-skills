# China Stock Research Skills

[简体中文](README.md)

Turn a vague prompt like `analyze this stock` into a structured, source-backed, Chinese-first workflow for China stock research.

This is an open-source agent skills system for China stock research, designed around public-information workflows and Simplified Chinese outputs by default. It is suitable for fundamentals, business analysis, risk monitoring, and valuation framing, but not for real-time market data, automated trading, or proprietary database workflows.

## At A Glance

- `Route first` - identify the research pattern before choosing modules
- `Evidence first` - key facts must carry accessible source links
- `Chinese first` - intermediate and final outputs default to Simplified Chinese

## What You Get

- One parent orchestrator: `china-stock-research-orchestrator`
- Six composable core research modules
- Shared citation standards, pattern overlays, and templates
- A reusable framework built for public-information workflows

## What It Is

- A modular skills pack for China stock research
- A parent orchestrator that identifies analysis patterns and routes the workflow
- Six core modules covering strategy, business quality, financial health, competition, monitoring, and valuation
- Shared standards for sources, citations, output structure, analysis patterns, and overlays

## Who It Is For

- Equity researchers working from public disclosures
- Investors building structured stock research workflows
- Agent users who want reproducible, citation-first company analysis

## Not For

- Real-time quote systems or tick-level trading
- Fully automated investment advice
- Closed-data workflows that depend on paid terminals or private datasets

## Quick Start

Install the skills, then start with the orchestrator. If you only read three lines, this is enough.

```bash
bunx skills add <owner>/<repo>
```

Then use this prompt directly:

```text
Use the china-stock-research-orchestrator skill to analyze this China-listed company, identify the main analysis patterns, choose the required modules, and return a source-backed research framework. Default all intermediate and final outputs to Simplified Chinese.
```

For local development:

```bash
bunx skills add . --list
```

See `INSTALL.md` for install details.

## Language Behavior

- `README.md` is the default Simplified Chinese README
- `README.en.md` provides the English version
- All intermediate and final workflow outputs default to Simplified Chinese
- English output should be used only when the user explicitly asks for it
- English technical terms and source titles may be preserved when needed for accuracy and retrieval

See `skills/shared/references/language-output-standard.md`.

## Skill Map

This repository includes 7 skills:

1. `china-stock-research-orchestrator`
2. `strategy-business-transition`
3. `business-decomposition-order-quality`
4. `financial-health`
5. `industry-competition-moat`
6. `risk-warning-catalysts`
7. `valuation-investment-strategy`

See `SKILLS.md` for the full index.

## How It Works

Start with the parent skill:

1. `china-stock-research-orchestrator`

It will:

- identify the company's main analysis patterns
- decide which core modules are required
- load optional overlays only when needed
- merge outputs into one evidence-layered framework

Default full-flow module order:

1. `strategy-business-transition`
2. `business-decomposition-order-quality`
3. `financial-health`
4. `industry-competition-moat`
5. `risk-warning-catalysts`
6. `valuation-investment-strategy`

## Design Principles

- `Evidence first` - every key fact should carry an accessible source link
- `Layered output` - always separate `Facts`, `Interpretation`, and `Open Questions`
- `Official sources first` - disclosures and regulators outrank media summaries
- `Patterns over sectors` - start from reusable analysis patterns, then add sector overlays if needed
- `Composable modules` - the orchestrator routes work but does not replace specialist modules

## Shared Standards

Read these shared references before using any module:

- `skills/shared/references/source-registry.md`
- `skills/shared/references/citation-standard.md`
- `skills/shared/references/company-disclosure-map.md`
- `skills/shared/references/research-output-template.md`
- `skills/shared/references/analysis-pattern-selector.md`
- `skills/shared/references/language-output-standard.md`

Common optional overlays include:

- `skills/shared/references/business-model-transition-overlay.md`
- `skills/shared/references/project-order-business-overlay.md`
- `skills/shared/references/asset-heavy-ramp-overlay.md`
- `skills/shared/references/cyclical-price-driven-overlay.md`
- `skills/shared/references/consumer-channel-brand-overlay.md`
- `skills/shared/references/regulated-healthcare-policy-overlay.md`
- `skills/shared/references/export-manufacturing-supply-chain-overlay.md`

IDC is kept as an example overlay, not the default framework:

- `skills/shared/references/idc-heavy-asset-transition-overlay.md`
- `skills/shared/templates/idc-project-ledger.md`

## Repository Layout

```text
skills/
  china-stock-research-orchestrator/
  shared/
    references/
    templates/
  strategy-business-transition/
  business-decomposition-order-quality/
  financial-health/
  industry-competition-moat/
  risk-warning-catalysts/
  valuation-investment-strategy/
examples/
```

## Example Prompts

- `Use the china-stock-research-orchestrator skill to decide how this China-listed company should be analyzed and which modules to run.`
- `Use the financial-health skill to diagnose why revenue growth is not converting into profit and cash flow.`
- `Use the industry-competition-moat skill to analyze whether this cyclical materials company is benefiting from a true moat or just a price cycle.`
- `Use the risk-warning-catalysts skill with the healthcare overlay to build a monitoring dashboard for policy, approval, and reimbursement changes.`

See `examples/quickstart-prompts.md` and `examples/full-report-flow.md` for copy-paste examples.

## Limitations

- This repository depends on public, accessible information
- It does not guarantee correctness if source documents are incomplete, changed, or unavailable
- It does not replace reading original filings
- It is not investment advice
- Industry overlays are still expanding

## Contributing

Contributions are welcome. Start with `CONTRIBUTING.md`.

## Roadmap

See `ROADMAP.md`.

## Changelog

See `CHANGELOG.md`.

## Publishing

See `GITHUB_PUBLISHING.md`, `RELEASE_ASSETS.md`, and `PUBLISH_CHECKLIST.md` for publishing and maintenance support.

## License

MIT. See `LICENSE`.
