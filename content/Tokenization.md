---
tags:
  - concept
status: covered
---

# Tokenization

> [!info] In short
> The process of breaking text into [[Tokens]] — the small pieces that an [[LLMs|LLM]] actually works with.

Imagine you need to ship a large piece of furniture. You can't fit it through the door as-is, so you disassemble it into smaller standardized pieces, ship them, and they get reassembled on the other side. Tokenization is that disassembly step — breaking text into manageable, standardized chunks.

We said that [[LLMs]] predict the next token, but what even is a token? It's not exactly a word. Tokenization splits text into sub-word pieces based on patterns the tokenizer learned from a huge amount of text. Common words like "the" might be a single token, while uncommon words get broken into smaller pieces — "unbelievable" might become "un", "believ", "able."

Why not just use whole words? Because there are too many unique words in every language, and many words share common parts. By using sub-word tokens, the model can handle words it's never seen before by recognizing familiar pieces. It also means that different languages, code, and even emojis can all be processed through the same system — everything just becomes a sequence of tokens, which are then turned into numbers (see [[Numerical Representation]]).

This is also why [[Cost and Pricing|pricing]] for LLM APIs is based on tokens, not words — tokens are the actual unit of work the model does.

## Related
- [[Tokens]] - what tokenization produces
- [[LLMs]] - tokenization is the first step in how they process text
- [[Numerical Representation]] - tokens get converted to numbers
- [[Cost and Pricing]] - pricing is per token
