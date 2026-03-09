---
tags:
  - concept
status: covered
---

# Guardrails / Safety

> [!info] In short
> The rules, filters, and safety mechanisms placed around an AI system to prevent it from producing harmful, biased, or off-topic outputs.

[[LLMs]] are powerful, but they can produce harmful, biased, or just plain wrong outputs if left unchecked. Guardrails are the safety layers that keep AI systems behaving responsibly.

Like the safety systems in a modern car. You have preventive controls (lane-departure warning that catches you before you drift), active controls (steering and braking that keep you on track), and reactive controls (airbags that deploy if something still goes wrong). No single system is enough on its own — you layer them together.

Guardrails operate at three levels:
1. **Input guardrails** — check what goes into the AI. They detect prompt injection attacks (where someone tries to trick the AI into ignoring its [[System Prompt|instructions]]), filter out sensitive personal data, and validate that queries are in scope
2. **Behavioral guardrails** — shape how the AI thinks. This includes training techniques like RLHF (Reinforcement Learning from Human Feedback) and the [[System Prompt]] itself
3. **Output guardrails** — check what comes out. They scan responses for toxic language, bias, personal information, policy violations, or [[Hallucination|hallucinated]] content before the response reaches the user

There's always a trade-off here — more aggressive guardrails mean slower responses and more false positives (blocking legitimate queries). Teams have to calibrate based on their risk tolerance. For regulated industries like healthcare, finance, or legal, guardrails aren't optional — they're a compliance requirement.

The OWASP Top 10 for LLM Applications is a widely referenced checklist for the most critical security risks in LLM deployments — a good starting point for any team deploying AI.

## Related
- [[System Prompt]] - one layer of guardrails
- [[Hallucination]] - guardrails help catch it
- [[AI Engineering]] - guardrails are essential for production
- [[Inference]] - guardrails wrap around the inference process
