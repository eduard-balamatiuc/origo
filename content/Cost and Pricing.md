---
tags:
  - concept
status: covered
---

# Cost & Pricing

> [!info] In short
> LLM services charge per [[Tokens|token]] (roughly 3/4 of a word), with separate rates for what you send in and what the model generates back.

Like a lawyer who charges differently for reading your documents versus writing a legal brief. Reading (input) is cheaper; writing (output) is more expensive. Except instead of billing by the hour, they bill by the word — and AI calls them "tokens."

When you use an LLM through an [[API]], the text is broken into [[Tokens]]. A token is roughly 3/4 of a word, so a 750-word document is about 1,000 tokens. You're billed separately for input tokens (your prompt) and output tokens (the model's response). Output tokens usually cost 3–5x more because generating new text requires more computation than reading it.

To give you a sense of the range as of early 2026: a top-tier model like Claude Opus 4 costs around $15 per million input tokens and $75 per million output tokens. A budget model like DeepSeek V3 costs fractions of a cent by comparison. A typical business query (500 words in, 500 words out) costs fractions of a cent with most models — the costs add up at scale though.

There are ways to optimize: prompt caching (reusing repeated content saves up to 90%), batch processing (non-urgent jobs get discounts), and simply choosing smaller models for simpler tasks. The skill in [[AI Engineering]] is knowing which model to use for which task — you don't need the most expensive model for everything.

## Related
- [[Tokens]] - pricing is based on tokens
- [[API]] - how you access paid models
- [[Inference]] - every API call = inference = cost
- [[Open vs Closed Models]] - very different cost structures
- [[LLMs]] - different models, different prices
