---
description: "Vibe Coding：提交信息、PR 说明与变更粒度（需要时智能应用）"
alwaysApply: false
---
# Git / PR 工作流（Apply Intelligently）

## 提交粒度
- 一个提交做一件事：避免把重构、功能、格式化、依赖升级混在一起。
- 每步都可构建、可测试、可回滚。

## 提交信息建议
- 说明“做了什么 + 为什么”，必要时带影响范围（scope）。

## PR 描述必须包含
- Summary（做了什么）
- Changes（文件/模块级清单）
- Tests（跑了什么、怎么跑）
- Risks & Rollback（风险与回滚）
