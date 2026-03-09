# Skills 索引 / Skills Index

[中文](#中文) | [English](#english)

## 中文

本仓库当前包含 7 个 skills。

### 母 skill

| Skill | 适用场景 | 主要输出 |
| --- | --- | --- |
| `china-stock-research-orchestrator` | 识别分析模式、路由模块、选择 overlays、合并结果 | 统一研究框架 |

### 核心模块

| Skill | 适用场景 | 主要输出 |
| --- | --- | --- |
| `strategy-business-transition` | 业务历史、转型路径、 legacy drag、管理层战略 | 转型评估 |
| `business-decomposition-order-quality` | 分部结构、客户、项目、在手订单、订单质量 | 业务质量与 pipeline 视图 |
| `financial-health` | 盈利质量、营运资本、杠杆、偿债、减值 | 财务健康度评分卡 |
| `industry-competition-moat` | 行业结构、可比公司、供需、护城河强弱 | 竞争格局与护城河视图 |
| `risk-warning-catalysts` | 风险面板、催化剂日历、监测阈值 | 跟踪与监测框架 |
| `valuation-investment-strategy` | 情景假设、估值方法、估值框架 | 带来源支撑的估值区间 |

### 共享 references

建议先从这些共享 references 开始：

- `skills/shared/references/source-registry.md`
- `skills/shared/references/citation-standard.md`
- `skills/shared/references/company-disclosure-map.md`
- `skills/shared/references/research-output-template.md`
- `skills/shared/references/analysis-pattern-selector.md`
- `skills/shared/references/language-output-standard.md`

之后再根据公司匹配情况按需加载 overlays。

### 典型使用路径

1. 先运行 `china-stock-research-orchestrator`
2. 让它选择合适的核心模块
3. 只有在公司明确匹配时再加载可选 overlays
4. 按最终输出契约合并结果

## English

This repository currently ships 7 skills.

### Parent Skill

| Skill | Use It For | Main Output |
| --- | --- | --- |
| `china-stock-research-orchestrator` | Identify analysis patterns, route modules, choose overlays, and merge outputs | Unified research framework |

### Core Modules

| Skill | Use It For | Main Output |
| --- | --- | --- |
| `strategy-business-transition` | Business history, transformation path, legacy drag, management strategy | Transition assessment |
| `business-decomposition-order-quality` | Segment mix, customers, projects, backlog, and order quality | Business quality and pipeline view |
| `financial-health` | Earnings quality, working capital, leverage, solvency, and impairment | Financial health scorecard |
| `industry-competition-moat` | Industry structure, peers, supply-demand, and moat strength | Competitive landscape and moat view |
| `risk-warning-catalysts` | Risk dashboard, catalyst calendar, and monitoring thresholds | Monitoring framework |
| `valuation-investment-strategy` | Scenario hooks, method choice, and valuation framing | Source-backed valuation range |

### Shared References

Start with:

- `skills/shared/references/source-registry.md`
- `skills/shared/references/citation-standard.md`
- `skills/shared/references/company-disclosure-map.md`
- `skills/shared/references/research-output-template.md`
- `skills/shared/references/analysis-pattern-selector.md`
- `skills/shared/references/language-output-standard.md`

Then add overlays only when the company clearly matches the pattern.

### Typical Usage Path

1. Run `china-stock-research-orchestrator`
2. Let it choose the right core modules
3. Load optional overlays only when the company clearly matches them
4. Merge outputs using the final output contract
