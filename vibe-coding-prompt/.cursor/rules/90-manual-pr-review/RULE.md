---
description: "PR Review 模式：严格评审清单（仅手动触发）"
alwaysApply: false
---
# PR Review 模式（Apply Manually）

当我在对话中明确要求“进入 PR Review 模式/严格评审”时：
- 必须按优先级评审：正确性 → 架构 → 可维护性 → 测试 → 性能 → 安全 → DX
- 明确区分：
  - 🧨 Blocking：必须改，否则不建议合并
  - 🧹 Non-blocking：建议改，可后续
- 每条建议必须包含：原因 + 可执行修改方向
