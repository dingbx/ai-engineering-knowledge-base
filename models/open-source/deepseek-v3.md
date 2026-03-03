# DeepSeek-V3 / DeepSeek-R1

> Efficient frontier models that proved high-quality training doesn't require $100M+

---

## Models

| Model | Total Params | Active Params | Training Cost |
|-------|-------------|---------------|---------------|
| DeepSeek-V3 | 671B | 37B per token | ~$6M |
| DeepSeek-R1 | 671B | 37B per token | Fine-tuned from V3 |

---

## Key Innovations

### Multi-head Latent Attention (MLA)
- Compresses key-value cache
- Enables longer context with less memory
- Critical for efficiency at scale

### DeepSeekMoE
- Auxiliary-loss-free load balancing
- Better expert utilization than standard MoE

### Multi-Token Prediction
- Training objective predicts multiple tokens
- Improves sample efficiency

---

## Training Details

| Aspect | Value |
|--------|-------|
| Training Tokens | 14.8T |
| GPUs | 2048 H800 |
| Duration | ~2 months |
| Loss Spikes | None |
| Cost | ~$6M (2.788M H800 GPU hours) |

---

## DeepSeek-R1 Specifics

### RLVR (RL with Verifiable Rewards)
- Trains reasoning without expensive human feedback
- Uses math/code problems with verifiable answers

### R1-Zero
- Pure RL without supervised fine-tuning
- Demonstrates reasoning emergence from RL alone

### GRPO Algorithm
- Group Relative Policy Optimization
- Efficient RL training method

---

## Impact

Proved that frontier-quality models can be trained for ~$6M instead of $100M+, democratizing access to advanced AI development.

---

## Resources

- [DeepSeek-V3 Technical Report](https://arxiv.org/pdf/2412.19437)
- [DeepSeek-R1 Paper](https://arxiv.org/pdf/2501.12948)
- [Technical Analysis - Graphcore](https://graphcore-research.github.io/deepseek/)
- [Technical Tour - Sebastian Raschka](https://magazine.sebastianraschka.com/p/technical-deepseek)

---

*Last updated: March 2026*
