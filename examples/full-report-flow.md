# Full Report Flow

## Orchestrator-First Flow

1. Start with the orchestrator.
2. Let it select the right patterns and modules.
3. Run the selected core modules.
4. Merge the outputs into one framework.

## Example Prompt

```text
使用 china-stock-research-orchestrator skill 按截至今天的公开信息分析这家 A 股公司。先识别主要分析模式，再选择必须调用的模块和可选 overlay，最后返回一份合并后的研究框架，结构包含：公司概览与路由决策、事实、解读、待验证问题、监测指标、情景与估值钩子、来源附录。所有中间与最终输出默认使用中文。
```

## Expected Behavior

- The workflow should not assume a sector too early.
- The workflow should explain why each module was selected.
- The workflow should keep source-backed facts separate from interpretation.
