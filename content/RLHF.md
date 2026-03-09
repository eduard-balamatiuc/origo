---
tags:
  - concept
status: covered
---

# RLHF (Reinforcement Learning from Human Feedback)

> [!info] In short
> The training technique that turns a raw text-predicting [[LLMs|LLM]] into a helpful, safe, conversational assistant — it's what makes ChatGPT feel like ChatGPT.

Imagine you hire a new employee who has read every book in the world but has never actually talked to a customer. They know a lot, but if you put them on the phone, they might ramble, say something inappropriate, or just dump trivia at people. So you have experienced staff sit next to them, listen to their calls, and rate how they did. Over time, the new hire learns what a good response looks like — not from reading more books, but from human judgment about what's actually helpful. That's RLHF.

After [[Pre-Training]], you have a model that's incredibly good at predicting the next word. But that's all it does — predict text. Ask it a question and it might give you an answer, or it might continue the question with more questions, or ramble off in a weird direction. It has no concept of "being helpful" or "being safe." So how do we go from that raw text predictor to something like [[ChatGPT Gemini Claude|ChatGPT]]? That's the magic gap, and RLHF is how it gets filled.

The process happens in stages. First comes **instruction tuning** — a form of [[Supervised Learning]] where humans write examples of good responses to prompts. "Given this question, here's what a helpful answer looks like." This is basically [[Fine-Tuning]] the model on high-quality conversation examples, and it gets the model pretty far. It learns to follow instructions, answer questions, and hold a conversation. But it's still not great at knowing *which* of several possible answers a human would actually prefer.

That's where RLHF kicks in. You take the instruction-tuned model and have it generate multiple responses to the same prompt. Then human raters rank those responses — this one's better than that one, this one's too verbose, that one's offensive. Those rankings are used to train a separate **reward model** — a smaller model that learns to predict what humans would rate highly. Finally, you use reinforcement learning (specifically an algorithm called PPO) to nudge the LLM toward generating responses that the reward model scores highly. The model is essentially learning to maximize a human-approval score while staying close enough to its original capabilities that it doesn't forget how to write coherent text.

This is expensive and kind of finicky — you need a lot of human raters, the reward model can have its own biases, and the reinforcement learning step can be unstable. That's why a simpler alternative called **DPO (Direct Preference Optimization)** has gained traction. Instead of training a separate reward model and then doing RL, DPO takes the human preference data and optimizes the LLM directly in a single step. It's faster, cheaper, and often works just as well. Many newer models use DPO or similar techniques instead of full RLHF, though the overall goal is the same — align the model with what humans actually want.

## Related
- [[Pre-Training]] - produces the raw model that RLHF then aligns
- [[Fine-Tuning]] - instruction tuning is a form of fine-tuning, and RLHF builds on top of it
- [[Training]] - RLHF is the final training phase before deployment
- [[Supervised Learning]] - instruction tuning uses supervised learning; RLHF adds reinforcement learning on top
- [[ChatGPT Gemini Claude]] - the products that exist because of RLHF
- [[Guardrails]] - RLHF is one layer of behavioral guardrails
