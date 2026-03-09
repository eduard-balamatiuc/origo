---
tags:
  - concept
status: covered
---

# Knowledge Distillation

> [!info] In short
> A technique where a small model learns to imitate a large, powerful model — getting most of its capability at a fraction of the cost.

Think of a senior expert training a junior colleague. The junior doesn't just get a list of correct answers — they shadow the expert, watch how they reason, see which options they hesitate on, and pick up on the subtle confidence levels behind each decision. After enough of that, the junior can handle most situations pretty well on their own, even though they don't have decades of experience.

Here's the basic setup: you have a big, expensive model — the "teacher" — and a smaller, cheaper model — the "student." The teacher has billions of [[Model Parameters|parameters]] and performs really well, but it's slow and costly to run. So instead of deploying that giant model everywhere, you train the student to mimic the teacher's behavior.

What makes this different from normal [[Training]] is what the student actually learns from. In regular training, the model just sees the correct answer — "this is a cat," end of story. But in distillation, the student gets the teacher's full probability distribution. That means it doesn't just learn that the answer is "cat" — it also learns that the teacher was 90% sure it was a cat, 8% sure it was a dog, and 2% sure it was something else. Those "soft labels," as they're called, carry a surprising amount of information about how the teacher reasons. The student picks up on relationships between concepts that it would never get from hard yes-or-no answers alone.

This is actually how a lot of [[SLMs]] got surprisingly good. Microsoft's Orca, for example, was trained on outputs from GPT-4 — not just the final answers, but the step-by-step reasoning and explanations. The result was a much smaller model that punched well above its weight class. You see this pattern everywhere now: take a massive [[LLMs|LLM]], use it to generate high-quality training data, and distill that knowledge into something you can actually afford to run in production.

And that's really the point — it's a practical tradeoff. Running a giant model for every single request is expensive and slow (see [[Cost and Pricing]] and [[Latency]]). A distilled model won't match the teacher on everything, but for most real-world tasks it gets you 90% of the performance at maybe 10% of the cost. That's a pretty good deal, especially when you're serving millions of requests or running on a phone.

## Related
- [[SLMs]] - distillation is a key reason small models can be surprisingly capable
- [[LLMs]] - typically serve as the teacher model
- [[Training]] - distillation is a specialized form of training
- [[Model Parameters]] - the student has far fewer parameters than the teacher
- [[Fine-Tuning]] - a related technique, but fine-tuning adapts to a domain while distillation compresses capability
- [[Cost and Pricing]] - distilled models are much cheaper to run
- [[Latency]] - smaller models respond faster
