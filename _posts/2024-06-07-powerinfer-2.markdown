---
layout: post
title:  "PowerInfer-2:"
date:   2024-06-03 03:00:45 +0000
categories: jekyll update
permalink: /v2/
---
## TL;DR

Today, we're excited to introduce PowerInfer-2, our highly optimized inference framework designed specifically for smartphones. PowerInfer-2 supports up to Mixtral 47B MoE models, achieving an impressive speed of 11.68 tokens per second, which is up to 23 times faster than other state-of-the-art frameworks. Even with 7B models, by placing just 50% of the FFN weights on the phones, PowerInfer-2 still maintains state-of-the-art speed!

Demo here.

## Background

The trend of deploying large models on mobile devices is rapidly gaining interest. Google has introduced AI Core, enabling the deployment of Gemini Nano on smartphones. Various smartphone manufacturers are also exploring ways to implement large models on mobile devices to enhance data privacy and other benefits. However, the models currently runnable on mobile devices are relatively small and consume significant memory, severely limiting the application scenarios for large models.

## Features

PowerInfer-2 is a high-speed inference engine for deploying activation-sparse LLMs for smartphones.

PowerInfer-2 is fast with:

- Heterogenous computing: Decompose coarse-grained matrix computations into fine-grained "neuron clusters," and then dynamically adjust the size of these clusters based on the characteristics of different hardware components.

- I/O-Compute Pipeline: Neuron caching and fine-grained neuron-level pipelining techniques aim to maximize the overlap between neuron loading and computation.

## Evaluation

Place some evaluation result here

## Models

PowerInfer is a model-system co-design solution that requires strong predictable sparsity at the model level. Currently, mainstream models primarily use the SwiGLU structure, which does not exhibit strong predictable sparsity. To enhance this property, we have made certain modifications to the models.

We introduce two new models: TurboSparse-Mistral-7B and TurboSparse-Mixtral-47B. These models are sparsified versions of Mistral and Mixtral, respectively, ensuring not only enhanced model performance but also higher predictable sparsity. Notbly, our models are trained with just 150B tokens within just 0.1M dollars.

<img src="../figures/takeaway.png" alt="avatar" width="300" height="200"/>
