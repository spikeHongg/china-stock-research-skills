# GitHub 发布指南 / GitHub Publishing Guide

[中文](#中文) | [English](#english)

## 中文

这份文件用于帮助你在将仓库公开到 GitHub 前，做最后一轮发布收尾。

### 建议仓库名

- `china-stock-research-skills`

简短、直观、易记。

### 建议的 GitHub Description

- `面向 A 股股票研究的开源 agent skills，强调工作流编排、证据优先分析与可复用 overlays。`

如果你更希望 description 用英文，也可以使用：

- `Open-source agent skills for A-share stock research, with orchestrated workflows, citation-first analysis, and reusable sector overlays.`

### 建议 Topics

- `a-share`
- `stock-research`
- `equity-research`
- `agent-skills`
- `claude-code`
- `opencode`
- `codex`
- `investment-research`
- `financial-analysis`
- `company-research`

### 建议 Homepage

- 初期可以留空，或者直接指向仓库自身
- 只有在你后续建立独立文档页或项目主页时，再补 homepage

### 建议 Social Preview 文案

- `面向 A 股结构化研究的开源 skills pack。强调证据优先、模块化设计与 agent 工作流。`

### 首个版本 Tag

- `v0.1.0`

这个版本已经具备较完整的首发条件，因为它包含：

- 1 个 orchestrator skill
- 6 个核心研究模块
- 共享来源与引用标准
- 面向常见 A 股研究问题的可复用 overlays
- 安装、使用、贡献、示例等基础文档

### 首个 Release 标题

- `v0.1.0 - 首个开源版本`

### 首个 Release Notes

```md
## 亮点

- 新增 `china-stock-research-orchestrator`，用于把一只股票路由到合适的研究流程
- 提供 6 个核心 A 股研究模块，覆盖战略、业务质量、财务健康度、竞争格局、风险监测、估值框架
- 新增证据优先的共享标准，要求关键事实附可访问来源链接
- 新增可复用 overlays，覆盖业务转型、订单驱动、重资产爬坡、周期、消费品牌、医药政策、出口制造等常见场景
- 将 IDC 保留为可选示例 overlay，而不是默认假设

## 本版本包含

- `china-stock-research-orchestrator`
- `strategy-business-transition`
- `business-decomposition-order-quality`
- `financial-health`
- `industry-competition-moat`
- `risk-warning-catalysts`
- `valuation-investment-strategy`

## 文档

- `README.md`
- `INSTALL.md`
- `SKILLS.md`
- `CONTRIBUTING.md`
- `ROADMAP.md`
- `examples/`

## 说明

- 本项目面向基于公开信息的 A 股研究工作流
- 它不是实时行情工具，也不是投资建议系统
```

### 建议的发布前检查清单

#### 发布前

- 确认 `README.md` 从头到尾读起来顺畅
- 确认 `LICENSE` 已存在
- 确认 `bunx skills add . --list` 能发现全部 skills
- 确认 examples 中的 skill 名称与仓库当前一致
- 确认公开文档中没有残留本地私有路径

#### 发布后

- 在 GitHub 设置中补 description 和 topics
- 创建 tag `v0.1.0`
- 将上面的 release notes 粘贴到 GitHub Release 页面
- 在新目录中测试远程安装：`bunx skills add <owner>/<repo> --list`
- 如有需要，可先自建一个 roadmap issue 方便外部用户了解后续计划

### 建议首批 Pin 的 Issues

- `Roadmap: next overlays and example outputs`
- `Request for feedback: install flow and first-use prompts`

### 之后可以再补的内容

- `CODE_OF_CONDUCT.md`
- `SECURITY.md`
- 更完整的双语文档
- 示例输出截图或快照

### 配套文件

- `RELEASE_ASSETS.md`：可直接复制到 GitHub 的 about、release、issues 文案
- `PUBLISH_CHECKLIST.md`：实际发布时可以逐步执行的 checklist

## English

Use this file as the final polish checklist before making the repository public on GitHub.

### Recommended Repository Name

- `china-stock-research-skills`

Short, descriptive, and easy to remember.

### Recommended GitHub Description

- `Open-source agent skills for A-share stock research, with orchestrated workflows, citation-first analysis, and reusable sector overlays.`

### Recommended Topics

- `a-share`
- `stock-research`
- `equity-research`
- `agent-skills`
- `claude-code`
- `opencode`
- `codex`
- `investment-research`
- `financial-analysis`
- `company-research`

### Suggested Homepage

- Leave blank at first, or point it to the GitHub repository itself
- Add a homepage later only if you create dedicated docs or a project page

### Suggested Social Preview Copy

- `Open-source skills pack for structured A-share stock research. Citation-first, modular, and built for agent workflows.`

### First Release Tag

- `v0.1.0`

This version is a strong first public release because it already includes:

- 1 orchestrator skill
- 6 core research modules
- shared source and citation standards
- reusable overlays for common A-share analysis patterns
- install docs, examples, and contribution docs

### First Release Title

- `v0.1.0 - Initial open-source release`

### First Release Notes

```md
## Highlights

- Add `china-stock-research-orchestrator` to route a stock into the right research workflow
- Ship 6 core A-share research modules covering strategy, business quality, financial health, competition, monitoring, and valuation
- Add citation-first shared standards with accessible source-link requirements
- Add reusable overlays for business-model transition, project-order businesses, asset-heavy ramps, cyclicals, consumer brands, healthcare-policy cases, and export manufacturing
- Keep IDC as an optional example overlay instead of a default assumption

## Included In This Release

- `china-stock-research-orchestrator`
- `strategy-business-transition`
- `business-decomposition-order-quality`
- `financial-health`
- `industry-competition-moat`
- `risk-warning-catalysts`
- `valuation-investment-strategy`

## Documentation

- `README.md`
- `INSTALL.md`
- `SKILLS.md`
- `CONTRIBUTING.md`
- `ROADMAP.md`
- `examples/`

## Notes

- This project is designed for public-information A-share research workflows
- It is not a real-time market data tool and not investment advice
```

### Suggested Launch Checklist

#### Before Publishing

- Confirm `README.md` reads well from top to bottom
- Confirm `LICENSE` is present
- Confirm `bunx skills add . --list` shows all expected skills
- Confirm examples still match the current skill names
- Confirm no local-only paths remain in public docs

#### After Publishing

- Add repository description and topics in GitHub settings
- Create tag `v0.1.0`
- Paste the release notes above into the GitHub release page
- Test remote install from a fresh clone using `bunx skills add <owner>/<repo> --list`
- Open one self-filed issue for roadmap visibility, if desired

### Suggested First Pinned Issues

- `Roadmap: next overlays and example outputs`
- `Request for feedback: install flow and first-use prompts`

### Optional Nice-to-Haves Later

- `CODE_OF_CONDUCT.md`
- `SECURITY.md`
- more complete bilingual docs
- sample output snapshots

### Companion Files

- `RELEASE_ASSETS.md`: copy-ready text for GitHub about, release notes, and pinned issues
- `PUBLISH_CHECKLIST.md`: a step-by-step checklist for the actual launch
