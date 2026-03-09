---
tags:
  - concept
status: covered
---

# Structured Outputs

> [!info] In short
> A way to force an [[LLMs|LLM]] to respond in a specific, predictable format (like JSON with exact fields) instead of free-form text — so your software can actually use the response without breaking.

When you're building software that uses an [[LLMs|LLM]], you need the AI's responses to come back in a predictable format your code can work with — not free-form text that changes shape every time.

Imagine you ask ten people to describe a product they bought. You'll get ten wildly different answers — paragraphs, bullet points, one-word responses, poems if someone's feeling creative. Now imagine you hand them a form with specific boxes: "Product name," "Rating (1-5)," "Would you recommend it? Yes/No." Suddenly every response comes back in the same shape, and you can easily put all ten into a spreadsheet. Structured outputs are that form — you're telling the LLM exactly what shape its answer should take.

By default, LLMs produce free-form text. That's great for chatbots, but the moment you want to plug an LLM into a real software pipeline — say, automatically extracting product data from customer reviews, or categorizing incoming support tickets — you need the output to follow a predictable structure. If the model returns "The customer seemed pretty happy, probably a 4 out of 5" instead of `{"sentiment": "positive", "rating": 4}`, your code downstream has no idea what to do with that.

Structured outputs solve this by letting you define a schema — basically a template that says "your response must have these exact fields, with these exact types." The model then constrains its generation to always match that schema. OpenAI introduced this as a formal feature in 2024, and it scores 100% on schema-following benchmarks. Before this, developers relied on "JSON mode," which guaranteed valid JSON but couldn't guarantee the JSON would have the right fields. You'd still get surprises. Structured outputs removed that ambiguity.

This is closely related to [[Tool Use|function calling]]. When an LLM decides to call a tool, it needs to produce a structured request with the right parameters — that's structured output under the hood. In fact, most providers implement structured outputs through the same mechanism they use for function calling schemas. So if you've heard about function calling, structured outputs are kind of the same idea applied more broadly — not just for tool calls, but for any response you want in a specific shape.

Why does this matter? Because it's what turns LLMs from "interesting demo" into "production-ready component." Without reliable structured outputs, every LLM integration needs fragile parsing code, retry logic, and error handling for when the model decides to get creative with its formatting. With structured outputs, you just define what you want and get it back consistently. That's the difference between a prototype and something you can actually ship.

## Related
- [[API]] - structured outputs are configured through API parameters
- [[AI Engineering]] - making LLM outputs reliable is a core engineering concern
- [[Tool Use]] - function calling uses structured outputs to format tool requests
- [[Inference]] - structured outputs constrain what happens during inference
- [[Prompt Engineering]] - before structured outputs, prompt engineering was the main way to get formatted responses
