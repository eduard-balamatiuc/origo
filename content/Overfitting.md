---
tags:
  - concept
status: covered
---

# Overfitting

> [!info] In short
> When a [[Model]] starts memorizing the data instead of actually forming logic behind it.

Like a student who memorized every answer in the textbook but can't solve a new problem that's slightly different.

During [[Training]], a [[Model]] learns from [[Data]] so it can later handle new, unseen situations. Overfitting is when the model performs great on that training data because it's basically "seen the answers before," but fails on new data. The best way to fight this is giving the model a lot of different examples so it can form actual logic. [[Data Splitting]] helps detect overfitting — if training performance is great but validation performance is bad, that's a red flag.

## Related
- [[Underfitting]] - the opposite problem
- [[Training]] - overfitting is a training risk
- [[Data Splitting]] - helps detect it
- [[Data Quality]] - more diverse data helps prevent it
