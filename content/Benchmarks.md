---
tags:
  - concept
status: covered
---

# Benchmarks

> [!info] In short
> Standardized tests for AI models — like exams that let you compare how well different models perform on specific skills.

Just like students take standardized exams (SAT, GRE) so universities can compare applicants, AI models are run through benchmark tests so developers and buyers can compare them. And just as you wouldn't judge a student solely by their SAT score, you shouldn't judge a model by a single benchmark.

With so many [[LLMs]] available — from OpenAI, Google, Anthropic, Meta, and others — benchmarks give you a way to compare them on the same playing field. Each benchmark focuses on a specific capability. The model is given questions or tasks, its answers are scored, and the result is expressed as a percentage or score. Some common ones:

- **MMLU** — broad knowledge across 57 subjects (math, law, medicine, history). Like a comprehensive final exam
- **HumanEval** — code generation. Can the model write working code?
- **GSM8K** — grade-school math word problems
- **MT-Bench** — multi-turn conversation quality, scored by another LLM acting as judge

The catch is that models can be specifically optimized for benchmark performance without actually improving at real-world tasks — this is called "benchmark gaming" or "teaching to the test." That's why benchmarks are a starting point for comparison, but you should always supplement them with testing on your actual use case through proper [[Evaluation]].

## Related
- [[Evaluation]] - benchmarks are one piece of evaluation
- [[Model]] - benchmarks compare models
- [[LLMs]] - most benchmarks target LLMs now
