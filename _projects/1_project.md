---
layout: page
title: Hybrid TPU-PIM LLM Accelerator
description:
img: assets/img/motivation.png
importance: 1
category: work
giscus_comments: false
---

We focus on the matrix multiplication (MatMul) operations in the projection and attention layers of the LLM architecture.

<div class="row justify-content-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/decoder.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="caption">
    The architecture of decoder-only LLMs. The tokenization and embedding layers are not shown in the figure.
</div>

## Features of 1-bit LLM
- Attention heads require higher precision (8-bit) MatMul
- Projection layer MatMul operations can undergo extreme quantization (1-bit)
- Most of the LLM models have higher percentage of the MatMul operations in the projection layer

<div class="row justify-content-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/motivation.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="caption">
    (a) The 1-bit LLMs divide the model into two portions: attention heads with high-precision MatMul operations (shown in red) and projection layers with low-precision MatMuls (shown in green). (b) The percentage of the low-precision MatMul operations in various OPT models.
</div>

## Proposed Architecture
We suggest a hybrid architecture of Tensor Processing Unit (TPU) and Processing-in-Memory (PIM) system. Basically,
- We perform the high precision MatMul operations into our LLM-specific TPU design
- We shift 1-bit MatMul operations onto PIM system

<div class="row justify-content-center">
    <div class="col-sm-12 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/PIM-LLM-Arch.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="caption">
    The proposed TPU-PIM hybrid architecture. (a) The LLM-specific TPU architecture, (b) The PIM architecture with multiple banks. (b) The PIM tile consists of a network of PEs. (c) The PEs include memristive crossbars to perform MVM operations.
</div>

## Initial results
Initial results show significant performance gains compared to the TPU baselines.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/token/tokens_comparison_128.png" title="example image" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            (a) l=128
        </div>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/token/tokens_comparison_256.png" title="example image" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            (b) l=256
        </div>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/token/tokens_comparison_512.png" title="example image" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            (c) l=512
        </div>
    </div>
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/token/tokens_comparison_1024.png" title="example image" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            (d) l=1024
        </div>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/token/tokens_comparison_2048.png" title="example image" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            (e) l=2048
        </div>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/token/tokens_comparison_4096.png" title="example image" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            (f) l=4096
        </div>
    </div>
</div>

<div class="caption">
    Tokens per second result for various LLMs with different context lengths (l).
</div>

Some of the interesting points include:
- Models with shorter context lengths achieves higher speedup
- Larger models obtain higher speedup
