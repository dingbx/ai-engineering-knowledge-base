# Developer Tools Index

> Frameworks, coding assistants, and autonomous agents for AI development

---

## Frameworks

For building LLM applications:

| Framework | Stars | Best For |
|-----------|-------|----------|
| [LangChain](frameworks/langchain.md) | 128K+ | Agent orchestration, complex workflows |
| [LlamaIndex](frameworks/llamaindex.md) | 35K+ | RAG applications, data retrieval |

**Common pattern**: Use LlamaIndex as knowledge layer, LangChain as orchestration layer.

---

## Coding Assistants

AI tools for software development:

| Tool | Users/Stars | Strength |
|------|-------------|----------|
| [GitHub Copilot](coding-assistants/copilot.md) | 1.8M paying | Broad integration, Agent Mode |
| [Cursor](coding-assistants/cursor.md) | Popular | AI-native IDE, large codebases |
| [Claude Code](coding-assistants/claude-code.md) | - | 50K+ LOC refactors, 200K context |

**Usage pattern**: 26% of developers use multiple tools for different tasks.

---

## Autonomous Agents

| Project | Stars | Status |
|---------|-------|--------|
| [OpenClaw](agents/openclaw.md) | 234K+ | Viral, security concerns |

---

## How to Add

Create file in appropriate subfolder:

```markdown
# Tool Name

> One-line description

**Category:** Framework / Coding Assistant / Agent
**Website:** [url](url)
**GitHub:** [repo](url)

## Overview
...

## Key Features
...

## When to Use
...
```
