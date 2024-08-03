---
title: "Virtual Large Language Model (vLLM)"
aliases:
- vLLM
---

vLLM stands for Virtual Large Language Model and is an open source library that supports LLMs in inferencing and model serving efficiently

Article Link: https://www.hopsworks.ai/dictionary/vllm
## Background

vLLM was first introduced in a paper `Efficient Memory Management for Large Language Model Serving with Paged Attention` authored by Kwon et al. The paper identified several issues with LLMs main of which being memory allocation which can lead to negative impact on their performance

The paper specifically emphasizes the inefficiency of managing Key-Value cache memory in current LLM serving systems. This can result in slow inference speed and high memory footprint


## Solution

To fix this issue the paper presents `PagedAttention` an algorithm inspired by virtual memory and paging techniques used commonly used in operating systems. 

PagedAttention enables efficient memory management by allowing for non-contiguous (objects not adjacent or sequentially connected) storage of attention keys and values

Following this idea the paper develops vLLM, a LLM serving engine built on PageAttention. vLLM achieves near-zero waste in KV cache memory.

## Other techniques used

vLLM uses a lot of techniques to optimize LLM serving

- Continuous Batching: Incoming requests are continuously batched together to maximize hardware utilization and reduce computing waste (minimizing idle time)
- Quantization: vLLM utilized quantization techniques like FP16 to optimize memory usage
- Optimized CUDA Kernels: vLLM hand-tunes the code executed on the GPU for maximum performance. 

