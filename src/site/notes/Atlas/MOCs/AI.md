---
{"dg-publish":true,"permalink":"/atlas/mo-cs/ai/","tags":["📍"],"updated":"2024-10-30T07:55:39.806-07:00"}
---

"AI" in scare quotes because it's not really AI yet.

# LLMs
- Ollama for running models locally

# RAG
- https://vectorize.io/multimodal-rag-patterns/
	- Basically, store vector encodings in the same vector space across all content types.
	- Pattern 3 in the above is about storing pointers to the raw file for later retrieval when your LLM is multimodal and needs access to the source data
	- If you don't need the source data, you can use Pattern 1, which is to just encode a text description. e.g. You take the image and run it through a "describe this image" and then use the resulting text for your encoding.

# Agentic RAG