---
title: "Embeddings"
---

Embeddings are representation of values or objects like text, images, and audio that are to be consumed by [[Machine Learning Models|machine learning]]and semantic search models.

Important Link: https://www.cloudflare.com/learning/ai/what-are-embeddings/

Embeddings enable Machine Learning models to find similar objects. Given a photo or document a machine learning model that uses embeddings could find a similar photo or document. Embeddings make it possible for computers to understand the relationships between words and other objects, they are foundation for [[Artificial Intelligence]].

## How do Embeddings work?

Embedding is the process of creating vectors using deep learning. An "embedding" is the output of this process. In simpler words: a vector that is created by a deep learning model for the purpose of similarity searches by that model

Embeddings that are "close" to each other can be considered similar. Using embeddings, an algorithm can suggest a relevant TV show, find similar locations, or identify which words are likely to be used together or similar to each other, as in language models

## How do [[Neural Networks]] create embeddings?

Creation of embeddings is a hidden layer which usually takes place before additional layer processes the input. A human would not need to specify where a TV show falls along a hundred different dimensions, a hidden layer in neural networks should do that automatically.

Creating the embedding layer may involve some manual effort at first. A programmer may have to feed examples of how to create an embedding, which dimensions to include, etc. But the embedding layer will be able to operate on its own eventually.

## How are embeddings used in LLMs?

Context of every word becomes in embedding in addition to the word itself. The meanings of entire sentences, paragraphs, and articles can be searched and analyzed. The context for queries can be stored as embeddings, saving time and compute power for future queries