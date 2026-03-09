---
tags:
  - concept
status: covered
---

# Data Splitting

> [!info] In short
> Dividing your [[Data]] into three parts — training, validation, and testing — so the [[Model]] can learn, check its understanding, and prove itself on unseen data.

At school: practice exercises (training), flash tests along the way (validation), and the final exam (testing). You never get the same question twice — that would be cheating.

When you have a dataset, you split it into 3 parts:
- **Training set** — the largest portion, where the model actually learns
- **Validation set** — used during training to check progress without bias
- **Test set** — the final check, data the model has never seen

These don't have to be equal, but the distribution of examples should be balanced. You know when at school you were taught something in class and then given something completely different at the test? That's what we want to avoid. All the use cases the model should handle need to be present in all 3 sets.

## Related
- [[Data]] - what gets split
- [[Training]] - uses all three sets
- [[Overfitting]] - splitting helps detect it
