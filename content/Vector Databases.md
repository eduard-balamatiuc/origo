---
tags:
  - concept
status: covered
---

# Vector Databases

> [!info] In short
> A special kind of database designed to store [[Embeddings]] and find things by meaning rather than by exact matches — the infrastructure that makes [[RAG]] actually work.

If you want an AI system to search your documents by meaning — not just keywords — you need somewhere to store those meaning representations. That's what vector databases are built for.

Imagine a librarian who has read every single book in the library. You walk up and say, "I'm looking for something about people surviving alone in nature." A traditional database librarian would search the catalog for those exact words in a title. But a vector database librarian actually understands what you mean — they'd pull out "Hatchet," "Into the Wild," and "Robinson Crusoe," even though none of those titles contain the words you used. They're searching by meaning, not by keywords.

Traditional databases are built around exact lookups. You ask "give me all customers where city equals 'Paris'" and you get precise matches. That works great for structured business data, but it completely falls apart when you're dealing with meaning. If you search for "affordable housing options" you also want results about "budget-friendly apartments" and "low-cost rentals" — same idea, totally different words. Traditional databases can't do that.

That's where vector databases come in. They store [[Embeddings]] — those lists of numbers that represent the meaning of text, images, or other data. When you run a query, the database converts your question into an embedding too, and then finds the stored embeddings that are closest to yours in meaning. The typical operation is something like "find the 5 most similar documents to this query," and the database uses math (distance calculations like cosine similarity) to figure out which stored items are the nearest match. It's not doing keyword matching — it's doing meaning matching.

This is the critical piece of infrastructure behind [[RAG]] systems. When a company wants their AI chatbot to answer questions about internal policies, they first convert all their documents into embeddings and store them in a vector database. Then when someone asks a question, the system searches that database for the most relevant chunks of text, pulls them out, and hands them to the [[LLMs|LLM]] as context. Without a vector database, there's no efficient way to do that retrieval step at scale.

The popular options right now include Pinecone (a fully managed cloud service, very easy to get started with), Weaviate (open source, strong hybrid search that combines meaning-based and keyword-based approaches), Chroma (lightweight and open source, popular for prototyping), and pgvector (a PostgreSQL extension, which is great if your team already uses Postgres and doesn't want to add a whole new system). The choice depends on your scale, budget, and how much operational complexity you want to take on.

## Related
- [[Embeddings]] - what gets stored in a vector database
- [[RAG]] - the main use case that drives adoption
- [[Semantic Search]] - the search technique that vector databases enable
- [[AI Engineering]] - vector databases are a core part of the AI engineering stack
- [[Data Engineering]] - managing vector databases falls under data infrastructure
