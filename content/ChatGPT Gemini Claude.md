---
tags:
  - concept
status: covered
---

# ChatGPT / Gemini / Claude

> [!info] In short
> The three most well-known [[LLMs|LLM]] products — made by OpenAI, Google, and Anthropic respectively. What most people picture when they hear "AI" today.

Think of them like different car brands. A Toyota, a BMW, and a Volvo all get you from A to B, but each company has a different philosophy — one focuses on reliability and mass market, another on performance and features, another on safety. Same with these AI products. They all answer questions, write text, and help you think — but each company has a different bet on what matters most.

The whole current wave started on November 30, 2022, when OpenAI released ChatGPT. It used the GPT-3.5 model and was free to try. Within two months it had 100 million users — the fastest-growing consumer app in history at the time. That single launch basically kicked off the AI boom we're still in. Google scrambled to release Bard (later renamed to Gemini) in February 2023, and Anthropic launched Claude in March 2023. Since then, it's been a constant race of new model releases and feature updates.

One thing that trips people up: there's a difference between the **product** and the **model**. ChatGPT is the product — the website and app you chat with. GPT-4, GPT-4o, GPT-5.2 — those are the models running under the hood. Same with Claude (the product) versus Claude Opus, Claude Sonnet (the models). And Gemini (the product) versus Gemini 2.5 Pro, Gemini 3 (the models). The product is the thing you interact with. The model is the engine inside. Products add features like memory, file uploads, web browsing, and image generation on top of the raw model capabilities.

Each company has a noticeably different approach. **OpenAI** has been the most aggressive — they move fast, ship constantly, and have bet big on scaling models up and getting them into as many hands as possible. They went consumer-first with ChatGPT and built a massive user base. **Google** plays the integration game — Gemini is getting woven into Search, Gmail, Docs, YouTube, Android, basically everywhere Google already is. Their models also tend to lead on [[Multimodal]] capabilities (handling text, images, video, audio together) and they hold the record on [[Context Window]] size. **Anthropic** takes a more safety-focused path. They were founded by ex-OpenAI researchers specifically because they thought AI safety wasn't getting enough attention. Their Claude models are known for being careful, honest, and particularly strong at coding and long-document analysis. Enterprises in regulated industries (finance, security) tend to gravitate toward Claude.

On pricing, all three offer free tiers with usage limits and paid plans around \$20/month that unlock more usage and access to their strongest models. OpenAI and Anthropic both have premium tiers at \$200/month for power users. Google bundles its AI into Google One AI Premium at \$19.99/month, with an Ultra tier at \$249.99/month. For developers building applications through [[API|APIs]], pricing is per-token and varies by model — this matters a lot for [[AI Engineering]] since costs can add up fast at scale.

There are other notable players you should know about. **Meta** releases their Llama models as [[Open vs Closed Models|open-source]], meaning anyone can download and run them — Llama has become the backbone of the open-source AI ecosystem. **Mistral**, a French startup, punches above its weight with efficient, high-quality models. **DeepSeek**, a Chinese lab, shocked the industry in early 2025 by releasing reasoning models that matched top proprietary ones at a fraction of the training cost. **Alibaba's Qwen** models lead in math and coding benchmarks. And **xAI** (Elon Musk's company) has Grok, which is integrated into X (formerly Twitter) and goes for a more personality-driven, unfiltered approach. The landscape keeps shifting, but these are the names you'll keep hearing.

## Related
- [[LLMs]] - the technology powering all of these products
- [[AI]] - what people associate with AI today
- [[Next Token Prediction]] - what they're all doing under the hood
- [[AI Engineering]] - the field of building applications with these models
- [[Open vs Closed Models]] - the open-source alternatives
- [[Multimodal]] - a key differentiator between models
- [[Context Window]] - varies significantly between providers
- [[API]] - how developers access these models programmatically
- [[Cost and Pricing]] - varies across providers and tiers
