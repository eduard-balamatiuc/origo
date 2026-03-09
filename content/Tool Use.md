---
tags:
  - concept
status: covered
---

# Tool Use / Function Calling

> [!info] In short
> The capability that lets an [[LLMs|LLM]] reach out to external tools — like search engines, calculators, databases, or [[API|APIs]] — instead of trying to answer everything from memory alone.

Imagine a very knowledgeable office worker who has memorized thousands of books but has no phone or internet. Without tool use, if you ask them for today's weather, they can only guess. With tool use, you give them a phone and a list of numbers they can call — weather service, calculator hotline, database lookup. Now they can recognize when they need real information, pick up the phone, call the right service, and give you an accurate response.

When you ask an LLM something that requires real-time data or a specific action, the model recognizes it can't answer from its training data alone. Instead of guessing, it generates a structured request that says: "call this specific tool with these specific parameters." The application then executes that tool call, gets the result, and feeds it back to the LLM, which incorporates the real data into its response.

The important thing to understand is that the LLM itself never executes the tool — it only decides which tool to call and what to send. The actual execution happens in the surrounding application.

This is the foundational technology behind [[Agents]]. Without tool use, agents can't interact with the outside world. All major model providers — OpenAI, Anthropic, Google, Mistral — support function calling natively now.

Common real-world uses: looking up live data, querying databases, sending emails, creating calendar events, running calculations, searching the web, reading and writing files.

## Related
- [[Agents]] - tool use is what makes agents possible
- [[API]] - tools are typically accessed via APIs
- [[LLMs]] - the ones deciding which tools to call
- [[Inference]] - tool use happens during inference
