---
tags:
  - concept
status: covered
---

# Hallucination

> [!info] In short
> When an [[LLMs|LLM]] generates a response that sounds confident and plausible but is factually wrong or completely made up.

Think of a very enthusiastic new employee on their first day. When a client asks them a detailed question they don't know the answer to, instead of saying "let me check," they confidently improvise an answer that sounds reasonable but may be completely wrong. They're not lying — they genuinely think they're being helpful. That's hallucination.

This happens because of how [[LLMs]] work under the hood — they predict the next [[Tokens|token]] (word fragment) based on statistical patterns. They don't actually "know" facts the way we do. When the model hits a question where it doesn't have enough information, it doesn't say "I don't know." Instead, it generates the most plausible-sounding answer based on patterns it's seen. This can result in fabricated citations, invented statistics, or confidently wrong claims.

This isn't a bug that will be fully "fixed" — a 2024 academic paper proved mathematically that hallucination is inevitable when LLMs are used as general problem solvers. Rates have decreased with newer models, but they haven't reached zero.

The main ways to fight hallucination are: [[RAG]] (grounding answers in real documents), [[Chain of Thought|chain-of-thought prompting]] (asking the model to show its reasoning), and human review for anything high-stakes. A practical rule of thumb: never deploy LLM outputs in high-stakes contexts — legal, medical, financial — without human review. Treat AI-generated content as a first draft, not a final answer.

## Related
- [[RAG]] - helps reduce hallucination by grounding in real data
- [[Guardrails]] - can catch hallucinated content
- [[Next Token Prediction]] - the root cause
- [[Evaluation]] - measuring hallucination rates
