---
tags:
  - concept
status: covered
---

# AI Regulation

> [!info] In short
> The growing set of laws and rules that governments are putting in place to control how AI systems are built, deployed, and used — think of it as the legal side catching up to the technology.

As [[AI]] systems move from research labs into real products that affect people's lives — hiring decisions, loan approvals, medical diagnoses — governments have started asking: who's responsible when these things go wrong? If you're managing or overseeing AI projects, regulation is the thing you can't afford to ignore even though it's still a moving target. Right now, the most comprehensive framework is the **EU AI Act**, which entered into force in August 2024 and becomes fully applicable by August 2026. It uses a risk-based classification system with four tiers. **Unacceptable risk** covers things that are outright banned — social scoring by governments, manipulative AI techniques, emotion recognition in workplaces and schools. **High risk** includes AI used in hiring, credit decisions, education, and law enforcement — these systems need thorough documentation, human oversight, and conformity assessments before they can be deployed. **Limited risk** means lighter transparency requirements — basically, if someone is talking to a chatbot, they need to know it's AI. And **minimal risk** covers most everyday AI applications and is essentially unregulated. If your product touches the EU market, this applies to you regardless of where your company is based — kind of the same as GDPR.

The US takes a very different approach. There's no single comprehensive federal AI law. Instead, you've got a patchwork. The Biden administration issued executive orders on AI safety in 2023, which the Trump administration revoked in January 2025 in favor of a "remove barriers to AI leadership" stance. Then in December 2025, a new executive order tried to establish a national AI policy framework that would preempt state-level AI laws — because by that point, multiple states had passed their own regulations, creating a messy compliance landscape for companies operating across state lines. So the US situation right now is genuinely uncertain: state laws are going into effect while the federal government is actively trying to override some of them.

China has moved fast too, but with a narrower, topic-by-topic approach rather than one sweeping law. They've rolled out specific regulations for recommendation algorithms, deepfakes, generative AI services, and — as of late 2025 — AI companions and chatbots. China's broader AI law is being drafted and could land in 2026 or 2027. The strategic goal is pretty clear: regulate enough to maintain social stability and data control, but not so much that it slows down the AI race.

Here's the honest part: enforcement is still a real challenge everywhere. Many EU countries are still setting up the agencies that will actually oversee the AI Act. US companies are dealing with conflicting federal and state requirements. And the technology moves so fast that by the time a regulation is finalized, the AI landscape has already shifted. If you're a project manager or director, the practical takeaway is this: start documenting your AI systems now — what data they use, what decisions they influence, what [[Guardrails]] you have in place. Build compliance readiness into your process from the start rather than trying to retrofit it later. You don't need to have all the answers, because honestly, the regulators don't either. But showing that you've thought about risk, bias, and transparency will put you in a much better position no matter which regulatory framework ends up applying to you.

## Related
- [[Guardrails]] - the technical controls that help you meet regulatory requirements
- [[Bias in AI]] - a major reason regulation exists in the first place
- [[AI Engineering]] - regulation shapes how you build and deploy AI systems
- [[Open vs Closed Models]] - regulatory obligations differ depending on model type and access
- [[AI]] - regulation applies across the whole field
