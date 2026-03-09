---
tags:
  - concept
status: covered
---

# Open vs Closed Models

> [!info] In short
> Open models (like Meta's Llama, Mistral, DeepSeek) release their weights so anyone can download, modify, and run them. Closed models (like GPT-4, Claude) are only accessible through the provider's [[API]] — you never get the model itself.

When companies build [[AI]] systems — specifically [[LLMs]] (the technology behind tools like [[ChatGPT Gemini Claude|ChatGPT and Claude]]) — they have to decide whether to use a model they control end-to-end or one they access as a service. That choice shapes everything from cost to privacy.

Like renting vs owning a car. A closed model is like using a premium taxi service — excellent quality, no maintenance, but you pay per ride and the company controls everything. An open model is like buying your own car — higher upfront investment and you handle maintenance, but you control where you go, you can customize it, and there are no per-trip fees.

A **closed model** is a service: you send your data to the provider's servers, they run it through their model, and send results back. You never see or control the model's internals. A **open model** is a product you can take home: you download the [[Model Parameters|weights]], run it on your own servers, and have full control — you can [[Fine-Tuning|fine-tune]] it, inspect how it works, and ensure your data never leaves your infrastructure.

The performance gap between them is closing fast. As of early 2026, top open models match or exceed closed models on many [[Benchmarks]]. Open models accessed through third-party APIs often cost 70–90% less than closed providers. But self-hosting requires significant infrastructure investment and ML expertise.

The trade-off usually comes down to: closed models for best out-of-the-box performance and zero infrastructure maintenance, open models for data privacy, no vendor lock-in, and cost control at scale.

## Related
- [[LLMs]] - both types are LLMs
- [[API]] - closed models are API-only
- [[Fine-Tuning]] - open models can be fine-tuned freely
- [[GPU]] - self-hosting open models needs GPUs
- [[Cost and Pricing]] - very different cost structures
