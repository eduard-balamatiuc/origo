---
tags:
  - concept
status: covered
---

# Latency

> [!info] In short
> How long it takes for an AI model to respond. A constant trade-off between speed, quality, and cost.

Whenever you use an AI tool and notice a pause before it starts responding, that's latency. It's one of the key practical trade-offs in [[AI Engineering]] — speed versus quality versus [[Cost and Pricing|cost]].

Like ordering at a restaurant. A fast-food counter (small model) gives you your meal in 30 seconds — quick but basic. A fine-dining kitchen (large model) takes 20 minutes but delivers a gourmet dish. Depending on the situation — a quick lunch vs a special dinner — you'll choose differently.

When you send a request to an [[LLMs|LLM]], there's a delay before the first word appears (called Time to First Token, or TTFT), and then each word appears at a certain speed. Larger, smarter models are generally slower. Smaller ones are faster but less capable.

What affects latency: [[Model Parameters|model size]] (bigger = slower), input length (more [[Tokens]] = longer wait), hardware ([[GPU]] quality), and network distance to the server.

In practice, you're always balancing three things: latency vs quality vs [[Cost and Pricing|cost]]. You can have faster responses with a smaller model, but you might sacrifice accuracy. You can have better quality with a bigger model, but it takes longer and costs more.

Streaming is a common trick: the model sends tokens as they're generated rather than waiting for the full response, so users see words appearing in real-time. It doesn't reduce total latency but makes the experience *feel* faster.

## Related
- [[Inference]] - latency is an inference concern
- [[Cost and Pricing]] - the speed/cost/quality trade-off
- [[LLMs]] - different models, different latency
- [[GPU]] - better hardware = lower latency
