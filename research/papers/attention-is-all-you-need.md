# Attention Is All You Need

> The foundational Transformer paper that started the modern LLM era

**Authors:** Vaswani et al. (Google)
**Published:** 2017
**Link:** [arXiv:1706.03762](https://arxiv.org/abs/1706.03762)

---

## Key Contributions

1. Introduced the **Transformer architecture**
2. Replaced recurrence with **self-attention**
3. Enabled massive parallelization in training
4. Foundation for GPT, BERT, and all modern LLMs

---

## Main Ideas

### Self-Attention Mechanism
- Each position attends to all positions in previous layer
- Computes relevance scores between all token pairs
- Enables capturing long-range dependencies

### Multi-Head Attention
- Multiple attention "heads" learn different relationships
- Heads are concatenated and projected
- Richer representations than single attention

### Positional Encoding
- Transformers have no inherent position sense
- Sinusoidal encodings added to embeddings
- Allows model to use sequence order

### Encoder-Decoder Structure
- Encoder processes input sequence
- Decoder generates output autoregressively
- Cross-attention connects them

---

## Architecture Diagram

```
Input → Embedding + Positional Encoding
      → N × (Multi-Head Attention → Add & Norm → FFN → Add & Norm)
      → Output
```

---

## Why It Matters

Every modern LLM is built on this foundation:
- GPT series (decoder-only)
- BERT (encoder-only)
- T5 (encoder-decoder)

Understanding attention is prerequisite for understanding any current model.

---

## Key Sections to Read

- **Section 3.2**: Scaled Dot-Product Attention
- **Section 3.3**: Multi-Head Attention

---

*Last updated: March 2026*
