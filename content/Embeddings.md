---
tags:
  - concept
status: covered
---

# Embeddings

> [!info] In short
> A way of converting words, sentences, or documents into lists of numbers so that a computer can understand meaning and similarity. Similar things end up with similar numbers.

Think of GPS coordinates for concepts. Just as GPS coordinates place cities on a map so you can measure distances between them, embeddings place ideas on a "meaning map" so the computer can measure how close or far apart concepts are. "Paris" and "Lyon" are close on a real map; "king" and "queen" are close on the meaning map.

Computers can't work with words directly — everything has to be converted to numbers first (that's [[Numerical Representation]]). Embeddings take that idea further. Instead of just assigning arbitrary numbers, embeddings capture actual meaning. The word "dog" and the word "puppy" would end up with very similar number lists, while "dog" and "refrigerator" would be very different.

What makes this really powerful is that the model understands context too. The word "bank" gets a different set of numbers in "river bank" versus "bank account."

This is the technology behind semantic search — finding results by meaning, not just keyword matching. You search for "how to fix a broken pipe" and it also finds documents about "plumbing repairs" even if those exact words aren't used. Embeddings are also the foundation of [[RAG]] systems, where documents are stored as embeddings so the AI can quickly find the most relevant ones for your question.

Modern embedding models are even becoming multimodal — they can put text, images, and audio on the same meaning map, so you could search images using a text query.

## Related
- [[Numerical Representation]] - embeddings are a meaningful version of this
- [[RAG]] - embeddings power the retrieval step
- [[Tokens]] - text gets tokenized before being embedded
- [[LLMs]] - use embeddings internally
