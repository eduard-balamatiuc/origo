---
tags:
  - concept
status: covered
---

# Temperature

> [!info] In short
> A setting that controls how predictable or creative the [[LLMs|LLM]]'s responses are. Like a dial between "follow the recipe" and "improvise."

Think of a chef deciding what ingredient to add next. At low temperature, the chef always follows the recipe exactly — reliable but predictable. At high temperature, the chef improvises — you might get a brilliant new flavor combination, or something that doesn't taste good at all.

When an LLM generates text, it's predicting the next [[Tokens|token]] by calculating probabilities for every possible word. Temperature adjusts how those probabilities are used. At low temperature (near 0), the model almost always picks the most probable word — consistent, safe, but repetitive. At high temperature (near 1 or above), it's more willing to pick less obvious words — more varied and surprising, but also riskier.

The typical range is 0.0 to 1.0 (some providers go up to 2.0). As a rule of thumb: use low temperature (0.0–0.3) for things that need accuracy — data extraction, code generation, factual questions. Use higher temperature (0.7–1.0) for creative tasks — brainstorming, writing copy, generating ideas.

One interesting thing though: recent research found that higher temperature is only weakly correlated with actual novelty. "More random" doesn't automatically mean "more creative."

## Related
- [[Inference]] - temperature is a setting during inference
- [[Next Token Prediction]] - temperature tweaks this process
- [[LLMs]] - all LLMs have this parameter
