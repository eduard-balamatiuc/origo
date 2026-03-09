---
tags:
  - concept
status: covered
---

# Underfitting

> [!info] In short
> When a [[Model]] is not adapting to the data and isn't creating any logical connections.

Like a student who sat through all the lectures but didn't grasp any of the concepts — not even close to memorizing, just lost.

When a [[Model]] is being [[Training|trained]], it goes through [[Data]] over and over, trying to find patterns it can use to make predictions. Underfitting is what happens when the model isn't learning enough from that [[Training]] data. It's nowhere near memorizing it either — it just isn't picking up on the patterns. This usually means the model needs more training time, more data, or a better [[Model Architecture]] that can capture the complexity of the problem. We want the model to sit in the sweet spot between underfitting and [[Overfitting]].

## Related
- [[Overfitting]] - the opposite problem
- [[Training]] - underfitting is a training risk
- [[Model Architecture]] - might need a more capable one
