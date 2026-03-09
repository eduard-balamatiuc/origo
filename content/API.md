---
tags:
  - concept
status: covered
---

# API (Application Programming Interface)

> [!info] In short
> A standardized way for software programs to communicate with each other. In the LLM context, it's how your applications send prompts to and receive responses from AI models programmatically — no human clicking buttons.

Think of a restaurant. You don't walk into the kitchen and cook your own food. Instead, you interact with a waiter (the API). You look at the menu (the API documentation, which lists what you can request and how), place your order (send your request in the correct format), and the waiter brings your food back (the response). The kitchen (the LLM) does the actual work, but the waiter handles all communication.

When you use ChatGPT or Claude in a browser, you're interacting through a graphical interface. But if your company wants to build AI into its own product — say, automatically summarizing support tickets — you need a way for your software to talk to the AI model directly. That's what an API provides.

Your application sends a message (the prompt) to the API endpoint, and the API sends back the model's response. All automatically, no human in the loop. Most LLM APIs follow a similar pattern: you send a list of messages ([[System Prompt]] + user message) and receive a generated response. This makes it relatively straightforward to switch between providers.

API keys are used for authentication — they're essentially passwords that identify your application and track usage for billing. This is also where [[Cost and Pricing|token-based pricing]] kicks in — you pay for what you use, both for the text you send in and the text you get back.

## Related
- [[AI Engineering]] - APIs are how you build with LLMs
- [[Inference]] - every API call is an inference request
- [[Cost and Pricing]] - API usage is priced per token
- [[Tool Use]] - tools are typically accessed through APIs
