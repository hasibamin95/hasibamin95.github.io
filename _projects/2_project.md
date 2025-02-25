---
layout: page
title: SW/HW Co-optimization of PIM Systems
description:
img: assets/img/method_new.png
importance: 2
category: work
giscus_comments: false
---

We use the Single-Path One-shot weight sharing approach on PIM systems.

<div class="row justify-content-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/method_new.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Hierarchical sampling of subnet from supernet. (a) building blocks, (b) NN architecture buildup by depth sampling, (c) block sampling, (d) output channel sampling via slicing of the weight matrix, and (e) layerwise weight and activation quantization for mixed precision quantization search.
</div>

<div class="row justify-content-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/flow-new.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Optimization flow for the proposed co-optimization framework
</div>

We obtained promising results on CIFAR-10 and CIFAR-100 datasets.

| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |

