---
tags:
  - concept
status: covered
---

# Context Window

> [!info] In short
> The maximum amount of text an [[LLMs|LLM]] can "see" and work with at one time. Think of it as the model's short-term memory.

Imagine you're reading a report, but you can only keep a certain number of pages on your desk at any time. If someone hands you a new page and your desk is full, you have to remove an older page. The context window is the size of that desk.

Every time you send a message to an LLM, the model doesn't just see your latest message — it sees the entire conversation history plus any attached documents, all at once. The context window is the hard limit on how much total text it can hold. Once the conversation exceeds it, the oldest parts get dropped and the model effectively "forgets" them.

Text is measured in [[Tokens]] (roughly 1 token ≈ 0.75 English words). As of early 2026, Claude offers around 200K tokens (~150,000 words), GPT-4o around 128K tokens, and Google's Gemini up to 1 million tokens.

But bigger doesn't always mean better. Models suffer from something called the "lost-in-the-middle" problem — they pay attention well to information at the beginning and end of the window but lose accuracy for content buried in the middle.

Also worth noting: the context window is shared across everything — the [[System Prompt]], the full conversation history, any attached documents, and the model's own response. So a 200K context window doesn't mean 200K tokens for your documents alone.

## Related
- [[Tokens]] - context window is measured in tokens
- [[LLMs]] - every LLM has a context window limit
- [[RAG]] - helps when you have more info than fits in the window
- [[Cost and Pricing]] - more tokens in = higher cost
