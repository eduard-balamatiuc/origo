---
tags:
  - concept
status: covered
---

# System Prompt

> [!info] In short
> A hidden set of instructions, written by developers, that tells the [[LLMs|LLM]] how to behave before a user ever types anything.

When you build an application on top of an [[LLMs|LLM]] — a chatbot, a writing assistant, anything — you need a way to set ground rules for how it behaves. That's where system prompts come in.

Like the employee handbook and standing orders you give to a new hire on their first day. The customer never sees those instructions, but they shape every interaction that employee has. The system prompt is the AI's employee handbook.

Before any conversation begins, developers can give the model a system prompt — a block of text the user never sees that defines the model's personality, rules, tone, and boundaries. A customer-service chatbot might have something like: "You are a helpful support agent for Acme Corp. Always be polite. Never discuss competitor products. If asked about refunds, direct the user to the refund policy page."

The system prompt stays constant across all user interactions while each user's messages change. It's probably the single biggest lever for making an AI product behave consistently and reliably.

One thing to keep in mind — system prompts are meant to be confidential. If users can extract them (called "system prompt leakage"), it can expose your business logic, safety rules, or sensitive instructions. So there's a whole side of [[Guardrails]] dedicated to protecting them.

## Related
- [[Prompt Engineering]] - system prompt is a specific type of prompt
- [[Guardrails]] - protecting the system prompt
- [[AI Engineering]] - system prompts are fundamental to building AI apps
