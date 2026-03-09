---
tags:
  - concept
status: covered
---

# Transformer Architecture

> [!info] In short
> The [[Model Architecture]] behind [[LLMs]] — introduced in 2017, it changed everything because it processes text all at once instead of word by word.

Imagine you're trying to understand a long email. The old way (RNNs) was like reading it through a tiny slit in a piece of paper — one word at a time, left to right, trying to remember what you read earlier. By the time you reach the end, you've half-forgotten the beginning. The Transformer way is like laying the entire email out on a big table and being able to look at all of it at once — drawing lines between words that relate to each other, no matter how far apart they are.

Before transformers, the best models for language were called RNNs and LSTMs. They processed text sequentially — word 1, then word 2, then word 3 — kind of like reading one word at a time and passing a note forward about what you've seen so far. This had two big problems: it was painfully slow (you couldn't speed it up by throwing more hardware at it, because each step depended on the previous one), and the model would start "forgetting" stuff from earlier in the text. LSTMs were an improvement that tried to fix the forgetting problem, but the sequential bottleneck remained.

In 2017, a team of researchers at Google published a paper called "Attention Is All You Need" — which is one of the most influential papers in all of AI. Their insight was: what if we throw away the sequential processing entirely and just let every word look at every other word at the same time? That's the [[Attention Mechanism]] — or more precisely, "self-attention." When processing the word "it" in a sentence like "The cat sat on the mat because it was tired," self-attention lets the model figure out that "it" refers to "the cat" and not "the mat." It does this for every word in the input, all in parallel. That parallel processing is why transformers could take full advantage of [[GPU|GPUs]], which are designed to do lots of computations at the same time. Training times went from weeks to days.

The original transformer had two main parts: an encoder (which reads and understands the input) and a decoder (which generates the output). This encoder-decoder design was built for translation — you encode a French sentence, then decode it into English. But then people discovered something interesting: you could use just the decoder part on its own and get amazing results for text generation. That's what GPT (Generative Pre-Trained Transformer) does — it's "decoder-only." It just predicts [[Next Token Prediction|the next token]], over and over, using self-attention to keep track of everything that came before. Most of the [[LLMs]] you hear about today — GPT-4, Claude, Llama — are decoder-only transformers.

What made transformers truly revolutionary wasn't just one thing — it was the combination. Parallel processing meant you could train on way more [[Data]]. Self-attention meant you could capture relationships across long stretches of text. And the architecture turned out to be weirdly general — people started applying it to images, audio, protein structures, you name it. It went from a machine translation trick to the foundation of pretty much all modern AI.

## Related
- [[Model Architecture]] - transformer is a type of architecture
- [[LLMs]] - built on transformers
- [[Attention Mechanism]] - the key innovation inside transformers
- [[GPU]] - parallel processing is why transformers need GPUs
- [[Next Token Prediction]] - what decoder-only transformers do
- [[Pre-Training]] - transformers enabled training on massive datasets
- [[Scaling Laws]] - transformers scale better than previous architectures
