---
tags:
  - concept
status: covered
---

# Large Language Models (LLMs)

> [!info] In short
> Models built on the [[Transformer]] architecture, trained on massive text data. They predict the next [[Tokens|token]] given everything that came before.

Imagine someone who has read every book, article, and website ever written. You start a sentence and they complete it — one word at a time — based on everything they've read. That's essentially what an LLM does.

In AI, a [[Model]] is a program that has learned patterns from [[Data]]. Language Models specifically have the [[Transformer]] architecture at their base, which showed really good results for text processing.

But what are they actually predicting? Words — or better said, [[Tokens]] (we'll get to that). The task is: given all the text you've been provided, what is the next probable word? And they do this for every single word, one by one. That's [[Next Token Prediction]].

An interesting thing about these models is that they keep getting better as you give them more data and make their architectures bigger ([[Scaling Laws]]). Previous models usually hit a sweet spot, but LLMs just kept improving. That's how they evolved from a few millions of [[Model Parameters|parameters]] to hundreds of billions.

There's also the word "Large" in the name, but it's become relative. What was considered large before is now small compared to today's top models. That's where [[SLMs|Small Language Models]] come from — models that can run on your laptop or phone. The naming is fuzzy and keeps shifting as hardware gets better.

## Related
- [[Transformer]] - the architecture behind LLMs
- [[Tokens]] - what LLMs actually predict
- [[Next Token Prediction]] - the core task
- [[Scaling Laws]] - why bigger = better for LLMs
- [[SLMs]] - the smaller counterpart
- [[ChatGPT Gemini Claude]] - the most well-known examples
- [[Model Parameters]] - LLMs have billions of them
