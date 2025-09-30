# ChoreoAtlas 变更守护（Change Guard）

[English](guard.en.md) | [中文](#)

## 目的
确保所有改动在**版本管理**与**审核**下进行；保护"只读仓库"（CE/Pro），避免误改。

## 只读仓库（不可直接改动）
- **choreoatlas2025/cli** - CE 版核心仓库

> 对只读仓库：只允许 **Issue** 或来自 **fork 的 Draft PR**，禁止直接向主仓库推送代码。

## 本周变更原则
- ✅ **新增优先**：新增目录/文件（examples、flows、tools、scripts、docs、assets、.github/workflows）。
- ⛔ **禁止覆盖**：未经豁免，不改现有文件的语义或删除内容。
- 🔁 **可回滚**：每个里程碑 PR 合并后打 tag（`milestone-YYYYMMDD-n`）。

## 标准改动流程
1. 在目标仓库开分支（或 fork）；
2. 提交变更，使用 PR 模板填写 **复现 / 证据 / KPI**；
3. 通过 `CODEOWNERS` 指定的 Review；
4. CI 绿灯后合并；
5. 打里程碑 tag。

## 紧急"豁免改动"流程（只在必要时）
1. 开 Issue：`Change Exemption: <scope>`，说明影响面、回滚方式；
2. 开 **小粒度 PR**（仅影响一处），并附 `revert.sh` 或回滚指南；
3. 由 @youming1970 审批通过后合并；
4. 48 小时内复盘并还原到"新增优先"的正轨。

## 联系
- 变更审批人：@youming1970
- 安全年限：所有讨论统一在 `community` 仓库 Issues 中留痕。