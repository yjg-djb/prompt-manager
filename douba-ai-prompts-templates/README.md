# AI Prompts Templates

AI技术落地提示词模板库 - 专为AI应用开发设计的结构化提示词模板集合。

## 目录结构

```
ai-prompts-templates/
├── flowise/                    # Flowise相关模板
│   ├── flowise-node-troubleshooting.md    # 节点配置问题排查
│   ├── flowise-ollama-integration.md      # Flowise与Ollama集成配置
│   └── flowise-rag-workflow.md            # RAG知识库问答流程搭建
│
├── ollama/                     # Ollama相关模板
│   ├── ollama-model-finetuning.md         # 模型微调需求梳理
│   ├── ollama-api-code-generation.md      # 模型调用代码生成
│   └── ollama-connection-troubleshooting.md # 服务连接问题排查
│
├── fastapi-integration/        # FastAPI集成模板
│   ├── fastapi-ollama-api-development.md  # FastAPI封装Ollama接口开发
│   ├── fastapi-performance-optimization.md # 接口性能优化
│   └── fastapi-test-case-generation.md    # 接口测试用例生成
│
├── document-conversion/        # 文档格式转换模板
│   ├── pdf-to-markdown-tools.md           # PDF转Markdown工具选型
│   ├── ppt-to-latex-conversion.md         # PPT转LaTeX格式转换
│   └── document-standardization.md        # 技术文档格式规范化
│
└── technical-design/           # 技术方案设计模板
    ├── ai-knowledge-base-system-design.md # AI知识库问答系统方案设计
    ├── offline-deployment-guide.md        # 开源AI应用离线部署方案
    └── technical-challenge-resolution.md  # 技术难点拆解与解决方案
```

## 使用说明

每个模板文件包含以下结构：

1. **场景说明** - 模板适用的具体场景
2. **核心用途** - 模板能解决的问题
3. **提示词模板** - 结构化的输入框架
4. **期望输出要求** - 期望AI返回的内容格式
5. **输出格式约束** - 对输出格式的具体要求
6. **使用示例** - 完整的使用案例

## 模板分类

| 分类 | 文件数 | 适用场景 |
|------|--------|----------|
| Flowise相关 | 3 | Flowise节点配置、集成、RAG流程搭建 |
| Ollama相关 | 3 | 模型微调、代码生成、问题排查 |
| FastAPI集成 | 3 | API开发、性能优化、测试用例 |
| 文档格式转换 | 3 | PDF/PPT转换、文档规范化 |
| 技术方案设计 | 3 | 系统架构、离线部署、技术难点 |

## 最佳实践

1. **填写完整信息**：模板中的每个字段都会影响AI的输出质量
2. **提供具体示例**：越具体的描述，输出越精准
3. **明确约束条件**：技术栈、资源限制等信息有助于获得可落地的方案
4. **使用格式约束**：指定输出格式可确保答案结构清晰

## 版本信息

- 版本：1.0.0
- 更新日期：2025-12-30
