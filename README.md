# 🎯 Prompt Manager

<p align="center">
  <strong>A curated collection of AI prompt templates for developers and professionals</strong>
</p>

<p align="center">
  <a href="#features">Features</a> •
  <a href="#quick-start">Quick Start</a> •
  <a href="#template-categories">Templates</a> •
  <a href="#usage">Usage</a> •
  <a href="#contributing">Contributing</a>
</p>

---

## ✨ Features

- 📚 **Multi-scenario Coverage** - Templates for coding, research, legal consulting, and technical design
- 🔧 **Production-ready** - Battle-tested prompts optimized for real-world tasks
- 🎨 **Modular Design** - Mix and match templates for complex workflows
- 🤖 **Multi-platform Support** - Compatible with Claude, Cursor, Doubao, and more

---

## 📁 Template Categories

```
prompt-manager/
├── claude-prompt/              # Claude global prompt templates
│   ├── 00_设计原则.md            # Prompt design principles
│   ├── 01_通用基础模板.md         # General purpose template
│   ├── 02_法律咨询模板.md         # Legal consulting
│   ├── 03_学术研究模板.md         # Academic research
│   ├── 04_技术架构模板.md         # Technical architecture
│   ├── 05_编程开发模板.md         # Programming & development
│   └── 06_组合使用指南.md         # Combination guide
│
├── vibe-coding-prompt/         # Vibe Coding prompts for Cursor IDE
│   ├── prompts/vibe-coding/    # 10 coding workflow templates
│   │   ├── 01-feature-impl.md    # Feature implementation
│   │   ├── 02-bugfix.md          # Bug fixing
│   │   ├── 03-refactor.md        # Code refactoring
│   │   ├── 04-add-tests.md       # Test writing
│   │   ├── 05-pr-review.md       # PR review
│   │   ├── 06-performance.md     # Performance optimization
│   │   ├── 07-security-hardening.md  # Security hardening
│   │   ├── 08-dependency-upgrade.md  # Dependency management
│   │   ├── 09-api-design.md      # API design
│   │   └── 10-docs-adr.md        # Documentation & ADR
│   └── .cursor/rules/          # Cursor IDE rules
│
└── douba-ai-prompts-templates/ # AI tech implementation templates
    ├── flowise/                # Flowise workflow templates
    ├── ollama/                 # Ollama model templates
    ├── fastapi-integration/    # FastAPI + AI integration
    ├── document-conversion/    # Document format conversion
    └── technical-design/       # Technical design patterns
```

---

## 🚀 Quick Start

### Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/prompt-manager.git
cd prompt-manager
```

### Choose your template

| Use Case | Recommended Templates |
|----------|----------------------|
| Coding with Cursor IDE | `vibe-coding-prompt/` |
| General AI conversations | `claude-prompt/` |
| AI application development | `douba-ai-prompts-templates/` |

---

## 📖 Usage

### 1. Claude Prompt Templates

Perfect for professional consulting scenarios:

```markdown
# Example: Using the legal consulting template

1. Open `claude-prompt/02_法律咨询模板.md`
2. Replace [placeholders] with your specific case details
3. Copy the entire template to Claude
4. Iterate based on the response
```

### 2. Vibe Coding Prompts (Cursor IDE)

For AI-assisted development workflow:

```bash
# Copy rules to your project
cp -r vibe-coding-prompt/.cursor/rules/ your-project/.cursor/rules/

# Use prompts in Cursor chat
# Copy content from prompts/vibe-coding/01-feature-impl.md
```

### 3. AI Tech Implementation Templates

For building AI applications with Flowise, Ollama, FastAPI:

```markdown
# Example: Building a RAG system

1. Open `douba-ai-prompts-templates/flowise/flowise-rag-workflow.md`
2. Fill in your project requirements
3. Get step-by-step implementation guidance
```

---

## 📋 Template Details

### Claude Prompt Templates

| Template | Description | Best For |
|----------|-------------|----------|
| Design Principles | Core principles for effective prompts | Everyone |
| General Template | Universal consulting framework | Any professional task |
| Legal Consulting | Labor disputes, contracts, IP | Legal professionals |
| Academic Research | Paper writing, methodology | Researchers, students |
| Tech Architecture | System design, tech selection | Architects, tech leads |
| Programming | Code implementation, demos | Developers |

### Vibe Coding Prompts

| Template | Description |
|----------|-------------|
| Feature Implementation | New feature development workflow |
| Bug Fix | Systematic debugging approach |
| Refactor | Code improvement patterns |
| Add Tests | Test coverage enhancement |
| PR Review | Code review guidelines |
| Performance | Optimization strategies |
| Security Hardening | Security best practices |
| Dependency Upgrade | Safe dependency management |
| API Design | RESTful API design patterns |
| Docs & ADR | Documentation and decision records |

### AI Tech Templates

| Category | Templates |
|----------|-----------|
| Flowise | Node troubleshooting, Ollama integration, RAG workflow |
| Ollama | Model finetuning, API code generation, connection troubleshooting |
| FastAPI | API development, performance optimization, test generation |
| Document Conversion | PDF to Markdown, PPT to LaTeX, document standardization |
| Technical Design | Knowledge base system, offline deployment, challenge resolution |

---

## 💡 Best Practices

1. **Read the design principles first** - Understand what makes a good prompt
2. **Start with the base template** - Add domain-specific requirements gradually
3. **Be specific with constraints** - Vague requests get vague responses
4. **Require citations** - Always ask for sources in professional domains
5. **Iterate and refine** - Use follow-up questions to improve output

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/new-template`)
3. Commit your changes (`git commit -m 'Add new template for XYZ'`)
4. Push to the branch (`git push origin feature/new-template`)
5. Open a Pull Request

### Template Guidelines

- Use clear, descriptive filenames
- Include usage examples in each template
- Follow the existing structure and formatting
- Add both English and Chinese versions when possible

---

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- Vibe Coding prompts inspired by modern AI-assisted development practices
- Claude prompt templates based on Anthropic's best practices
- Community contributions and feedback

---

<p align="center">
  <sub>Made with ❤️ for the AI development community</sub>
</p>
