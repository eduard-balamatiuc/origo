---
tags:
  - concept
status: covered
---

# Evaluation

> [!info] In short
> The practice of systematically assessing whether an [[LLMs|LLM]]'s responses are accurate, relevant, safe, and useful — going beyond [[Benchmarks]] to measure real-world quality.

Benchmarks are like a job candidate's exam scores on their resume. Evaluation is the actual job interview and the probation period. You're testing "does this model work well for *our* specific needs?"

When you're building something with an [[LLMs|LLM]] — a chatbot, a summarizer, an internal tool — you need a way to know whether the [[Model]] is actually doing a good job. That's what evaluation is for. There are three main approaches to evaluating LLM outputs:
1. **Human evaluation** — people review outputs for accuracy, helpfulness, and tone. The gold standard but expensive and slow
2. **Automated metrics** — algorithms compare the model's output to reference answers using scoring formulas
3. **LLM-as-a-Judge** — using a powerful LLM to evaluate outputs from another model. This has become the dominant trend because it's 500–5,000x cheaper than human evaluation while matching human consistency levels

The key things teams track: accuracy and [[Hallucination|hallucination]] rate (is the information correct?), relevance (does it actually answer the question?), coherence (is it well-structured?), and safety (does it avoid harmful content?).

A practical approach is to combine automated evaluation at scale — catching most issues cheaply — with targeted human review on flagged or high-stakes cases. Don't treat evaluation as a one-time thing; it should be continuous.

## Related
- [[Benchmarks]] - one piece of the evaluation puzzle
- [[Hallucination]] - a key thing to evaluate for
- [[Guardrails]] - evaluation feeds into guardrail design
- [[Model]] - evaluation helps you pick the right model
