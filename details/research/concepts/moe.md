# Mixture of Experts (MoE)

> Architecture that enables massive models with efficient inference

---

## The Problem

Large models = better performance, but:
- Training costs scale with parameters
- Inference costs scale with parameters
- Memory requirements scale with parameters

**MoE solution**: Have many parameters, but only use some per token.

---

## How It Works

```
Input Token
    │
    ▼
┌─────────┐
│ Router  │ ─── Decides which experts to use
└─────────┘
    │
    ▼ (top-k selection)
┌─────────┬─────────┬─────────┬─────────┐
│Expert 1 │Expert 2 │Expert 3 │Expert N │
└─────────┴─────────┴─────────┴─────────┘
    │         │
    ▼         ▼
  Output (weighted combination)
```

### Key Components

1. **Router/Gating Network**: Learns which experts handle which inputs
2. **Experts**: Typically feed-forward networks
3. **Top-k Selection**: Usually k=1 or k=2 experts per token

---

## Real-World Examples

| Model | Total Params | Active Params | Experts |
|-------|-------------|---------------|---------|
| DeepSeek-V3 | 671B | 37B | - |
| Llama 4 Maverick | 288B | 17B | 128 |
| Llama 4 Scout | - | 17B | 16 |
| GLM-5 | 744B | 44B | - |

---

## Benefits

1. **Scale without proportional cost**: 671B params but only 37B compute
2. **Specialization**: Experts can learn different skills
3. **Efficiency**: Inference cost of smaller model

## Challenges

1. **Load balancing**: Ensuring all experts get used
2. **Communication**: In distributed training
3. **Routing collapse**: All tokens going to few experts

---

## DeepSeek's Innovation

**Auxiliary-Loss-Free Load Balancing**:
- Traditional MoE adds loss term to encourage balanced routing
- DeepSeek found a way to balance without auxiliary loss
- Results in better overall performance

---

## When to Use MoE

- Very large scale models (100B+ total params)
- When you need capacity but inference budget is limited
- When different inputs genuinely need different processing

---

*Last updated: March 2026*
