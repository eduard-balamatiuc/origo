---
tags:
  - concept
status: covered
---

# Computer Vision (CV)

> [!info] In short
> The field of AI that teaches machines to "see" — to understand and make decisions based on images, video, and other visual data.

Think of a quality inspector at a factory who stares at thousands of products sliding by on a conveyor belt, spotting tiny scratches or defects. Computer Vision is like cloning that inspector — except the clone never gets tired, never blinks, and can check a thousand items per second.

Computer Vision is all about getting machines to extract useful information from visual stuff — photos, video feeds, medical scans, satellite images, you name it. When you unlock your phone with your face, that's CV. When a Tesla detects a stop sign, that's CV. When a radiologist's software highlights a suspicious spot on a lung X-ray, that's CV too.

For years, the go-to architecture for CV was the Convolutional Neural Network (CNN). CNNs work by scanning an image in small patches, detecting low-level features first (edges, textures) and building up to high-level ones (faces, objects). They were kind of the breakthrough that made CV actually useful — before CNNs, computer vision was pretty rough. The real-world applications are everywhere: self-driving cars use CV to detect lanes, pedestrians, and other vehicles in real time. Manufacturing plants use it for automated quality control, catching defects that a human eye would miss. In healthcare, [[Deep Learning]]-based CV models can detect cancers, retinal diseases, and fractures from medical images, sometimes more accurately than trained specialists. And facial recognition — love it or hate it — powers everything from airport security to unlocking your phone.

More recently, the field has shifted toward Vision Transformers (ViTs), which apply the same [[Transformer]] architecture that powers [[LLMs]] but for images. Instead of scanning in patches like a CNN, a Vision Transformer chops an image into a grid of patches and processes them kind of the same way a language model processes words. This turned out to work really well, especially for large-scale tasks.

The biggest shift right now is [[Multimodal]] models — systems that bridge vision and language. Models like GPT-4o, Gemini, and Claude can look at an image and answer questions about it, describe what's happening, or even generate images from text descriptions. This blurs the line between CV and [[Natural Language Processing]] in a way that would have seemed like science fiction just a few years ago. You're no longer building a separate "vision system" and a separate "language system" — it's all one model that can see and talk.

## Related
- [[AI]] - CV is a subfield of AI
- [[Deep Learning]] - most modern CV runs on deep learning
- [[Multimodal]] - modern models combine vision with language
- [[Natural Language Processing]] - the "other side" — text instead of images
- [[Neural Network]] - CNNs are a type of neural network
- [[Transformer]] - Vision Transformers brought the transformer revolution to CV
