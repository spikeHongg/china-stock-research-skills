# China Stock Research Skills

[English](README.en.md)

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![GitHub release](https://img.shields.io/github/v/release/spikeHongg/china-stock-research-skills)](https://github.com/spikeHongg/china-stock-research-skills/releases)
[![GitHub stars](https://img.shields.io/github/stars/spikeHongg/china-stock-research-skills?style=social)](https://github.com/spikeHongg/china-stock-research-skills)
[![GitHub forks](https://img.shields.io/github/forks/spikeHongg/china-stock-research-skills?style=social)](https://github.com/spikeHongg/china-stock-research-skills/forks)

把一句模糊的 `分析这只股票`，变成一套结构化、可引用、默认中文输出的中国股票研究工作流。

这是一个面向中国股票研究的开源 agent skills 系统，默认服务于基于公开信息的中文研究流程。它适用于基本面、业务面、风险与估值分析，不适用于实时行情、自动交易或依赖私有数据库的工作流。

## 一句话看懂

- `先路由`：先判断股票属于哪类研究问题，再决定该跑哪些模块
- `先证据`：关键事实必须附可访问来源链接
- `先中文`：中间产物和最终产物默认输出简体中文

## 你会得到

- 一个总控母 skill：`china-stock-research-orchestrator`
- 六个可组合的核心研究模块
- 一套共享引用标准、分析模式 overlays 与模板
- 一套适合公开信息研究的可复用框架

## 这是什么

- 一套面向中国股票研究的模块化 skills pack
- 一个总控母 skill，用来识别分析模式并编排研究流程
- 六个核心模块，覆盖战略、业务质量、财务健康度、行业竞争、风险监测、估值
- 一套共享标准，统一来源、引用、输出结构、分析模式与 overlays

## 适合谁

- 基于公开披露做股票研究的研究员和投资者
- 想把股票分析工作流 agent 化、模块化的人
- 希望让研究过程可复盘、可核查、可迁移的人

## 不适合什么场景

- 实时行情或高频交易系统
- 自动化投资建议系统
- 必须依赖付费终端或私有数据库的封闭工作流

## 快速开始

先安装，再从总控母 skill 开始；如果只看三行，这三步就够了。

可直接复制的远程安装命令：

```bash
bunx skills add spikeHongg/china-stock-research-skills
```

上面的占位写法 `bunx skills add <owner>/<repo>` 也是对的，只是对首次访问者不如可复制示例直观。

然后直接使用下面这条提示词：

```text
使用 china-stock-research-orchestrator skill 分析这家中国上市公司，先识别它属于哪些分析模式，再选择需要调用的模块，并返回一份带可访问来源链接的研究框架。所有步骤与最终输出默认使用中文。
```

本地开发时可以先检查发现情况：

```bash
bunx skills add . --list
```

安装细节见 `INSTALL.md`。

## 语言规则

- `README.md` 默认中文
- 英文说明见 `README.en.md`
- 使用过程中，所有中间产物和最终产物默认输出为简体中文
- 若用户明确要求英文，再切换为英文
- 若引用英文术语、监管名词、文档标题，为保证可检索性可保留原文，但整体句子结构仍默认中文

详见 `skills/shared/references/language-output-standard.md`。

## Skill 地图

本仓库包含 7 个 skills：

1. `china-stock-research-orchestrator`
2. `strategy-business-transition`
3. `business-decomposition-order-quality`
4. `financial-health`
5. `industry-competition-moat`
6. `risk-warning-catalysts`
7. `valuation-investment-strategy`

完整索引见 `SKILLS.md`。

## 如何工作

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

## 设计原则

- `证据优先`：每条关键事实都应带可访问来源链接
- `输出分层`：必须区分 `事实`、`解读`、`待验证问题`
- `官方优先`：交易所、监管、公司正式披露优先于媒体摘要
- `模式优先于行业`：先识别共性分析模式，再决定是否加载行业 overlay
- `模块可组合`：母 skill 只编排，不替代各专业模块

## 共享标准

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

其他 overlays 与模板可直接查看 `skills/shared/references/` 和 `skills/shared/templates/`。

## 仓库结构

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

## 示例提示词

- `使用 china-stock-research-orchestrator skill 判断这只中国股票应该走哪条研究路径，并列出需要运行的模块。`
- `使用 financial-health skill 诊断这家公司为什么收入增长没有转化成利润和现金流。`
- `使用 industry-competition-moat skill 判断这家周期材料公司赚的是周期的钱还是护城河的钱。`
- `使用 risk-warning-catalysts skill，并结合 healthcare overlay，为这家公司建立政策、审批、医保相关的监测面板。`

更多复制即用示例见 `examples/quickstart-prompts.md` 和 `examples/full-report-flow.md`。

## 局限性

- 本仓库依赖公开、可访问的信息源
- 若原始披露不完整、被修改或不可访问，结果也会受影响
- 它不能替代对原始公告和财报的直接阅读
- 它不是投资建议
- 行业 overlays 仍会继续扩展

## 贡献

欢迎贡献，先看 `CONTRIBUTING.md`。

## 路线图

见 `ROADMAP.md`。

## 更新记录

见 `CHANGELOG.md`。

## 发布说明

如果你准备继续维护 GitHub 发布，见 `GITHUB_PUBLISHING.md`、`RELEASE_ASSETS.md`、`PUBLISH_CHECKLIST.md`。

## 许可证

MIT，见 `LICENSE`。
