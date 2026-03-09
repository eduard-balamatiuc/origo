---
tags:
  - concept
status: covered
---

# Transfer Learning

> [!info] In short
> The idea that a model trained on one task can reuse what it learned for a different task — so you don't have to start from scratch every time.

Say you learned to drive a car. When you get behind the wheel of a truck, you don't need to re-learn what a steering wheel does, how mirrors work, or what traffic signs mean. You already have a foundation — you just need to adjust to the bigger vehicle. That's transfer learning: taking knowledge from one context and applying it to another.

This is the concept that makes the whole [[Pre-Training]] + [[Fine-Tuning]] pipeline actually work. When a model goes through [[Pre-Training]], it reads enormous amounts of text and learns patterns about language — grammar, facts, reasoning structures, stuff like that. All of that gets encoded in the model's [[Model Parameters|parameters]]. Transfer learning is the reason those parameters are still useful when you later want the model to do something specific, like classify legal documents or answer medical questions.

Without transfer learning, you'd need to train a brand new model from zero for every single task. That would be absurdly expensive and slow. Imagine needing millions of medical examples and months of [[Training]] just to build a medical chatbot — when instead, you can take an [[LLMs|LLM]] that already understands language pretty well and fine-tune it on a few thousand medical texts. The model transfers what it already knows about language and just adapts to the medical domain. That's why this approach has become the standard.

This is also why modern AI feels so practical compared to what we had five or ten years ago. Back then, every new use case basically meant training from scratch. Now, companies release pre-trained models, and anyone can take them and specialize them for their own needs with relatively little data and compute. Transfer learning is the reason that's possible — it dramatically cuts both the cost and the amount of domain-specific data you need to get good results.

## Related
- [[Pre-Training]] - the phase where the model builds its transferable knowledge
- [[Fine-Tuning]] - where that knowledge gets adapted for a specific task
- [[Training]] - the broader process that transfer learning makes more efficient
- [[Model Parameters]] - what actually carries the learned knowledge between tasks
- [[LLMs]] - the models that benefit from transfer learning the most today
