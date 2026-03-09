---
tags:
  - concept
status: covered
---

# Semantic Search

> [!info] In short
> A way of searching that finds results based on what you *mean*, not just the exact words you typed.

Think about asking a librarian for help. A keyword search is like a librarian who can only look at book titles and find exact word matches — you ask for "fixing a broken pipe" and they only bring you books with those exact words in the title. A semantic search is like a librarian who actually understands your question — they'd also bring you books on "plumbing repair guides" and "home water system maintenance" because they get what you're really asking about, even though none of those words match.

Traditional search is basically pattern matching. You type in "budget laptop for students" and the system looks for documents that contain those exact words. If a great article is titled "affordable notebooks for college" — tough luck, the keywords don't overlap, so you never see it. This has been the fundamental limitation of search for decades, and if you've ever spent 20 minutes rewording a Google query trying to find something you know exists, you've felt the pain firsthand.

Semantic search fixes this by working with meaning instead of keywords. Here's how it works under the hood: both your query and all the documents in the system get converted into [[Embeddings]] — those lists of numbers that capture meaning. Your query becomes a point on a "meaning map," and the system finds documents whose points are closest to yours. "Broken pipe" and "plumbing repair" end up near each other on that map because they're about the same thing, even though they share zero words. The math behind finding those nearest neighbors is mostly cosine similarity — basically measuring the angle between two vectors — but you don't need to worry about that. The important thing is: similar meaning equals nearby points, and nearby points get returned as results.

This is what makes [[RAG]] actually work in practice. When your AI assistant needs to look up relevant company documents before answering a question, it's using semantic search to find the right ones. Without it, RAG would just be keyword matching against a database, and you'd miss half the relevant information. It's also what powers the smarts behind Google Search (they switched to a model called BERT for understanding queries back in 2019), product recommendations on e-commerce sites, and enterprise tools that help employees find information buried in thousands of internal documents. Pretty much anywhere you need to find things by meaning rather than by exact phrasing, semantic search is doing the heavy lifting.

## Related
- [[Embeddings]] - the technology that powers semantic search by converting text into meaning-capturing vectors
- [[RAG]] - semantic search is the retrieval mechanism that makes RAG work
- [[Natural Language Processing]] - semantic search is one of NLP's most practical applications
- [[AI Engineering]] - building semantic search pipelines is a core AI engineering task
