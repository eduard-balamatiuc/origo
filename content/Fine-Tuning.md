---
tags:
  - concept
status: covered
---

# Fine-Tuning

> [!info] In short
> Taking a [[Pre-Training|pre-trained]] model and further training it on specific data to specialize it for a particular use case.

Like training a general physician to become a cardiologist. They already know medicine broadly — now you're sharpening their expertise in one specific area.

After [[Pre-Training]] gives a model broad language understanding, fine-tuning narrows and sharpens it. You take the pre-trained model and continue [[Training]] it on a much smaller, carefully curated dataset specific to your needs — your company's support tickets, legal documents, medical records, internal policies, whatever. The model adjusts its [[Model Parameters|parameters]] slightly so it becomes better at your particular task.

While pre-training costs millions, fine-tuning can range from a few hundred to a few thousand dollars depending on the model size and dataset. Modern techniques like LoRA make this even cheaper by only updating a small fraction of the parameters rather than all of them.

The decision of whether to fine-tune, use [[RAG]], or rely on [[Prompt Engineering]] is actually more of a business decision than a technical one. Fine-tuning works best when you need consistent behavior and you have high-quality domain-specific [[Data]]. [[RAG]] is often better when your data changes frequently.

## Related
- [[Pre-Training]] - what happens before fine-tuning
- [[Training]] - fine-tuning is a type of training
- [[RAG]] - an alternative approach to specialization
- [[Prompt Engineering]] - another alternative, no training needed
- [[Data]] - you need good domain-specific data
