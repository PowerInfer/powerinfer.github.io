---
layout: page
title: About
permalink: /about/
---

## Welcome to PowerInfer

At PowerInfer, we are dedicated to pushing the boundaries of large language model (LLM) performance on consumer-grade hardware. Our mission is to make high-speed, efficient LLM inference accessible to everyone, leveraging innovative techniques to maximize the potential of everyday computing resources. Below is an overview of our groundbreaking research projects.

### [PowerInfer: Fast Large Language Model Serving with a Consumer-grade GPU](https://arxiv.org/abs/2312.12456)

PowerInfer is our flagship high-speed LLM inference engine designed for personal computers equipped with a single consumer-grade GPU. Our research uncovers the power-law distribution in neuron activation during LLM inference, revealing that a small subset of neurons (hot neurons) are consistently activated across inputs, while the majority (cold neurons) vary.

**Key Innovations:**
- **GPU-CPU Hybrid Inference Engine:** By preloading hot neurons onto the GPU and computing cold neurons on the CPU, we significantly reduce GPU memory demands and minimize CPU-GPU data transfers.
- **Adaptive Predictors and Neuron-aware Sparse Operators:** These optimizations enhance the efficiency of neuron activation and computational sparsity.

**Performance:**
PowerInfer achieves an impressive average token generation rate of 13.20 tokens per second, peaking at 29.08 tokens per second, across various LLMs, including OPT-175B, on a single NVIDIA RTX 4090 GPU. This performance is only 18% lower than that of a server-grade A100 GPU and outperforms llama.cpp by up to 11.69x, all while maintaining model accuracy.

At PowerInfer, we continue to explore and develop cutting-edge techniques to democratize access to high-performance LLM inference, making advanced AI technology more accessible and practical for a broader audience. Stay tuned for more exciting updates and breakthroughs!

## Links

- [GitHub Repo](https://github.com/SJTU-IPADS/PowerInfer)
- [Hugging Face Models](https://huggingface.co/PowerInfer)

