---
tags:
  - concept
status: covered
---

# Gradient Descent

> [!info] In short
> The optimization algorithm that actually updates the [[Model Parameters]] to make better predictions.

Imagine you're blindfolded on a hilly terrain and you need to find the lowest valley. You feel the slope under your feet and take a step downhill. Repeat until you can't go any lower.

When a [[Model]] is [[Training|training]], it makes predictions, and the [[Cost Function]] tells it how wrong those predictions were. But knowing you're wrong isn't enough — you need a way to get better. That's where Gradient Descent comes in. We know how bad the model did (thanks to the cost function), but how do we actually make it better? Gradient Descent takes into consideration all the operations the model performed to reach its prediction, uses the cost function to understand how well it did, and then updates the [[Model Parameters]] to improve the prediction. We do a full pass through the training data, update the parameters, and repeat.

## Related
- [[Cost Function]] - tells gradient descent which direction to go
- [[Model Parameters]] - what gets updated
- [[Training]] - gradient descent is the engine of training
