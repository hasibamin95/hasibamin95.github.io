---
layout: page
title: Hybrid TPU-PIM LLM Accelerator
description:
img: assets/img/motivation.png
importance: 1
category: work
giscus_comments: false
---

We compute the low-precision MatMuls on PIM hardware.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/decoder.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="caption">
    The architecture of decoder-only LLMs. The tokenization and embedding layers are not shown in the figure.
</div>


