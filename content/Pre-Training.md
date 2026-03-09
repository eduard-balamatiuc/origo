---
tags:
  - concept
status: covered
---

# Pre-Training

> [!info] In short
> The massive, expensive, months-long process of teaching an [[LLMs|LLM]] to understand language by having it read the internet — books, code, papers, everything.

Imagine hiring someone who has never seen any written text and asking them to read trillions of words and learn how language works purely by predicting the next word in a sentence over and over, billions of times. That's pre-training.

The model doesn't memorize documents — it learns patterns about how words and ideas relate to each other through [[Next Token Prediction]]. After pre-training, the model can write coherently, answer questions, summarize text, and reason — but it has no specific personality, no safety guardrails, and no domain expertise yet. It's a generalist.

You will almost certainly never do this yourself. Pre-training a frontier model costs tens to hundreds of millions of dollars and requires thousands of [[GPU|GPUs]] running for months. This is what companies like OpenAI, Google, Meta, and Anthropic do. The quality of pre-training data sets the upper bound of what the model can know — if it wasn't in the training data, the model can't reason about it well.

This is also why models have a "knowledge cutoff." When someone says "this model's knowledge cuts off at April 2025," they mean that's when the pre-training data stopped being collected.

## Related
- [[Training]] - pre-training is the first phase
- [[Fine-Tuning]] - the specialization step that comes after
- [[Data]] - pre-training needs enormous amounts of it
- [[LLMs]] - this is how they're built
- [[Scaling Laws]] - more data and compute in pre-training = better model
