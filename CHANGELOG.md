# 更新记录 / Changelog

[中文](#中文) | [English](#english)

## 中文

本文件记录项目的重要变更。

格式参考 Keep a Changelog，但按本仓库实际情况保持简洁。

## [0.1.0] - 2026-03-09

### 新增

- 发布 A 股股票研究 skills pack 的首个开源版本
- 新增母 skill：`china-stock-research-orchestrator`
- 新增 6 个核心研究模块，覆盖战略、业务质量、财务健康度、竞争格局、风险监测、估值框架
- 新增共享 references，用于统一来源选择、引用规则、披露地图、输出结构与分析模式选择
- 新增可复用 analysis-pattern overlays，覆盖转型、订单驱动、重资产爬坡、周期、消费、医药政策、出口制造等常见场景
- 将 IDC 保留为可选示例 overlay，而不是默认框架
- 新增共享模板，用于证据表、公司事实卡、催化剂日历、估值情景表和 IDC 项目台账
- 新增开源文档：`INSTALL.md`、`SKILLS.md`、`CONTRIBUTING.md`、`ROADMAP.md`
- 新增 `examples/` 目录中的使用示例
- 新增 `.github/` 下的协作模板

### 引入的设计原则

- 关键事实必须带可访问来源链接
- `事实`、`解读`、`待验证问题` 必须严格分层
- 官方披露优先于评论和媒体摘要
- 优先复用分析模式，再决定是否加载行业 overlay

## English

This file records notable changes to the project.

The format is loosely based on Keep a Changelog, while staying compact for this repository.

## [0.1.0] - 2026-03-09

### Added

- Initial open-source release of the China stock research skills pack
- Parent workflow skill: `china-stock-research-orchestrator`
- Six core research modules for strategy, business quality, financial health, competition, monitoring, and valuation
- Shared references for source selection, citation rules, disclosure mapping, output structure, and pattern selection
- Reusable analysis-pattern overlays for transition, project-order, asset-ramp, cyclical, consumer, healthcare-policy, and export-manufacturing cases
- IDC overlay as an optional example, not the default framework
- Shared templates for evidence tables, fact sheets, catalyst calendars, valuation scenarios, and IDC project ledgers
- Open-source docs: `INSTALL.md`, `SKILLS.md`, `CONTRIBUTING.md`, `ROADMAP.md`
- Usage examples under `examples/`
- GitHub collaboration templates under `.github/`

### Design Principles Introduced

- Facts must carry accessible source links
- Facts, Interpretation, and Open Questions stay separate
- Official disclosures outrank commentary
- Reusable analysis patterns come before sector-specific overlays
