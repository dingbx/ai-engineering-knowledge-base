# Llama 4

> Meta's open-weight models with record-breaking context length

**Released:** 2025
**License:** Open-weight

---

## Models

| Model | Active Params | Total Params | Context | Experts |
|-------|--------------|--------------|---------|---------|
| Llama 4 Scout | 17B | - | 10M tokens | 16 |
| Llama 4 Maverick | 17B | 288B | 10M tokens | 128 |

---

## Architecture

### Mixture of Experts (MoE)
- Sparse MoE framework
- Only 17B parameters active per token
- Up to 128 experts in Maverick

### Context Length
- **10 million tokens** - longest open-weight LLM
- Enables processing of entire codebases, books, document collections

---

## Performance

| Benchmark | Result |
|-----------|--------|
| LMarena | 1400+ (beats GPT-4o, DeepSeek V3) |

---

## Why It Matters

1. **Accessibility** - Open weights enable self-hosting and customization
2. **Context** - 10M tokens enables new use cases
3. **Efficiency** - MoE keeps inference costs manageable
4. **Competition** - Pushes closed-source providers

---

## Resources

- [Llama Evolution Survey](https://arxiv.org/html/2510.12178v1)
- [Hugging Face meta-llama](https://huggingface.co/meta-llama)
- [llama.com](https://www.llama.com/)

---

*Last updated: March 2026*
