---
tags:
  - concept
status: covered
---

# Model

> [!info] In short
> Models are in itself functions. The simplest example: `y = a * x + b`. The value `x` is the input, and `a` and `b` are the [[Model Parameters]] (also called weights).

In [[Machine Learning]], the whole idea is that instead of coding rules by hand, you let a system learn patterns from [[Data]]. The model is that system — the thing that actually does the learning and makes predictions.

Think of the function like a blueprint or architecture of a building, and the weights are the different parameters that can be changed to make it suit your use case better. Maybe you want it more robust to windstorms so you use metal instead of wood, or cheaper so you use cement, or an office space so you add more separate rooms.

At the end of the day all models process numerical information (see [[Numerical Representation]]). But there are different ways you could represent data and different ways you could architect a model to learn from it. Some [[Model Architecture|architectures]] are really good for image and video processing but that doesn't mean they'll also be good for text. It's like having a very muscular body — great for lifting heavy weights, probably struggling at a marathon.

The process of fitting a model to your use case is called [[Training]]. Anything that can be represented in a numerical format can be used to train a model. And everything can be represented in a numerical format.

## Related
- [[Model Parameters]] - the learnable values inside the model
- [[Model Architecture]] - the blueprint/structure
- [[Training]] - how models learn
- [[Numerical Representation]] - why everything is numbers
