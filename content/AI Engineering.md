---
tags:
  - concept
status: covered
---

# AI Engineering

> [!info] In short
> The emerging field focused on building products and applications with [[LLMs]] — more about integration and software craft than training models from scratch.

Think of the difference between someone who designs and manufactures car engines versus someone who takes those engines and builds actual cars people can drive — with steering, brakes, navigation, and a nice interior. AI Engineers are the car builders. They don't create the engine (the LLM), but they turn it into something real people can use. They pick the right engine, wire it into the vehicle, add all the systems around it, and make sure the whole thing drives smoothly.

Before roughly 2023, if you wanted to work in AI, you pretty much had to be a machine learning engineer or a data scientist. That meant heavy math, training your own models, working with massive datasets, and spending weeks getting a model to converge. Then ChatGPT dropped in November 2022, and suddenly a huge range of AI capabilities became available through a simple API call. You didn't need a PhD or a GPU cluster anymore — you needed to know how to build software and how to talk to an LLM effectively.

That shift created a new role. Shawn "swyx" Wang wrote a widely-shared essay in mid-2023 called "The Rise of the AI Engineer," and the term stuck. The core idea is straightforward: tasks that used to take a research team five years can now be done by a software engineer with API docs and a spare afternoon. That's obviously a bit of an exaggeration, but the direction is real. The AI Engineer is basically a software engineer who specializes in building applications on top of LLMs instead of training them.

So what does the typical stack look like? You're working with LLM APIs (OpenAI, Anthropic, Google), writing and refining prompts ([[Prompt Engineering]]), building [[RAG]] pipelines so your app can work with private or current data, setting up [[Agents]] that can take actions autonomously, storing [[Embeddings]] in vector databases for fast retrieval, and often using orchestration frameworks like LangChain or LlamaIndex to glue it all together. LangChain is more of a general-purpose toolkit for chaining LLM steps together, while LlamaIndex is more focused on indexing and retrieving documents. In practice, a lot of teams mix and match or skip the frameworks entirely and build directly on the APIs.

The key skills are a blend: solid software engineering fundamentals (you're still building production systems that need to be reliable, tested, and monitored) plus a practical understanding of how LLMs behave — their strengths, their failure modes, how [[Context Window|context windows]] work, how [[Tokens|tokenization]] affects costs, when to use [[Fine-Tuning]] versus RAG, stuff like that. You don't need to understand backpropagation in detail, but you do need to know enough about the technology to make smart architectural decisions. The day-to-day feels much more like product engineering than research — you're shipping features, iterating on prompts, managing costs, and handling the reality that your core component (the LLM) is non-deterministic, meaning it won't give the exact same answer every time.

## Related
- [[AI]] - AI Engineering is a subfield
- [[LLMs]] - the core technology you're building on
- [[Prompt Engineering]] - a key skill in the toolkit
- [[RAG]] - the most common pattern for working with private data
- [[Agents]] - an emerging approach for autonomous task completion
- [[API]] - how you interact with LLMs programmatically
- [[Fine-Tuning]] - an alternative to RAG for specializing model behavior
- [[Embeddings]] - used in retrieval and search
- [[ChatGPT Gemini Claude]] - the major LLM products you'll work with
