# Cursor Project Rules Pack (for .cursor/rules)

> 目标：把“长期指令”固化为 Cursor 项目规则（Rules），减少每次对话重复交代。
> 你可以按下面的目录创建文件夹，每个文件夹内放一个 RULE.md。

建议目录：
.cursor/rules/
  00-vibe-core/RULE.md
  10-output-format/RULE.md
  20-code-style/RULE.md
  30-testing/RULE.md
  40-git-workflow/RULE.md
  50-security/RULE.md
  60-build-and-deps/RULE.md
  90-manual-pr-review/RULE.md

---

## 00-vibe-core/RULE.md

```md
---
description: "Vibe Coding：核心协作方式（始终应用）"
alwaysApply: true
---
# Vibe Coding 核心规则（Always Apply）

## 基本原则
- 先理解再改：先定位入口/数据流/边界，再做最小改动。
- 小步可回滚：优先拆成小提交/小 diff，避免“一把梭”。
- 不要凭空编造：如果仓库里不存在某文件/函数，先搜索确认。
- 避免无关改动：不要顺手格式化全仓库、不要改无关文件。

## 开发节奏（强制）
1) 先给计划：文件级变更清单 + 风险点 + 测试策略
2) 再实现：按现有架构/约定，不引入无关重构
3) 补测试：至少覆盖关键路径与失败/边界
4) 自检：lint/typecheck/test/build 通过
5) 总结：按输出格式规则输出可验收结果
```

---

## 10-output-format/RULE.md

```md
---
description: "Vibe Coding：统一输出格式（始终应用）"
alwaysApply: true
---
# 统一输出格式（Always Apply）

每次完成一项改动后，用以下结构输出（简洁、可验收）：
- ✅ 一句话总结：完成了什么
- 🧭 变更范围：修改/新增文件清单
- 🧩 关键实现说明：3–7 条
- 🧪 测试：新增/更新测试 + 如何运行
- ⚠️ 风险与回滚：风险点 + 回滚方式
- 📌 未解决项：TODO（若有）
```

---

## 20-code-style/RULE.md

```md
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
- 新增 public API 必须有：用法示例 或 测试覆盖（至少其一，最好两者都有）。

## 可替换区域（把你项目约定写进来）
- Lint/Formatter：{{your_lint_and_formatter}}
- 分层/目录约定：{{your_arch_conventions}}
```

---

## 30-testing/RULE.md

```md
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
```

---

## 40-git-workflow/RULE.md

```md
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
```

---

## 50-security/RULE.md

```md
---
description: "Vibe Coding：安全与隐私（需要时智能应用）"
alwaysApply: false
---
# 安全与隐私（Apply Intelligently）

## 默认原则
- 所有外部输入都要校验/净化（类型、长度、范围、格式）。
- 默认拒绝：鉴权/权限校验要明确，避免越权（IDOR 等）。
- 不在日志/错误信息中输出敏感信息（token、密码、隐私数据）。
- 对外请求注意 SSRF：域名白名单/超时/重试上限/禁止内网地址（按项目能力实现）。

## 如涉及安全改动，必须补
- 1 个恶意输入测试用例
- 1 个权限边界测试用例
```

---

## 60-build-and-deps/RULE.md

```md
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
```

---

## 90-manual-pr-review/RULE.md

```md
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
```

---

## 备注：如何把变量填满
把下列占位符替换成你项目的真实命令/约定：
- {{unit_test_command}} / {{build_command}} / {{lint_command}} / {{typecheck_command}}
- {{your_lint_and_formatter}} / {{your_arch_conventions}}
