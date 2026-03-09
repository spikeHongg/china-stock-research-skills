# Final Output Contract

Merge module outputs into one research framework without collapsing evidence layers.

Default the merged output to Simplified Chinese. See `skills/shared/references/language-output-standard.md`.

## Required Section Order

1. `公司概览与路由决策`
2. `事实`
3. `解读`
4. `待验证问题`
5. `监测指标`
6. `情景与估值钩子`
7. `来源附录`

## Section Rules

### 1. 公司概览与路由决策

- State the company name, ticker, as-of date, and selected patterns.
- State which core modules were run and why.
- State which overlays were loaded and why.

### 2. 事实

- Include only source-backed facts.
- Keep the citation with each key statement.
- Tag the originating module when useful, for example `事实 | financial-health`.

### 3. 解读

- Explain what the facts likely mean.
- Do not convert inference into fact.
- Refer back to the supporting facts and sources.

### 4. 待验证问题

- State what is still unknown.
- State the next source to check.
- Keep open questions explicit instead of hiding uncertainty.

### 5. 监测指标

- Pull the highest-signal indicators from `risk-warning-catalysts`.
- Attach thresholds and source paths where possible.

### 6. 情景与估值钩子

- Include only the assumptions and method hooks needed for valuation.
- Do not force an exact target price if the evidence is incomplete.

### 7. 来源附录

- List the primary source set.
- List important secondary source set.
- Note inaccessible, conflicting, or incomplete evidence.

## Merge Rule

- Never merge facts and interpretation into one sentence if that hides the evidence boundary.
- If two modules conflict, keep both views and explain the difference.
