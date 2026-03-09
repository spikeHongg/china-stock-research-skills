# 发布执行清单 / Publish Checklist

[中文](#中文) | [English](#english)

## 中文

这份文件是实际发布时可以按顺序执行的 checklist。

## 一、本地仓库准备

1. 确认当前目录文件齐全：`README.md`、`INSTALL.md`、`SKILLS.md`、`CONTRIBUTING.md`、`ROADMAP.md`、`CHANGELOG.md`、`GITHUB_PUBLISHING.md`、`RELEASE_ASSETS.md`
2. 检查 skills 是否可发现：

```bash
bunx skills add . --list
```

3. 如果还没有初始化 git：

```bash
git init
git add .
git commit -m "add initial China stock research skills pack"
```

## 二、创建 GitHub 仓库

1. 在 GitHub 创建新仓库
2. 仓库名建议使用：`china-stock-research-skills`
3. 在仓库设置中填写：
   - Description：使用 `RELEASE_ASSETS.md` 中的 About 文案
   - Topics：使用 `RELEASE_ASSETS.md` 中的 topics 建议

## 三、推送代码

假设远程仓库地址为 `<your-remote-url>`：

```bash
git remote add origin <your-remote-url>
git branch -M main
git push -u origin main
```

## 四、创建首个版本

1. 创建 tag：

```bash
git tag v0.1.0
git push origin v0.1.0
```

2. 到 GitHub Release 页面新建 release
3. 标题建议：`v0.1.0 - 首个开源版本`
4. 正文直接复制 `RELEASE_ASSETS.md` 中的中文 release 正文

## 五、发布后验证

在一个新的目录中测试远程安装：

```bash
mkdir -p /tmp/a-share-skills-test && cd /tmp/a-share-skills-test
bunx skills add <owner>/<repo> --list

发布当前仓库时，对应命令是：

```bash
bunx skills add spikeHongg/china-stock-research-skills --list
```
```

确认能看到全部 7 个 skills。

然后再测试一次使用入口：

```text
使用 china-stock-research-orchestrator skill 分析这家 A 股公司，识别主要分析模式，选择需要调用的模块，并默认使用中文输出。
```

## 六、建议的首批维护动作

1. 创建并 pin 两个 issues，可直接使用 `RELEASE_ASSETS.md` 中的标题与正文
2. 关注外部用户对安装流程与 examples 的反馈
3. 若发现远程安装说明不够清晰，优先更新 `INSTALL.md`

## English

This file is a step-by-step execution checklist for the actual GitHub launch.

## 1. Prepare the Local Repository

1. Confirm the key files are present: `README.md`, `INSTALL.md`, `SKILLS.md`, `CONTRIBUTING.md`, `ROADMAP.md`, `CHANGELOG.md`, `GITHUB_PUBLISHING.md`, `RELEASE_ASSETS.md`
2. Check that the skills are discoverable:

```bash
bunx skills add . --list
```

3. If git is not initialized yet:

```bash
git init
git add .
git commit -m "add initial China stock research skills pack"
```

## 2. Create the GitHub Repository

1. Create a new repository on GitHub
2. Recommended name: `china-stock-research-skills`
3. In GitHub settings, fill in:
   - Description: use the About text from `RELEASE_ASSETS.md`
   - Topics: use the suggested topics from `RELEASE_ASSETS.md`

## 3. Push the Code

Assuming the remote URL is `<your-remote-url>`:

```bash
git remote add origin <your-remote-url>
git branch -M main
git push -u origin main
```

## 4. Create the First Release

1. Create the tag:

```bash
git tag v0.1.0
git push origin v0.1.0
```

2. Open the GitHub Releases page and create a release
3. Suggested title: `v0.1.0 - Initial open-source release`
4. Paste the release body from `RELEASE_ASSETS.md`

## 5. Post-Publish Verification

In a fresh directory, test remote install:

```bash
mkdir -p /tmp/a-share-skills-test && cd /tmp/a-share-skills-test
bunx skills add <owner>/<repo> --list

For this repository, the concrete command is:

```bash
bunx skills add spikeHongg/china-stock-research-skills --list
```
```

Confirm that all 7 skills are visible.

Then test the entry prompt:

```text
Use the china-stock-research-orchestrator skill to analyze this A-share company, identify the main analysis patterns, select the required modules, and default all outputs to Simplified Chinese.
```

## 6. Suggested First Maintenance Steps

1. Create and pin the two issues suggested in `RELEASE_ASSETS.md`
2. Watch for feedback on the install flow and examples
3. If remote install instructions cause confusion, update `INSTALL.md` first
