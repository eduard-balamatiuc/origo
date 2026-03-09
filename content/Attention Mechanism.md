---
tags:
  - concept
status: covered
---

# Attention Mechanism

> [!info] In short
> The core innovation inside the [[Transformer]] architecture. It lets the model decide which parts of the input are relevant to each other when making a prediction.

When you read a sentence like "The cat sat on the mat because it was tired," your brain automatically connects "it" back to "the cat" and not "the mat." You're paying attention to the right words. That's essentially what the attention mechanism does — it figures out which words (or [[Tokens]]) in the input should be paying attention to which other words.

Before attention came along, language models processed text in order — word by word, left to right — and had a hard time remembering what happened earlier in long sequences. The attention mechanism changed that by letting the model look at the entire input at once and weigh how important each part is relative to every other part.

This is what made the [[Transformer]] so powerful for [[Natural Language Processing|NLP]]. Instead of hoping the model remembers something from 200 words ago, attention explicitly creates connections between all positions in the text. It's the reason [[LLMs]] can handle long conversations and maintain context across thousands of [[Tokens]].

## Related
- [[Transformer]] - attention is the core piece of this architecture
- [[LLMs]] - powered by attention
- [[Tokens]] - what the attention mechanism operates over
- [[Context Window]] - attention across the whole window is what makes it work
