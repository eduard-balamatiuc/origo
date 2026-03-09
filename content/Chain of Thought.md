---
tags:
  - concept
status: covered
---

# Chain of Thought

> [!info] In short
> A technique (and now a built-in capability) that makes [[LLMs]] perform better by getting them to "think step by step" instead of jumping straight to an answer.

[[LLMs]] — the AI models behind tools like ChatGPT and Claude — are surprisingly good at language tasks, but they can stumble on problems that require multi-step reasoning. Chain of thought is a technique that helps them get past that.

Imagine you ask someone "what's 17 times 24?" If they just blurt out a number instantly, they'll probably get it wrong. But if they grab a piece of paper, write out the steps — 17 times 20 is 340, 17 times 4 is 68, add them up, 408 — they'll get it right. Chain of thought is that piece of paper for an LLM. The model doesn't get smarter, it just gets the space to work things out.

Here's something that surprised a lot of researchers: if you just add "let's think step by step" to your prompt, [[LLMs]] suddenly get way better at complex tasks. Math problems, logic puzzles, multi-step reasoning — stuff that models would consistently mess up, they'd start getting right just because you told them to show their work. This is called chain-of-thought prompting, and it's one of the most important [[Prompt Engineering]] techniques out there.

Why does it work? It comes down to [[Next Token Prediction]]. Remember, an LLM generates text one [[Tokens|token]] at a time. Each token it produces becomes part of the context for the next one. So when a model writes out intermediate steps, each step is a kind of computation — the model is literally using its own output as a scratch pad. More tokens generated means more "thinking" happening. When you ask it to jump straight to an answer, it only has one shot to get it right. When you let it reason through it, each step nudges the next prediction in the right direction.

This idea got so powerful that companies started building it directly into models. OpenAI released o1 and later o3 — models specifically trained to reason before answering. Anthropic did something similar with Claude's extended thinking mode. These "reasoning models" don't just follow a prompt instruction to think step by step — they're trained with reinforcement learning to actually develop internal chains of thought, check their own work, and try different approaches before giving you a final answer. The model generates what are sometimes called "reasoning tokens" internally, and then only shows you the polished result.

The trade-off? All that thinking takes more [[Tokens]], which means more [[Latency]] and higher [[Cost and Pricing|cost]]. A reasoning model might use thousands of extra tokens working through a problem before it gives you a single sentence answer. For simple questions like "what's the capital of France," that's total overkill — you're paying for thinking the model doesn't need to do. But for complex coding tasks, multi-step analysis, or tricky logic problems, the extra time and cost are absolutely worth it. That's why some models now offer a "thinking budget" — you can decide how much reasoning you want, balancing quality against speed and price. It's not always about maximum intelligence; sometimes you just need a quick answer.

## Related
- [[Prompt Engineering]] - chain-of-thought prompting is a key technique
- [[Next Token Prediction]] - each reasoning step is a token prediction that feeds the next
- [[Tokens]] - more reasoning = more tokens used
- [[LLMs]] - the models that benefit from this approach
- [[Temperature]] - often set low for reasoning tasks to keep outputs focused
- [[Latency]] - reasoning takes longer because of extra tokens
- [[Cost and Pricing]] - more tokens means higher cost
