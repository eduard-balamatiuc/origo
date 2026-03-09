---
tags:
  - concept
status: covered
---

# GPU (Graphics Processing Unit)

> [!info] In short
> A specialized computer chip that can perform thousands of calculations simultaneously, making it essential for [[Training|training]] and running AI models.

A regular processor (CPU) is like a single brilliant mathematician who can solve any equation, but only one at a time. A GPU is like a stadium full of 10,000 average calculators, each solving a simple equation simultaneously. AI workloads are like grading 10,000 multiple-choice exams — you don't need a genius, you need a lot of people working at once.

AI models need to perform billions of mathematical operations — multiplying huge tables of numbers together. A GPU can do thousands of these multiplications in parallel. That's why training a model that might take months on a regular processor can take days or hours on GPUs.

The dominant GPU maker for AI is NVIDIA. GPU costs are a major driver of AI expenses — renting a single high-end GPU in the cloud runs roughly $2–4 per hour. Training a frontier model can cost tens of millions of dollars in GPU time. This is also why running your own [[Open vs Closed Models|open models]] requires serious investment.

GPUs are used for both phases: [[Training]] (teaching the model, extremely compute-heavy) and [[Inference]] (running the trained model, less intensive but still benefits from GPUs). The cost and availability of GPUs is one of the main reasons why AI development is concentrated among a handful of large companies.

## Related
- [[Training]] - GPUs make training feasible
- [[Inference]] - GPUs speed up inference
- [[Open vs Closed Models]] - self-hosting needs GPUs
- [[Cost and Pricing]] - GPUs drive a lot of AI costs
