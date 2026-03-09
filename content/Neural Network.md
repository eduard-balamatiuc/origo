---
tags:
  - concept
status: covered
---

# Neural Network

> [!info] In short
> A [[Model Architecture]] inspired loosely by how the brain works — layers of connected "neurons" that pass information forward and learn from feedback. The building block of [[Deep Learning]].

Think of it like a chain of people playing telephone, but instead of whispering one message, each person hears from multiple people, decides what's important, and passes their own summary forward. By the end of the chain, the last person gives a final answer. If the answer is wrong, everyone in the chain adjusts how they filter information next time.

A neural network is a model made up of layers. You have an input layer where the data comes in, one or more hidden layers in the middle where the actual processing happens, and an output layer that gives you the result. Each layer is made of small units (called neurons) that take in numbers, do some math on them, and pass the result to the next layer.

What makes neural networks powerful is that they can learn incredibly complex relationships in data — things you could never write rules for by hand. The catch is they need a lot of [[Data]] and compute power to train. When you stack many of these layers on top of each other (hence "deep"), you get [[Deep Learning]], which is what powers most of the AI you hear about today, including [[LLMs]].

## Related
- [[Deep Learning]] - neural networks with many layers
- [[Model Architecture]] - neural networks are a type of architecture
- [[Training]] - how neural networks learn
- [[Model Parameters]] - each connection between neurons has a weight
