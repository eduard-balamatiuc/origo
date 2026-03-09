---
tags:
  - concept
status: covered
---

# RAG (Retrieval-Augmented Generation)

> [!info] In short
> A technique where the AI looks up relevant information from your documents or databases *before* writing its answer, so it can give responses grounded in real, current data instead of just its training memory.

[[LLMs]] are trained on massive amounts of public data, but they don't know anything about your company's internal documents, and their knowledge has a cutoff date. RAG is the most common way to bridge that gap.

Imagine a consultant answering your question. Without RAG, the consultant answers purely from memory — which may be outdated or incomplete. With RAG, the consultant first walks over to a filing cabinet, pulls out the relevant company policies and latest data, reads through them, and then answers. The answer is grounded in your actual documents rather than general knowledge.

RAG works in three steps:
1. **Retrieve** — when a user asks a question, the system searches a knowledge base (your company documents, policies, databases) using [[Embeddings]] to find the most relevant pieces of information
2. **Augment** — those retrieved documents are attached to the user's question as additional context
3. **Generate** — the [[LLMs|LLM]] then writes its answer using both its general knowledge and the specific retrieved documents

This is the most popular way to make an AI system work with your organization's private data without expensive [[Fine-Tuning|fine-tuning]]. It significantly reduces [[Hallucination|hallucinations]] because the AI is answering based on retrieved facts, not guessing. And it keeps answers current — unlike the model's training data which has a fixed cutoff date, the knowledge base can be updated continuously.

The decision between RAG and [[Fine-Tuning]] is a common one. RAG is usually better when your data changes frequently. Fine-tuning is better when you need deeply specialized behavior that's consistent across all interactions.

## Related
- [[Embeddings]] - power the retrieval step
- [[Hallucination]] - RAG helps reduce it
- [[Context Window]] - retrieved docs must fit in the window
- [[Fine-Tuning]] - an alternative approach
- [[AI Engineering]] - RAG is a core pattern
