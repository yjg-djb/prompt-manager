---
description: "Vibe Coding：构建、依赖与可回滚升级（需要时智能应用）"
alwaysApply: false
---
# 构建与依赖（Apply Intelligently）

## 依赖升级纪律
- 小步升级：每一步都通过测试与构建。
- 处理 breaking changes：按迁移指南逐条落地，并记录回滚方式。
- 避免无意义改 lockfile；如必须改，说明原因与验证方式。

## 构建自检命令（请填）
- Build：{{build_command}}
- Lint：{{lint_command}}
- Typecheck：{{typecheck_command}}
