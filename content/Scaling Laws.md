---
tags:
  - concept
status: covered
---

# Scaling Laws

> [!info] In short
> The observation that language models keep getting better as you give them more [[Data]] and make their architectures bigger — unlike previous models that usually hit a sweet spot.

When you [[Training|train]] a [[Model]], you're feeding it [[Data]] and giving it enough [[Model Parameters|parameters]] to learn from that data. The natural question is: what happens if you just keep adding more data and more parameters? That's exactly what scaling laws describe.

This is what drove the LLM revolution. Previous model types would reach a point of diminishing returns — more data or bigger models wouldn't help much. But [[LLMs]] broke that pattern. They just kept improving with scale. That's how they went from a few million [[Model Parameters|parameters]] to hundreds of billions. This is a key reason companies are pouring so much money into building bigger and bigger models.

## Related
- [[LLMs]] - scaling laws apply primarily to LLMs
- [[Model Parameters]] - more parameters = bigger model
- [[Data]] - more data = better performance
- [[Training]] - scaling requires more training compute
