---
description: "Vibe Coding：代码风格与可维护性（匹配源码文件时应用）"
alwaysApply: false
globs:
  - "**/*.ts"
  - "**/*.tsx"
  - "**/*.js"
  - "**/*.jsx"
  - "**/*.py"
  - "**/*.go"
  - "**/*.java"
---
# 代码风格与可维护性（Apply to Specific Files）

## 通用
- 命名清晰：避免缩写堆叠；必要时补注释解释业务语义。
- 控制复杂度：长函数拆分；重复逻辑抽公共方法/模块。
- 错误处理统一：不要吞错；错误信息对调用方友好、对日志可定位。

## 变更纪律
- 不做“顺手重构”；需要重构就单独说明原因与范围。
- 新增 public API 必须有：用法示例或测试覆盖（至少其一，最好两者都有）。

## 可替换区域（把你项目约定写进来）
- Lint/Formatter：{{your_lint_and_formatter}}
- 分层/目录约定：{{your_arch_conventions}}
