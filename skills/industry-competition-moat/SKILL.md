---
name: industry-competition-moat
description: Analyze the industry structure, competition, supply-demand balance, and moat of an A-share company. Use this skill when testing whether a company's growth can be sustained, whether its claimed differentiation is real, and which external industry forces could compress returns. All outputs must include accessible source links.
---

# Industry Competition Moat

Place the company inside its real industry structure and test whether it has defensible economics.

## Non-Negotiable Rules

- Use public policy, statistics, procurement, and company disclosures to validate industry claims.
- Separate company claims from third-party validation.
- State which competitor comparison points are fact and which are inference.
- Do not repeat detailed company financial scoring here.
- Default every intermediate and final output to Simplified Chinese unless the user explicitly requests another language.

## Read First

- `skills/shared/references/source-registry.md`
- `skills/shared/references/citation-standard.md`
- `skills/shared/references/analysis-pattern-selector.md`
- `skills/shared/references/language-output-standard.md`
- `skills/shared/references/sector-adaptation-checklist.md`
- `skills/industry-competition-moat/references/moat-grid.md`
- If the company is in a policy-sensitive or asset-heavy sector, load the relevant shared overlay first.
- If the company is an IDC or AI-compute infrastructure case, `skills/shared/references/idc-heavy-asset-transition-overlay.md` and `skills/industry-competition-moat/references/idc-value-chain-and-peers.md` are optional example overlays.

## When to Use

- Assess industry attractiveness and rivalry.
- Compare the company with listed peers and alternative business models.
- Test whether policy, capital, qualification, data, channel, or switching cost creates a moat.

## Workflow

1. Define the value chain and the company's exact position in it.
2. Pull industry-policy and demand data from official sources.
3. Select a source-backed peer set and compare capacity, clients, margins, and business model.
4. Apply a moat grid and a five-forces style structure.
5. Highlight where the company captures value and where it remains vulnerable.

## Required Output

- `事实`: industry size, policy tailwind/headwind, peer positions, value-chain role
- `解读`: moat strength, structural advantage, likely pressure points
- `待验证问题`: missing peer metrics, uncertain supply additions, unclear regulation
- `Value Chain Map`: each link labeled strong, medium, or weak capture ability

## Boundaries

- Do not run the company's order pipeline in detail.
- Do not build the risk dashboard here.
- Do not produce target price or trading plan.
