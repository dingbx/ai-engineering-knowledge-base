# AI Models Index

> Detailed specifications and analysis of major AI models

---

## Closed Source Models

### OpenAI
- [GPT-5 Series](openai/gpt-5.md) - Flagship unified model
- [o3/o4-mini](openai/o-series.md) - Dedicated reasoning models

### Anthropic
- [Claude Opus 4.5](anthropic/claude-opus-4.md) - Current flagship

### Google DeepMind
- [Gemini 3](google/gemini-3.md) - Multimodal flagship
- [Gemma 3](google/gemma-3.md) - Open-source efficient models

### xAI
- [Grok 4](xai/grok-4.md) - Multi-agent architecture

---

## Open Source Models

### Meta
- [Llama 4](meta/llama-4.md) - Scout & Maverick variants

### DeepSeek
- [DeepSeek-V3](open-source/deepseek-v3.md) - Efficient MoE architecture
- [DeepSeek-R1](open-source/deepseek-r1.md) - Reasoning model

### Alibaba
- [Qwen3](open-source/qwen3.md) - Strong benchmark performer

### Zhipu AI
- [GLM-5](open-source/glm-5.md) - Coding specialist

---

## Quick Comparison (March 2026)

| Model | Parameters | Context | Open? | Best For |
|-------|-----------|---------|-------|----------|
| GPT-5 | Unknown | ~128K | No | General, reasoning |
| Gemini 3.1 Pro | Unknown | 1M | No | Multimodal, long context |
| Claude Opus 4.5 | Unknown | 200K | No | Reasoning, safety, writing |
| Grok 4 Heavy | 1.7T | 256K | No | Multi-agent reasoning |
| Llama 4 Maverick | 17B/288B | 10M | Yes | Longest context, efficient |
| DeepSeek-V3 | 671B/37B | 128K | Yes | Cost-efficient training |
| Qwen3-235B | 235B | - | Yes | Strong benchmarks |

---

## How to Add a New Model

Create a new file in the appropriate company folder:

```markdown
# Model Name

> One-line description

**Released:** YYYY-MM
**Parameters:** X
**Context:** X tokens

## Architecture
...

## Performance
...

## Resources
- [Official Docs](url)
- [Paper](url)
```
