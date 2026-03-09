---
tags:
  - concept
status: covered
---

# Model Parameters / Weights

> [!info] In short
> The internal settings a [[Model]] tunes during [[Training]] to get better at its task. When someone says a model has "70 billion parameters," think of 70 billion tiny knobs that were adjusted until the model learned to do its job well.

If the model architecture is the blueprint of a building, the parameters are the material choices — wood vs metal vs cement. They define how the building actually behaves.

In [[Machine Learning]], a [[Model]] is a system that learns patterns from [[Data]]. The way it "learns" is by adjusting its parameters — these internal values are what actually change during [[Training]]. We start with random parameters — we don't really care about them at the start since we'll have to learn them anyway. Through the training process, [[Gradient Descent]] updates these parameters to improve predictions. Language models have evolved from a few millions of parameters to hundreds of billions, and these are all values that were learned during training.

## Related
- [[Model]] - what they belong to
- [[Training]] - the process that adjusts them
- [[Gradient Descent]] - the algorithm that updates them
