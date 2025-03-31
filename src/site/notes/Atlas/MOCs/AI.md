---
{"dg-publish":true,"permalink":"/atlas/mo-cs/ai/","tags":["📍"],"updated":"2025-01-11T09:34:14.480-08:00"}
---

"AI" in scare quotes because it's not really AI yet.
## Basics
- https://www.fast.ai/ - Learn AI
## LLMs
- Ollama for running models locally

## Tools
- [LibreChat](https://www.librechat.ai/docs/features) - open source tool for building AI chat bots locally
- [SenseVoice](https://github.com/FunAudioLLM/SenseVoice) - open source Speech to Text
## RAG
- https://vectorize.io/multimodal-rag-patterns/
	- Basically, store vector encodings in the same vector space across all content types.
	- Pattern 3 in the above is about storing pointers to the raw file for later retrieval when your LLM is multimodal and needs access to the source data
	- If you don't need the source data, you can use Pattern 1, which is to just encode a text description. e.g. You take the image and run it through a "describe this image" and then use the resulting text for your encoding.
## Agentic RAG

## Other pages
- [[_meta/prompts/Skill Tutor\|Skill Tutor]]
- [[Atlas/MOCs/Pose Estimation\|Pose Estimation]]
- [[Atlas/Atomic Notes/Variational Autoencoder\|Variational Autoencoder]]

{ .block-language-dataview}