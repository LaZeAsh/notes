---
title: "Retrieval Augmented Generation"
aliases:
- RAG
---

Explored this concept during HackAIThon 2024

RAG is an alternative to fine-tuning large language models.

Video Link: https://youtu.be/QE-JoCg98iU
## How it works?

![[Pasted image 20240604125129.png]]

RAG from my understanding is a tool to aid LLMs rather than replacing them.

In the example presented in the video it was shown that RAG takes documents that is relevant to the user inquiry from a big database (in this case it may be their water bill for the last few months) and returns the relevant information that Large Language Model can use to return an accurate answer.

This avoids issues like hallucination (where large language model makes up answers), avoids costs of fine-tuning a model, and gives model more up to date information + better context

