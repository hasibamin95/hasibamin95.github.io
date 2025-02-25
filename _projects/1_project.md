---
layout: page
title: Hybrid TPU-PIM LLM Accelerator
description:
img: assets/img/motivation.png
importance: 1
category: work
giscus_comments: false
---

There are matrix multiplication (MatMul) operations in the projection and attention layers of the LLM architecture.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/decoder.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="caption">
    The architecture of decoder-only LLMs. The tokenization and embedding layers are not shown in the figure.
</div>

In the 1-bit LLM, the attention heads are designed with high-precision matmul operations and the projection layers operate with low-precision MatMul operations. We observe that most of the LLM models have higher percentage of the MatMul operations in the projection layer. So, we shift the projection layer operations into PIM hardware.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/motivation.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="caption">
    (a) The 1-bit LLMs divide the model into two portions: attention heads with high-precision MatMul operations (shown in red) and projection layers with low-precision MatMuls (shown in green). (b) The percentage of the low-precision MatMul operations in various OPT models.
</div>
