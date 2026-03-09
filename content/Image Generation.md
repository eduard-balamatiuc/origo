---
tags:
  - concept
status: covered
---

# Image Generation

> [!info] In short
> AI systems that create images from text descriptions — you type what you want to see, and the model generates it from scratch.

[[AI]] isn't just about understanding things — it can create them too. Image generation is the branch of AI where models produce entirely new images from a text description you give them, and the results have gotten shockingly good in just a few years.

Imagine an art restorer who's given a canvas covered in random paint splatters. They slowly, carefully clean away the mess, and with each pass the image underneath becomes a little clearer — until a full painting emerges. That's roughly how diffusion models work, except the "painting underneath" never existed before. The model has learned what things look like from millions of images, so when you say "a cat sitting on a spaceship," it starts from pure noise and gradually refines it into something that matches your description.

Before diffusion models took over, the dominant approach was GANs (Generative Adversarial Networks). GANs worked by pitting two [[Neural Network|neural networks]] against each other — one generates fake images, the other tries to spot the fakes. It was clever, but tricky to train and prone to weird failure modes. Around 2020-2021, diffusion models showed up and basically overtook GANs on image quality and reliability. The idea is counterintuitive: you take a real image, gradually add random noise until it's pure static, and then train a model to reverse that process — to go from noise back to a coherent image. Do that millions of times with millions of images, and the model learns how to generate new images by starting from random noise and "denoising" step by step.

The text-to-image part is where things get really interesting. Models like DALL-E, Midjourney, and Stable Diffusion don't just generate random images — they generate images that match a text prompt you give them. This works because the model learns to connect text descriptions with visual concepts during training. So when you type "a watercolor painting of a fox reading a newspaper," the model uses that text to guide the denoising process toward an image that fits. This is where [[Prompt Engineering]] shows up again — the way you phrase your prompt dramatically affects what you get. The more specific and descriptive you are, the better the result.

The big three products you'll hear about are DALL-E (made by OpenAI, the same company behind ChatGPT), Midjourney (known for its artistic, stylized outputs), and Stable Diffusion (open source, meaning anyone can download and run it). This mirrors the [[Open vs Closed Models]] split you see in text AI: DALL-E and Midjourney are closed services you access through their platforms, while Stable Diffusion lets you run it on your own hardware, customize it, and fine-tune it for specific styles. Each has its strengths — Midjourney tends to produce the most aesthetically pleasing images, DALL-E is strongest at following complex prompts accurately, and Stable Diffusion gives you the most control and flexibility.

One thing you can't talk about image generation without mentioning is the controversy. These models were trained on billions of images scraped from the internet, including artwork by living artists who never consented to this use. There are ongoing lawsuits — artists have sued Stability AI and Midjourney for copyright infringement, and courts are still working through what's legal and what's not. Beyond copyright, there are concerns about deepfakes and misinformation — when anyone can generate photorealistic images of events that never happened, that's a real problem. The technology is powerful, but the ethical and legal frameworks are still catching up.

## Related
- [[Computer Vision]] - image generation is the flip side of CV (creating images vs. understanding them)
- [[Deep Learning]] - diffusion models are deep learning architectures
- [[Multimodal]] - modern multimodal models can both understand and generate images
- [[Neural Network]] - the building block behind all image generation approaches
- [[Prompt Engineering]] - how you write your prompt shapes what the model generates
- [[Open vs Closed Models]] - Stable Diffusion is open, DALL-E and Midjourney are closed
