# LangChain

> General-purpose framework for building LLM applications with tools, APIs, and data

**GitHub:** 128K+ stars
**Version:** v3.2.1 (2026)
**Website:** [langchain.com](https://langchain.com)

---

## Overview

LangChain is a framework for building applications that combine LLMs with external tools, APIs, and data sources. Its core abstraction is the **chain** — a composable sequence of steps.

---

## Core Concepts

### Chains
Composable sequences that can include:
- Prompt formatting
- LLM calls
- Tool invocations
- Output parsing
- Memory management

### Agents
LLM-powered decision makers that:
- Choose which tools to use
- Execute multi-step plans
- Handle errors and retry

### Tools
Integrations with external services:
- 1,000+ connectors available
- APIs, databases, search engines
- Custom tool creation

---

## Performance (2026)

| Metric | Value |
|--------|-------|
| p99 Latency (1K concurrent) | 45ms |
| Task completion improvement | 35% over v2.5 |

---

## When to Use LangChain

**Good for:**
- Complex multi-step agent workflows
- Broad tool integrations
- Applications needing orchestration logic
- Building autonomous agents

**Consider alternatives for:**
- Simple RAG (LlamaIndex may be better)
- Single-purpose applications

---

## Common Architecture

```
User Query
    │
    ▼
┌─────────────────┐
│   LangChain     │
│   Agent/Chain   │
└─────────────────┘
    │
    ├── LlamaIndex (Knowledge retrieval)
    ├── External APIs
    ├── Databases
    └── Custom tools
    │
    ▼
Response
```

---

## Resources

- [LangChain Documentation](https://docs.langchain.com/)
- [LangChain GitHub](https://github.com/langchain-ai/langchain)

---

*Last updated: March 2026*
