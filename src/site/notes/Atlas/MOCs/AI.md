---
{"dg-publish":true,"permalink":"/atlas/mo-cs/ai/","tags":["📍","📥"],"updated":"2024-11-09T07:34:54.252-08:00"}
---

"AI" in scare quotes because it's not really AI yet.
## Basics
- https://www.fast.ai/ - Learn AI
## LLMs
- Ollama for running models locally
## RAG
- https://vectorize.io/multimodal-rag-patterns/
	- Basically, store vector encodings in the same vector space across all content types.
	- Pattern 3 in the above is about storing pointers to the raw file for later retrieval when your LLM is multimodal and needs access to the source data
	- If you don't need the source data, you can use Pattern 1, which is to just encode a text description. e.g. You take the image and run it through a "describe this image" and then use the resulting text for your encoding.
## Agentic RAG

## Other pages
- [[Atlas/MOCs/Pose Estimation\|Pose Estimation]]
- [[Atlas/Atomic Notes/Variational Autoencoder\|Variational Autoencoder]]

{ .block-language-dataview}