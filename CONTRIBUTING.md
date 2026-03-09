# 贡献指南 / Contributing

[中文](#中文) | [English](#english)

## 中文

感谢你考虑为这个仓库贡献内容。

### 欢迎的贡献类型

- 提升现有 skills 的清晰度和边界感
- 增加新的、可复用的 A 股研究 overlays
- 改进来源与引用规范
- 增加能帮助新用户上手的 examples
- 修复会模糊 `事实`、`解读`、`待验证问题` 边界的措辞

### 提交 PR 前请注意

- 保持主流程是“通用 A 股研究框架”
- 优先沉淀可复用模式，不要把流程写死到单一公司或单一行业
- 只要新增来源指引，就补充可访问链接
- `SKILL.md` 保持简洁，把细节尽量下沉到 `references/`
- 默认输出语言应为简体中文，除非用户明确要求其他语言

### Skill 结构要求

每个 skill 至少应包含：

- 合法 frontmatter，其中必须有 `name` 和 `description`
- 清晰的 `When to Use`
- 清晰的 `Workflow`
- 清晰的 `Required Output`
- 清晰的 `Boundaries`

### 引用要求

- 每条关键事实都应指向可访问来源链接
- 官方披露优先于媒体或评论
- 不要把没有证据支撑的推断写进 `事实`

### 本地检查

在仓库根目录执行：

```bash
bunx skills add . --list
python3 ~/.config/opencode/skills/skill-creator/scripts/quick_validate.py skills/<skill-name>
```

### 范围建议

优先：

- 小步、可组合的改进
- 一次新增一个 overlay
- 围绕可复用模式设计 examples

避免：

- 把仓库改造成交易系统
- 依赖私有数据库或付费终端
- 在主流程里硬编码某只股票或某个行业

## English

Thanks for considering a contribution.

### Good Contribution Types

- Improve clarity and boundaries of existing skills
- Add reusable overlays for common A-share research patterns
- Improve source and citation standards
- Add examples that help first-time users
- Fix wording that blurs the boundaries between `Facts`, `Interpretation`, and `Open Questions`

### Before Opening a PR

- Keep the core workflow generic for A-share stock research
- Prefer reusable patterns over one-company or one-industry hardcoding
- Add accessible source links when introducing new source guidance
- Keep `SKILL.md` files concise and push detail into `references/`
- Default output language should remain Simplified Chinese unless the user explicitly requests another language

### Skill Structure Expectations

Every skill should include:

- valid frontmatter with `name` and `description`
- clear `When to Use`
- clear `Workflow`
- clear `Required Output`
- clear `Boundaries`

### Citation Expectations

- Every key fact should point to an accessible source link
- Official disclosures should outrank commentary or media
- Do not merge unsupported inference into `Facts`

### Local Checks

From the repository root:

```bash
bunx skills add . --list
python3 ~/.config/opencode/skills/skill-creator/scripts/quick_validate.py skills/<skill-name>
```

### Scope Guidance

Prefer:

- small, composable improvements
- one new overlay at a time
- examples based on reusable patterns

Avoid:

- turning the pack into a trading system
- depending on private databases or paid terminals
- hardcoding one stock or one sector into the main workflow
