---
tags:
  - concept
status: covered
---

# Cost Function

> [!info] In short
> Tells us how close the [[Model]]'s prediction is to the expected value. The closer, the better.

Like a teacher grading your answer — it tells you how far off you were from the correct one.

During [[Training]], a [[Model]] learns by making predictions and then checking how wrong it was. The cost function is what does that checking — after the model makes a prediction, it measures how well or how badly it did. This score is then used by [[Gradient Descent]] to figure out how to update the [[Model Parameters]] to improve next time. The whole [[Training]] loop revolves around minimizing this cost.

## Related
- [[Training]] - cost function drives the training loop
- [[Gradient Descent]] - uses the cost to update parameters
- [[Model Parameters]] - get adjusted based on cost
