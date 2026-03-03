# LlamaIndex

> Data framework for connecting LLMs with private and domain-specific data

**GitHub:** 35K+ stars
**Website:** [llamaindex.ai](https://llamaindex.ai)

---

## Overview

LlamaIndex (formerly GPT Index) specializes in **retrieval-augmented generation (RAG)** — retrieving relevant documents from a knowledge base and feeding them into an LLM's context.

---

## Core Concepts

### Data Connectors
- 160+ connectors for various sources
- Databases, APIs, file systems, cloud storage
- Custom connector creation

### Indices
Structures for organizing data:
- Vector indices
- Tree indices
- Keyword indices
- Knowledge graphs

### Query Engines
Process user queries:
- Route to appropriate index
- Retrieve relevant context
- Generate grounded responses

---

## Performance (2026)

| Metric | Value |
|--------|-------|
| p99 Latency (1K concurrent) | 30ms |
| Efficiency | Optimized for data retrieval |

---

## When to Use LlamaIndex

**Good for:**
- RAG applications over your own data
- Document Q&A systems
- Knowledge base search
- Data-augmented agents

**Consider alternatives for:**
- Complex multi-step workflows (use LangChain)
- Simple chatbots without data needs

---

## Common Use Cases

| Use Case | Approach |
|----------|----------|
| Search Engine | Vector index + semantic search |
| Document Q&A | Load docs → index → query engine |
| Enterprise Knowledge | Multiple indices + routing |

---

## Hybrid Architecture

Many production systems combine LlamaIndex + LangChain:

```
┌─────────────────────────────────────┐
│         LangChain Agent             │
│         (Orchestration)             │
└─────────────────────────────────────┘
              │
              ▼
┌─────────────────────────────────────┐
│      LlamaIndex Query Engine        │
│      (Knowledge Retrieval)          │
└─────────────────────────────────────┘
              │
              ▼
┌─────────────────────────────────────┐
│         Document Store              │
│    (Your private data)              │
└─────────────────────────────────────┘
```

---

## Resources

- [LlamaIndex Documentation](https://docs.llamaindex.ai/)
- [LlamaIndex GitHub](https://github.com/run-llama/llama_index)

---

*Last updated: March 2026*
