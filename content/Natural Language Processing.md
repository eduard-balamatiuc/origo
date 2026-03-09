---
tags:
  - concept
status: covered
---

# Natural Language Processing (NLP)

> [!info] In short
> The field of AI that deals with human language — getting machines to read, understand, and generate text.

Imagine hiring someone who doesn't speak your language, giving them a dictionary and a grammar book, and hoping they'll eventually understand not just your words but your sarcasm, your idioms, and what you actually mean versus what you literally said. That's essentially the challenge NLP has been trying to solve for decades.

NLP is behind a huge chunk of the AI tools you already use every day. When Gmail catches a phishing email before you see it — that's NLP analyzing the language for suspicious patterns (Google's spam filters block over 100 million spam messages per day this way). When you ask Siri something, the part that figures out what you meant is NLP. Google Translate turning a French article into English? NLP. A company scanning thousands of customer reviews to figure out if people are happy or angry? That's sentiment analysis, one of NLP's classic applications.

The field went through some pretty distinct phases. Early NLP (think 1960s-1990s) was rule-based — people literally hand-coded grammar rules and word lists. This worked for simple stuff but fell apart fast with real human language, which is messy, ambiguous, and full of exceptions. Then [[Machine Learning]] came along and things got better — instead of writing rules, you'd feed the system lots of examples and let it learn patterns. Statistical models like n-grams could predict what word comes next based on what words usually follow each other. Better, but still pretty limited.

The real game-changer was the [[Transformer]] architecture in 2017. It introduced something called the [[Attention Mechanism]], which lets a model look at all the words in a sentence simultaneously and figure out which ones are most relevant to each other. This was a massive leap. BERT (2018) could understand context in both directions — it knew that "bank" means something different in "river bank" versus "bank account." GPT (also 2018) showed that you could generate surprisingly coherent text. And then GPT-3 in 2020 blew the doors open with 175 billion [[Model Parameters|parameters]] and the ability to do tasks it was never explicitly trained for.

[[LLMs]] are, honestly, NLP's biggest achievement. They're the culmination of decades of work in this field. And they've gotten so dominant that when people say "AI" today, they often really mean "an LLM doing NLP." The line between NLP as a research field and LLMs as a product category has gotten pretty blurry. But it's worth remembering that NLP is the broader discipline — [[LLMs]] are one (very impressive) tool within it, and the field still covers everything from [[Tokenization]] to translation to information extraction.

## Related
- [[AI]] - NLP is a subfield of AI
- [[LLMs]] - the most prominent NLP achievement
- [[Tokens]] - how text gets broken down for processing
- [[Tokenization]] - the process of splitting text into tokens
- [[Transformer]] - the architecture that revolutionized NLP
- [[Attention Mechanism]] - the key innovation that made transformers work
- [[Computer Vision]] - the "other side" — images instead of text
- [[Multimodal]] - modern models combine NLP with vision and other modalities
- [[Machine Learning]] - NLP evolved through ML techniques
