---
tags:
  - concept
status: covered
---

# Batch Processing

> [!info] In short
> Sending a bunch of non-urgent [[API]] requests at once and getting them back later at a discount — typically 50% off.

When companies integrate [[LLMs]] into their products, they often need to process thousands or millions of requests. Not all of those need an instant answer — and that's where batch processing saves serious money.

Like sending a package via standard shipping instead of express. You don't need it tomorrow morning, so you pay less and it arrives in a day or two. Same package, same destination, just not rushed.

When you call an LLM through an [[API]], you normally get a response in seconds. But not every task needs an instant answer. If you're processing thousands of customer reviews, generating product descriptions, or running evaluations on a dataset, you probably don't care if results come back in 24 hours instead of 2 seconds.

That's where batch processing comes in. Providers like OpenAI and Anthropic let you bundle up requests and submit them as a batch. The provider processes them when they have spare capacity (off-peak hours, underutilized servers), and you get the results back within a set window — usually 24 hours. In return, you pay around 50% less per [[Tokens|token]].

For companies running AI at scale, this adds up fast. If you're making millions of API calls a month and half of them aren't time-sensitive, batch processing can cut that portion of your bill in half. Combined with other optimization techniques like prompt caching, the savings compound. It's one of those straightforward wins that doesn't require any changes to the quality of your output — just a bit of patience.

## Related
- [[Cost and Pricing]] - batch processing is a key cost optimization
- [[API]] - batch endpoints are a feature of LLM APIs
- [[Inference]] - each batch request is still an inference call
- [[Latency]] - you trade latency for cost savings
