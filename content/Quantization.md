---
tags:
  - concept
status: covered
---

# Quantization

> [!info] In short
> Making AI models smaller and faster by rounding their numbers to less precise versions — kind of like using fewer decimal places.

Imagine you have a recipe that calls for 2.3847 cups of flour. In practice, you'd just measure "about 2.4 cups" and the cake would turn out pretty much the same. Quantization does the same thing to the millions (or billions) of numbers inside a model — it rounds them down from very precise values to rougher ones. Each individual number loses a tiny bit of accuracy, but the overall result is almost identical, and now the recipe fits on an index card instead of a full page.

Every AI model is, at its core, a giant pile of numbers — the [[Model Parameters]]. These are typically stored as 32-bit or 16-bit floating-point numbers, which means each one takes up 2 or 4 bytes of memory. When your model has 70 billion parameters, that adds up fast — we're talking 140+ GB just to load the thing. That's way more than what fits on a normal laptop or even most single [[GPU|GPUs]].

Quantization shrinks these numbers down to 8-bit, 4-bit, or sometimes even lower precision. A 70-billion parameter model that normally needs 140 GB can be squeezed down to around 35-40 GB at 4-bit precision. That's the difference between needing a multi-GPU server room and running the model on a MacBook. The quality drop is surprisingly small — research consistently shows that well-done 4-bit quantization loses less than 1% accuracy on most tasks.

This is a big deal for the [[SLMs]] trend and for [[Open vs Closed Models|open models]] in general. When Meta releases Llama or Mistral drops a new model, the community immediately creates quantized versions in formats like GGUF that you can download and run locally through tools like Ollama or LM Studio. That's how people are running capable language models on their laptops and even phones — the model itself didn't get simpler, it just got packed more efficiently. Quantization directly improves [[Inference]] speed and [[Latency]] too, because the hardware has to move and crunch fewer bits for every single token.

## Related
- [[Model Parameters]] - the numbers that get quantized
- [[SLMs]] - quantization is a key enabler of running models on small hardware
- [[GPU]] - quantization reduces the GPU memory needed
- [[Inference]] - quantized models run inference faster
- [[Latency]] - less computation per token means lower latency
- [[Open vs Closed Models]] - quantization matters most for open models you run yourself
