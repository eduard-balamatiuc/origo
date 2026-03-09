---
tags:
  - concept
status: covered
---

# Memory

> [!info] In short
> LLMs don't actually remember anything between conversations — "memory" is faked by re-sending the entire conversation history each time and storing key facts externally.

Imagine you're texting a friend who has complete amnesia every time they put down their phone. The only way to keep a coherent conversation going is to copy-paste the entire chat log at the top of every single message you send. That's literally how LLM "memory" works — the application pastes the full conversation back into the prompt each time, and the model reads through it all again from scratch.

Here's the thing that surprises most people: [[LLMs]] are stateless. Every time you send a message, the model has zero recollection of what you said before. It's not like it's "thinking" between your messages — it's not doing anything at all. It only wakes up when a new request arrives, processes the input, generates a response, and goes back to being a blank slate.

So how does ChatGPT or Claude seem to remember what you said three messages ago? The application (not the model itself) stores your conversation and re-sends the whole thing as part of every new request. Your latest message gets tacked onto the end of all previous messages, and the model reads through everything as if it's seeing it for the first time. It then generates a response that feels like a natural continuation. Pretty clever trick, but it's just that — a trick.

This is exactly why the [[Context Window]] matters so much. Since the entire conversation history gets sent every time, longer conversations eat up more and more [[Tokens]]. Eventually you hit the limit, and the oldest messages start getting dropped. The model doesn't "gradually forget" — it just literally can't see those messages anymore because they no longer fit in the window. And there's a direct cost implication too: more conversation history means more input tokens, which means higher [[Cost and Pricing|cost]] and increased [[Latency|latency]] for every single reply.

What about the "memory" features that ChatGPT and Claude advertise? Those work differently from conversation history. The application stores summaries and key facts about you in an external database — stuff like "this user prefers Python over JavaScript" or "they're working on a startup in the healthcare space." When you start a new conversation, those stored facts get quietly injected into the [[System Prompt]] before the model sees anything. So the model isn't actually remembering you — it's being told about you, kind of the same way a colleague might brief a substitute before a meeting. This approach is related to [[RAG]] — both are about pulling in external information and stuffing it into the prompt so the model has context it wouldn't otherwise have.

## Related
- [[Context Window]] - conversation history must fit within it, or older messages get dropped
- [[Tokens]] - every message in the history costs tokens
- [[System Prompt]] - where stored "memories" get injected
- [[LLMs]] - fundamentally stateless, memory is handled by the app layer
- [[Cost and Pricing]] - longer conversations = more tokens = higher cost
- [[Latency]] - more context to process means slower responses
- [[RAG]] - a related pattern for injecting external knowledge into the prompt
