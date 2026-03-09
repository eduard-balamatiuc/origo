---
tags:
  - concept
status: covered
---

# Tokens

> [!info] In short
> The actual units [[LLMs]] work with — not words, not letters, but sub-word pieces. Everything the model reads and writes is made of tokens.

Think of LEGO bricks. You could build a house out of one giant custom piece for every object (a "sofa" brick, a "fireplace" brick), but that would mean you need millions of unique pieces. Instead, LEGO gives you a manageable set of small, reusable bricks that snap together to build anything. Tokens work the same way — instead of giving the model a unique piece for every word in every language, you give it a set of reusable sub-word pieces that combine to represent any text.

You might assume that [[LLMs]] work with words. That would be the intuitive thing. But it doesn't work well in practice. English alone has hundreds of thousands of words, and then there are misspellings, slang, technical jargon, other languages, code, numbers... You'd end up with a vocabulary so massive the model couldn't handle it. And every time someone invented a new word or made a typo, the model would have no idea what to do.

So instead, LLMs use something called sub-word [[Tokenization]]. The most common method is Byte Pair Encoding (BPE) — it's an algorithm that looks at a huge pile of text and figures out which chunks of characters appear together most often, then treats those as tokens. Common words like "the" or "is" stay as single tokens. But a word like "unbelievable" gets split into pieces like "un" + "believ" + "able." The model has seen those pieces in tons of other words, so it can handle "unbelievable" even if it's never seen that exact word before. In English, one word is roughly 1.3 tokens on average — so the mapping is pretty close but not one-to-one.

Here's where it gets practically interesting. Everything is tokens — not just words. Numbers, spaces, punctuation, code, emojis — all tokens. And different languages get tokenized very differently. English is efficient because most tokenizers were trained on tons of English text, so common English words map to single tokens. But languages like Japanese, Chinese, or Korean can use 2-4x more tokens to express the same idea. That directly affects [[Cost and Pricing]] — if you're using an LLM API and your content is in Japanese, you're paying significantly more per message than you would for the same content in English, because the model is processing more tokens.

The token system also explains some weird LLM behaviors. Ask a model "how many r's are in strawberry?" and it might get it wrong. Why? Because the model doesn't see individual letters. It might see "straw" + "berry" as two tokens — and it never actually looks inside those tokens at the character level. It's like asking someone to count the dots on a pair of dice that are glued shut — they know the dice represent numbers, but they can't see the individual dots. This is also why LLMs struggle with spelling tasks, character-level puzzles, and precise letter counting. And practically speaking, tokens define your [[Context Window]] limit. When a model says it supports "128K tokens," that's roughly 96,000 English words — but could be much less in other languages or for code-heavy content.

## Related
- [[LLMs]] - tokens are what LLMs work with
- [[Tokenization]] - the process of breaking text into tokens
- [[Next Token Prediction]] - the core task of LLMs
- [[Cost and Pricing]] - LLM pricing is based on tokens
- [[Context Window]] - measured in tokens, not words
- [[Numerical Representation]] - tokens get converted to numbers for the model
