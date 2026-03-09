---
tags:
  - concept
status: covered
---

# AI Agents

> [!info] In short
> Systems where an [[LLMs|LLM]] doesn't just answer questions — it plans, makes decisions, uses tools, and takes actions to accomplish goals autonomously.

Most AI tools you've used — like ChatGPT or Claude — are conversational: you ask, they answer. Agents take that a step further by letting the AI actually *do things* on its own.

A traditional chatbot is like an encyclopedia — you ask a question, it gives you an answer. An AI agent is more like a junior employee you can delegate tasks to. You say "book me a flight to London next Tuesday under $500" and the employee goes off, searches flight options, compares prices, checks your calendar, and comes back with a booking — making many small decisions along the way without asking you about each one.

A regular chatbot waits for your input, generates one response, and stops. An agent is different — you give it a goal ("research competitors and prepare a summary report") and it breaks that goal into steps, decides which tools it needs (web search, file reader, spreadsheet editor), executes those steps one by one, checks its own work, and adapts if something goes wrong. It operates in a continuous loop of perceive, reason, act, evaluate.

This is one of the fastest-moving areas in AI right now. Multi-agent systems — teams of specialized agents working together — are becoming a major trend. But human oversight remains critical. Hybrid human-agent systems generally produce better outcomes than either alone, especially for decisions with significant business consequences.

The key building block that makes agents possible is [[Tool Use]] — without the ability to call external tools, an agent can't actually interact with the outside world.

## Related
- [[Tool Use]] - what gives agents their superpowers
- [[AI Engineering]] - agents are a core pattern
- [[LLMs]] - the brain behind agents
- [[Prompt Engineering]] - agents need good instructions too
