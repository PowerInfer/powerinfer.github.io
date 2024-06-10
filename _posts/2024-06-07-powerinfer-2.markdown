---
layout: post
title:  "PowerInfer-2:"
date:   2024-06-03 03:00:45 +0000
categories: jekyll update
permalink: /v2/
---
## TL;DR

Today we're thrilled to introduce our efficient inference framework for smartphones, PowerInfer-2. We support up to Mixtral 47B MoE models with a speed of 11.1 tokens/s, up to 22x speedup compared with other state-of-the-art framework. For 7B models, even we just place 50% model weight on the phones, we still have the SOTA speed! 功耗XXX

Demo here.

## Background

The trend of deploying large models on mobile devices is becoming increasingly evident. Google has introduced AI Core, enabling the deployment of Gemini Nano on smartphones. Various smartphone manufacturers are also exploring ways to implement large models on mobile devices to enhance data privacy and other benefits. However, the models currently runnable on mobile devices are quite small and consume significant memory, which severely limits the application scenarios for large models.

## Features

PowerInfer-2 is a high-speed inference engine for deploying activation-sparse LLMs for smartphones.

PowerInfer-2 is fast with:

- Heterogenous computing: Decompose coarse-grained matrix computations into fine-grained "neuron clusters," and then dynamically adjust the size of these clusters based on the characteristics of different hardware components.

- I/O-Compute Pipeline: Neuron caching and fine-grained neuron-level pipelining techniques aim to maximize the overlap between neuron loading and computation.

## Evaluation

Place some evaluation result here

## Models

PowerInfer is a model-system co-design solution that requires strong predictable sparsity at the model level. Currently, mainstream models primarily use the SwiGLU structure, which does not exhibit strong predictable sparsity. To enhance this property, we have made certain modifications to the models.

We introduce two new models: TurboSparse-Mistral 7B and TurboSparse-Mixtral 47B. These models are modified versions of Mistral and Mixtral, respectively, ensuring not only enhanced model performance but also stronger predictable sparsity. Notbly, our models are trained with 150B tokens.这里突出一下150B,成本不高

Figure here.
