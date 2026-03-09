---
tags:
  - concept
status: covered
---

# Inference

> [!info] In short
> The moment the [[Model]] actually does its job — you send it a question and it gives you an answer. No learning happens here, the model just applies what it already knows.

AI models go through two phases in their life. First, [[Training]] — where they study massive amounts of data and learn patterns. Then inference — where they actually put that learning to use. If training is studying for an exam, inference is taking the exam. The model reads your input, processes it through everything it has learned, and generates a response. That's it — no more studying, just performing.

Every time you type something into ChatGPT or Claude, the model is doing inference — it's reading your input and producing output one [[Tokens|token]] at a time based on everything it learned during [[Training]]. No new learning happens during this process.

Here's the thing though — this is where most of the ongoing cost lives. Training is a one-time expense, but inference is the bill that keeps coming. Every API call, every user message, every response is inference. Industry estimates put inference at around 80-90% of the total cost of running an AI system over its lifetime. The good news is that inference costs have been dropping fast — something like 1,000x in three years. GPT-4-level performance that cost $20 per million tokens in late 2022 was around $0.40 by 2025.

When people complain that "the AI is slow," they're complaining about inference [[Latency]].

## Related
- [[Training]] - inference is the opposite phase (using vs learning)
- [[Tokens]] - inference generates tokens one at a time
- [[Cost and Pricing]] - inference is where the ongoing costs are
- [[Latency]] - how fast inference happens
- [[Temperature]] - controls randomness during inference
