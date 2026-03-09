---
tags:
  - concept
status: covered
---

# Bias in AI

> [!info] In short
> When an AI system produces unfair or skewed results because the [[Data]] it learned from reflects real-world prejudices and inequalities.

[[AI]] systems learn to make decisions by studying huge amounts of [[Data]] — past hiring records, loan histories, medical files, internet text. The problem is, that data carries the biases of the world it came from.

Imagine you grow up in a household where everyone says "cats are better than dogs." You've never really thought about it — it's just what you've always heard. So when someone asks your opinion, you confidently say cats are better. You're not being malicious, you're just repeating patterns from your environment. That's kind of what AI does with bias — it absorbs whatever its training data contains, including the unfair parts.

The real world isn't fair, and that shows up in the data. Hiring data from the past reflects decades of gender discrimination. Loan approval records carry racial disparities. Medical datasets underrepresent certain populations. When you [[Training|train]] a model on this data, it picks up those patterns and treats them as "how things should be."

There are some well-known examples. Amazon built a hiring tool that learned from ten years of resume data — and since most hires had been men, it started penalizing resumes that mentioned women's colleges or the word "women's." MIT researchers found that commercial facial recognition systems had error rates of up to 35% for darker-skinned women, while working pretty well for lighter-skinned men. Studies on automated lending found that Black and Latino borrowers were charged higher interest rates, even when their financial profiles were comparable to white borrowers.

Here's the tricky part — you can't just "remove" bias from the data. It's not like there's a bias column you can delete. The bias is baked into the patterns themselves, because the data reflects real societal inequalities. If you train on historical hiring data, you're training on a world where certain groups had fewer opportunities. Some teams try to balance datasets, others add fairness constraints during [[Training]], and others focus on [[Evaluation]] to catch biased outputs. But there's no silver bullet — it's an ongoing process that requires constant attention.

It's worth noting that bias is different from what [[Guardrails]] address. Guardrails are about preventing specific harmful outputs — like blocking toxic language or stopping the model from leaking personal information. Bias is more systemic. It's not one bad output you can filter — it's a pattern woven through the model's entire understanding of the world. You need both: guardrails to catch harmful responses, and deliberate bias testing to ensure the system treats people fairly.

## Related
- [[Data]] - bias comes from the data the model learns from
- [[Data Quality]] - biased data is a data quality problem
- [[Training]] - bias gets embedded during the training process
- [[Guardrails]] - different from bias, focused on preventing harmful outputs
- [[Evaluation]] - how you detect and measure bias in a model
