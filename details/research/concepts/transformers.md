# Transformer Architecture

> The foundational architecture behind all modern LLMs

---

## Overview

Transformers use **self-attention** to process sequences in parallel, replacing the sequential processing of RNNs/LSTMs.

---

## Core Components

### 1. Self-Attention
```
Attention(Q, K, V) = softmax(QK^T / √d_k) V
```
- **Q (Query)**: What am I looking for?
- **K (Key)**: What do I contain?
- **V (Value)**: What do I actually say?

### 2. Multi-Head Attention
- Multiple attention heads learn different patterns
- Heads concatenated and projected
- Typical: 8-128 heads

### 3. Feed-Forward Networks
- Two linear layers with activation
- Applied position-wise
- Expands then contracts dimension

### 4. Layer Normalization
- Stabilizes training
- Applied before or after each sublayer

### 5. Positional Encoding
- Transformers don't inherently understand order
- Position info added to embeddings
- Sinusoidal or learned

---

## Architecture Variants

| Variant | Structure | Examples |
|---------|-----------|----------|
| Encoder-only | Bidirectional attention | BERT |
| Decoder-only | Causal (left-to-right) attention | GPT, Llama, Claude |
| Encoder-Decoder | Both components | T5, BART |

Modern LLMs are predominantly **decoder-only**.

---

## The Architecture Stack

```
┌─────────────────────────────────────────────────────────┐
│              Applications (ChatGPT, Claude, etc.)        │
├─────────────────────────────────────────────────────────┤
│     Fine-tuning Layer                                    │
│     • SFT (Supervised Fine-Tuning)                      │
│     • RLHF (RL from Human Feedback)                     │
│     • Constitutional AI                                  │
├─────────────────────────────────────────────────────────┤
│              Base Model Architecture                     │
│   ┌─────────────────────────────────────────────────┐   │
│   │  Transformer (Self-Attention Mechanism)          │   │
│   │  ├── MoE (Mixture of Experts)                   │   │
│   │  ├── MLA (Multi-head Latent Attention)          │   │
│   │  └── Multi-Token Prediction                     │   │
│   └─────────────────────────────────────────────────┘   │
├─────────────────────────────────────────────────────────┤
│                   Pre-training Data                      │
│              (Trillions of tokens from internet)         │
└─────────────────────────────────────────────────────────┘
```

---

## Key Innovations Since 2017

| Innovation | Purpose |
|------------|---------|
| RoPE | Better positional encoding for long context |
| Flash Attention | Memory-efficient attention |
| MoE | Sparse activation for efficiency |
| MLA | Compressed KV cache |
| GQA | Grouped query attention |

---

*Last updated: March 2026*
