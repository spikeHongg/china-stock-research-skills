# 安装 / Install

[中文](#中文) | [English](#english)

## 中文

本仓库基于 open skills CLI 使用，面向中国股票、尤其是 A股 / A-share 研究场景，推荐使用 `bunx skills add` 进行安装与检查。

### 前置条件

- 已安装 `bun`
- 已安装支持 skills 的 agent 环境

### 从 GitHub 安装

可直接复制的远程安装命令：

```bash
bunx skills add spikeHongg/china-stock-research-skills
```

如果想先看有哪些 skills：

```bash
bunx skills add spikeHongg/china-stock-research-skills --list
```

### 从本地克隆目录安装

在仓库根目录执行：

```bash
bunx skills add . --list
```

确认可发现后，再安装：

```bash
bunx skills add .
```

### 如何验证安装成功

安装后，应当能看到以下 7 个 skills：

- `china-stock-research-orchestrator`
- `strategy-business-transition`
- `business-decomposition-order-quality`
- `financial-health`
- `industry-competition-moat`
- `risk-warning-catalysts`
- `valuation-investment-strategy`

### 第一次使用

建议从总控母 skill 开始：

```text
使用 china-stock-research-orchestrator skill 分析这家中国上市公司，尤其按 A股 / A-share 研究语境识别主要分析模式，选择需要调用的模块，并返回一份带可访问来源链接的研究框架。所有中间与最终输出默认使用中文。
```

### 常见问题

#### 找不到 skills

- 确认本地安装时，你是在仓库根目录执行命令
- 确认 `skills/` 下仍然存在有效的 `SKILL.md`

#### 安装了但不知道怎么开始

- 先从 `china-stock-research-orchestrator` 开始
- 再查看 `SKILLS.md` 和 `examples/quickstart-prompts.md`

#### 远程安装路径容易写错

- 优先直接复制：`bunx skills add spikeHongg/china-stock-research-skills`
- 本地调试时优先使用 `bunx skills add .`，不要先写很长的绝对路径

## English

This repository is designed to work with the open skills CLI and is especially natural for China stock and A-share research workflows. The recommended install path is `bunx skills add`.

### Prerequisites

- `bun` installed
- a compatible agent environment that supports skills

### Install From GitHub

Copy-paste remote install command:

```bash
bunx skills add spikeHongg/china-stock-research-skills
```

To inspect available skills before installing:

```bash
bunx skills add spikeHongg/china-stock-research-skills --list
```

### Install From a Local Clone

From the repository root:

```bash
bunx skills add . --list
```

Then install from the same local path:

```bash
bunx skills add .
```

### Verify Installation

After installation, you should be able to see these 7 skills:

- `china-stock-research-orchestrator`
- `strategy-business-transition`
- `business-decomposition-order-quality`
- `financial-health`
- `industry-competition-moat`
- `risk-warning-catalysts`
- `valuation-investment-strategy`

### First Use

Start with the orchestrator:

```text
Use the china-stock-research-orchestrator skill to analyze this China-listed company, especially in an A-share workflow context, identify the main analysis patterns, choose the required modules, and return a source-backed research framework. Default all intermediate and final outputs to Simplified Chinese.
```

### Common Problems

#### No skills found

- Make sure you are running the command from the repository root when installing locally
- Make sure valid `SKILL.md` files still exist under `skills/`

#### Installed but hard to know where to start

- Start with `china-stock-research-orchestrator`
- Then review `SKILLS.md` and `examples/quickstart-prompts.md`

#### Remote install path confusion

- Use the copy-ready command first: `bunx skills add spikeHongg/china-stock-research-skills`
- If you are testing locally, use `bunx skills add .` instead of a long absolute path
