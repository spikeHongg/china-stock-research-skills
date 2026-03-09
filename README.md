# China Stock Research Skills

[中文](#中文说明) | [English](#english)

## 中文说明

面向 A 股基本面、业务面、风险与估值研究的开源 agent skills 系统。

这个仓库的目标，是把一句模糊的 `分析这只股票`，转换成一套结构化、可追溯、引用优先的研究流程。它适用于基于公开信息的股票研究，不适用于实时行情、自动交易或依赖私有数据库的工作流。

### 这是什么

- 一套面向 A 股研究的模块化 skills pack
- 一个总控母 skill，用来识别分析模式并编排研究流程
- 六个核心模块，覆盖战略、业务质量、财务健康度、行业竞争、风险监测、估值
- 一套共享标准，统一来源、引用、输出结构、分析模式与 overlays

### 适合谁

- 基于公开披露做股票研究的研究员和投资者
- 想把股票分析工作流 agent 化、模块化的人
- 希望让研究过程可复盘、可核查、可迁移的人

### 不适合什么场景

- 实时行情或高频交易系统
- 自动化投资建议系统
- 必须依赖付费终端或私有数据库的封闭工作流

### 快速开始

先安装技能，再从总控母 skill 开始。

```bash
bunx skills add <owner>/<repo>
```

然后使用类似下面的提示词：

```text
使用 china-stock-research-orchestrator skill 分析这家 A 股公司，先识别它属于哪些分析模式，再选择需要调用的模块，并返回一份带可访问来源链接的研究框架。所有步骤与最终输出默认使用中文。
```

本地开发时可以先检查发现情况：

```bash
bunx skills add . --list
```

安装细节见 `INSTALL.md`。

### 语言规则

- README 默认中文，完整提供中英文切换
- 使用过程中，所有中间产物和最终产物默认输出为简体中文
- 若用户明确要求英文，再切换为英文
- 若引用英文术语、监管名词、文档标题，为保证可检索性可保留原文，但整体句子结构仍默认中文

详见 `skills/shared/references/language-output-standard.md`。

### Skill 地图

本仓库包含 7 个 skills：

1. `china-stock-research-orchestrator`
2. `strategy-business-transition`
3. `business-decomposition-order-quality`
4. `financial-health`
5. `industry-competition-moat`
6. `risk-warning-catalysts`
7. `valuation-investment-strategy`

完整索引见 `SKILLS.md`。

### 如何工作

建议总是从母 skill 开始：

1. `china-stock-research-orchestrator`

它会负责：

- 识别公司属于哪些分析模式
- 判断哪些核心模块必须运行
- 仅在必要时加载对应 overlay
- 把模块结果合并成一份分层研究框架

完整流程下，默认模块顺序是：

1. `strategy-business-transition`
2. `business-decomposition-order-quality`
3. `financial-health`
4. `industry-competition-moat`
5. `risk-warning-catalysts`
6. `valuation-investment-strategy`

### 设计原则

- `证据优先`：每条关键事实都应带可访问来源链接
- `输出分层`：必须区分 `事实`、`解读`、`待验证问题`
- `官方优先`：交易所、监管、公司正式披露优先于媒体摘要
- `模式优先于行业`：先识别共性分析模式，再决定是否加载行业 overlay
- `模块可组合`：母 skill 只编排，不替代各专业模块

### 共享标准

在使用任何模块前，优先阅读这些共享 references：

- `skills/shared/references/source-registry.md`
- `skills/shared/references/citation-standard.md`
- `skills/shared/references/company-disclosure-map.md`
- `skills/shared/references/research-output-template.md`
- `skills/shared/references/analysis-pattern-selector.md`
- `skills/shared/references/language-output-standard.md`

常见可选 overlays 包括：

- `skills/shared/references/business-model-transition-overlay.md`
- `skills/shared/references/project-order-business-overlay.md`
- `skills/shared/references/asset-heavy-ramp-overlay.md`
- `skills/shared/references/cyclical-price-driven-overlay.md`
- `skills/shared/references/consumer-channel-brand-overlay.md`
- `skills/shared/references/regulated-healthcare-policy-overlay.md`
- `skills/shared/references/export-manufacturing-supply-chain-overlay.md`

IDC 仅作为示例 overlay 保留，不是默认框架：

- `skills/shared/references/idc-heavy-asset-transition-overlay.md`
- `skills/shared/templates/idc-project-ledger.md`

### 仓库结构

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

### 示例提示词

- `使用 china-stock-research-orchestrator skill 判断这只 A 股应该走哪条研究路径，并列出需要运行的模块。`
- `使用 financial-health skill 诊断这家公司为什么收入增长没有转化成利润和现金流。`
- `使用 industry-competition-moat skill 判断这家周期材料公司赚的是周期的钱还是护城河的钱。`
- `使用 risk-warning-catalysts skill，并结合 healthcare overlay，为这家公司建立政策、审批、医保相关的监测面板。`

更多复制即用示例见 `examples/quickstart-prompts.md` 和 `examples/full-report-flow.md`。

### 局限性

- 本仓库依赖公开、可访问的信息源
- 若原始披露不完整、被修改或不可访问，结果也会受影响
- 它不能替代对原始公告和财报的直接阅读
- 它不是投资建议
- 行业 overlays 仍会继续扩展

### 贡献

欢迎贡献，先看 `CONTRIBUTING.md`。

比较有价值的贡献包括：

- 更清晰的来源与引用规则
- 更好的示例
- 新的可复用 analysis pattern 或 overlay
- 修复 skill 边界、措辞或流程设计问题

### 路线图

见 `ROADMAP.md`。

### 更新记录

见 `CHANGELOG.md`。

### 发布说明

如果你准备把这个仓库发布到 GitHub，见 `GITHUB_PUBLISHING.md`。

### 许可证

MIT，见 `LICENSE`。

## English

Open-source agent skills for A-share fundamental, business, risk, and valuation research.

This repository turns a vague prompt like `analyze this stock` into a structured, source-backed workflow. It is designed for public-information equity research, not real-time market data, automated trading, or proprietary database workflows.

### What It Is

- A modular skills pack for A-share stock research
- A parent orchestrator that identifies analysis patterns and routes the workflow
- Six core modules covering strategy, business quality, financial health, competition, monitoring, and valuation
- Shared standards for sources, citations, output structure, analysis patterns, and overlays

### Who It Is For

- Equity researchers working from public disclosures
- Investors building structured stock research workflows
- Agent users who want reproducible, citation-first company analysis

### Not For

- Real-time quote systems or tick-level trading
- Fully automated investment advice
- Closed-data workflows that depend on paid terminals or private datasets

### Quick Start

Install the skills, then start with the orchestrator.

```bash
bunx skills add <owner>/<repo>
```

Then use a prompt like:

```text
Use the china-stock-research-orchestrator skill to analyze this A-share company, identify the main analysis patterns, choose the required modules, and return a source-backed research framework. Default all intermediate and final outputs to Simplified Chinese unless I explicitly request another language.
```

For local development:

```bash
bunx skills add . --list
```

See `INSTALL.md` for install details.

### Language Behavior

- The README defaults to Chinese and provides a full English section
- All intermediate and final workflow outputs default to Simplified Chinese
- English output should be used only when the user explicitly asks for it
- English technical terms and source titles may be preserved when needed for accuracy and retrieval

See `skills/shared/references/language-output-standard.md`.

### Skill Map

This repository includes 7 skills:

1. `china-stock-research-orchestrator`
2. `strategy-business-transition`
3. `business-decomposition-order-quality`
4. `financial-health`
5. `industry-competition-moat`
6. `risk-warning-catalysts`
7. `valuation-investment-strategy`

See `SKILLS.md` for the full index.

### How It Works

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

### Design Principles

- `Evidence first` - every key fact should carry an accessible source link
- `Layered output` - always separate `Facts`, `Interpretation`, and `Open Questions`
- `Official sources first` - disclosures and regulators outrank media summaries
- `Patterns over sectors` - start from reusable analysis patterns, then add sector overlays if needed
- `Composable modules` - the orchestrator routes work but does not replace specialist modules

### Shared Standards

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

### Repository Layout

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

### Example Prompts

- `Use the china-stock-research-orchestrator skill to decide how this A-share company should be analyzed and which modules to run.`
- `Use the financial-health skill to diagnose why revenue growth is not converting into profit and cash flow.`
- `Use the industry-competition-moat skill to analyze whether this cyclical materials company is benefiting from a true moat or just a price cycle.`
- `Use the risk-warning-catalysts skill with the healthcare overlay to build a monitoring dashboard for policy, approval, and reimbursement changes.`

See `examples/quickstart-prompts.md` and `examples/full-report-flow.md` for copy-paste examples.

### Limitations

- This repository depends on public, accessible information
- It does not guarantee correctness if source documents are incomplete, changed, or unavailable
- It does not replace reading original filings
- It is not investment advice
- Industry overlays are still expanding

### Contributing

Contributions are welcome. Start with `CONTRIBUTING.md`.

### Roadmap

See `ROADMAP.md`.

### Changelog

See `CHANGELOG.md`.

### Publishing

See `GITHUB_PUBLISHING.md` for suggested GitHub publishing metadata and release notes.

### License

MIT. See `LICENSE`.
