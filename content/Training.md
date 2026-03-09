---
tags:
  - concept
status: covered
---

# Training

> [!info] In short
> The process of fitting a [[Model]] to a specific use case by adjusting its [[Model Parameters|parameters]]. An iterative process of prediction, evaluation, and updates.

It's like learning at school. You're taught something, then you have practice exercises, then flash tests to check understanding, and at the end a final exam. You never have repeating exercises — otherwise you'd just memorize answers like a poem, and that's not the goal.

Training depends on the use case. There are two main approaches: [[Supervised Learning]] (you have the task and the solution) and [[Unsupervised Learning]] (you only have the task).

We always need [[Data]] for training, and preferably good data (see [[Data Quality]]). The data gets split into three parts: training, validation, and testing (see [[Data Splitting]]).

The process itself works like this:
1. Start with random [[Model Parameters|parameters]]
2. Feed training inputs to the model, get predictions
3. Use a [[Cost Function]] to measure how bad the prediction was
4. Use [[Gradient Descent]] to update the parameters and improve
5. Validate on separate data to check real understanding
6. Repeat until performance is good enough

When the model starts memorizing instead of learning, that's [[Overfitting]]. When it's not adapting at all, that's [[Underfitting]]. The sweet spot is somewhere in between.

## Related
- [[Data]] - you always need data
- [[Supervised Learning]] - training with known answers
- [[Unsupervised Learning]] - training without known answers
- [[Data Splitting]] - train / validation / test
- [[Cost Function]] - measures prediction quality
- [[Gradient Descent]] - updates the parameters
- [[Overfitting]] - memorizing instead of learning
- [[Underfitting]] - not learning at all
