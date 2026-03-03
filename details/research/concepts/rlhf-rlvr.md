# RLHF vs RLVR

> How models learn to be helpful, harmless, and honest

---

## The Training Pipeline

```
1. Pre-training (Self-supervised)
   └── Predict next token on trillions of tokens
   └── Creates "base model" with world knowledge

2. Supervised Fine-Tuning (SFT)
   └── Train on instruction-response pairs
   └── Teaches model to follow instructions

3. Reinforcement Learning  ← RLHF or RLVR
   └── Optimizes for human preferences or verifiable rewards
```

---

## RLHF: Reinforcement Learning from Human Feedback

### How It Works

1. **Collect comparisons**: Humans rank model outputs
2. **Train reward model**: Learns to predict human preferences
3. **RL optimization**: Model optimizes against reward model

### Pros
- Works for subjective qualities (helpfulness, tone)
- Can shape complex behaviors

### Cons
- **Expensive**: Requires lots of human labeling
- **Noisy**: Human preferences vary
- **Reward hacking**: Model can game the reward model

---

## RLVR: Reinforcement Learning with Verifiable Rewards

### How It Works

1. **Use verifiable tasks**: Math problems, code execution
2. **Automatic verification**: Check if answer is correct
3. **RL optimization**: Reward correct answers, penalize incorrect

### Pros
- **No human labeling needed**
- **Objective rewards**: Right or wrong, no ambiguity
- **Scales infinitely**: Generate unlimited training problems

### Cons
- Only works for verifiable domains
- May not transfer to subjective tasks

---

## DeepSeek-R1's Approach

### R1-Zero: Pure RLVR
- No supervised fine-tuning
- Only RL on math/code problems
- **Key finding**: Reasoning emerges from pure RL

### Production R1
1. Cold-start SFT with small high-quality dataset
2. RLVR training
3. Results in strong reasoning + good general behavior

### GRPO Algorithm
- Group Relative Policy Optimization
- More efficient than PPO
- Better suited for language models

---

## Constitutional AI (Anthropic's Approach)

A third path:

1. Model generates responses
2. Model critiques based on principles (constitution)
3. Model revises
4. Train on revisions

**Benefit**: Reduces need for human labels on harmful content.

---

## Comparison

| Aspect | RLHF | RLVR | Constitutional AI |
|--------|------|------|-------------------|
| Human labeling | High | None | Low |
| Domains | All | Verifiable only | All |
| Scaling | Limited by humans | Unlimited | Moderate |
| Objectivity | Subjective | Objective | Principled |

---

## 2025-2026 Trend

The field is moving toward **hybrid approaches**:
- RLVR for reasoning capabilities
- Light RLHF or Constitutional AI for behavior
- Less reliance on expensive human feedback

---

*Last updated: March 2026*
