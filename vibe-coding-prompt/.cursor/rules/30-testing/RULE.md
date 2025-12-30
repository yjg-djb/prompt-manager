---
description: "Vibe Coding：测试策略与回归要求（匹配测试文件时应用）"
alwaysApply: false
globs:
  - "**/__tests__/**"
  - "**/tests/**"
  - "**/*.test.*"
  - "**/*.spec.*"
---
# 测试策略（Apply to Specific Files）

## 最小要求
- 每个 bugfix 至少补 1 个回归测试（修复前失败，修复后通过）。
- 每个 feature 至少覆盖：成功路径 + 1 个失败/边界路径。

## 稳定性（避免 flaky）
- 避免依赖真实时间/随机/外部网络；必要时使用假时钟/固定种子/mocks。
- 避免顺序敏感断言；并发场景要明确等待条件。

## 项目命令（请填）
- 单测：{{unit_test_command}}
- 集成：{{integration_test_command}}
- E2E：{{e2e_test_command}}
