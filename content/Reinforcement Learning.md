---
tags:
  - concept
status: covered
---

# Reinforcement Learning

> [!info] In short
> A type of [[Training]] where the model learns through trial and error — it tries things, gets a score telling it how well it did, and gradually figures out what works.

Think about how you'd train a dog. You don't sit the dog down and explain the rules. Instead, the dog tries something — sits when you say "sit" — and you give it a treat. It jumps on the couch, you say "no." Over time, the dog figures out which actions lead to treats and which ones don't. That's reinforcement learning in a nutshell: no answer key, no labels, just rewards and penalties through experience.

So you've got [[Supervised Learning]] where you have the answers upfront, and [[Unsupervised Learning]] where you're just looking for patterns. Reinforcement learning is the third approach, and it's kind of its own thing. Here, you have an "agent" that interacts with some environment, takes actions, and gets back a reward signal — basically a score that says "good move" or "bad move." The agent's entire goal is to maximize that score over time.

The most famous example is probably AlphaGo, the system DeepMind built that beat the world champion at Go in 2016. Go is absurdly complex — there are more possible board positions than atoms in the universe. You can't just brute-force it. Instead, AlphaGo played millions of games against itself, learning from each win and loss which moves tend to lead to victory. Same idea applies to robotics — a robot arm learning to pick up objects by trying thousands of times, getting a reward when it succeeds and nothing when it drops the thing.

Here's where it gets really relevant to modern [[AI]]: a technique called RLHF (Reinforcement Learning from Human Feedback) is one of the key reasons [[ChatGPT Gemini Claude|ChatGPT, Claude, and Gemini]] feel so much better to talk to than raw language models. After a model goes through [[Pre-Training]] on massive text data, human reviewers rank different responses — "this answer is helpful," "this one is misleading." Those rankings become the reward signal, and the model is further trained to produce responses humans actually prefer. It's pretty much the secret sauce behind making [[LLMs]] not just smart, but actually useful and safe. This also connects directly to the idea of [[Agents]] — when you have a model that can learn from feedback and take actions in an environment, you're getting close to systems that can operate more autonomously.

## Related
- [[Training]] - reinforcement learning is a type of training
- [[Supervised Learning]] - learning with labeled answers (a different paradigm)
- [[Unsupervised Learning]] - learning by finding patterns (another paradigm)
- [[AI]] - reinforcement learning is a key technique in the broader AI field
- [[Agents]] - agents use the perceive-act-evaluate loop that RL is built on
- [[LLMs]] - RLHF is used to align language models with human preferences
- [[Fine-Tuning]] - RLHF is kind of the same idea as fine-tuning but with rewards instead of examples
