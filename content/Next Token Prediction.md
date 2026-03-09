---
tags:
  - concept
status: covered
---

# Next Token Prediction

> [!info] In short
> The core task [[LLMs]] solve: given all the previous text, what is the next probable word (or [[Tokens|token]])?

At the heart of every [[LLMs|Large Language Model]] — the technology behind ChatGPT, Claude, and similar tools — is a surprisingly simple idea.

The models are solving this task: given the text "here usually goes all the text or discussion or information you provide to the LLM," what is the next probable word? And they do this for every single word, one by one. That's it. The entire magic of chatbots, code generators, and AI assistants boils down to predicting the next token, over and over.

## Related
- [[LLMs]] - this is what they do
- [[Tokens]] - the units being predicted
- [[Transformer]] - the architecture that makes it work well
