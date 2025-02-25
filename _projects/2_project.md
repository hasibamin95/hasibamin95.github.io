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
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/method_new.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Hierarchical sampling of subnet from supernet. (a) building blocks, (b) NN architecture buildup by depth sampling, (c) block sampling, (d) output channel sampling via slicing of the weight matrix, and (e) layerwise weight and activation quantization for mixed precision quantization search.
</div>

<div class="row justify-content-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/flow-new.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Optimization flow for the proposed co-optimization framework
</div>

We obtained promising results on CIFAR-10 datasets, both in terms of accuracy and energy efficiency.

| Method  | PIM Accuracy | Latency (ms)  | EDP (mJ X ms)  | Search time (h) |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| NACIM  | 73.9%  | -  | 1.55  | 59  |
| UAE  | 83%  | -  | -  | 154  |
| NAS4RRAM  | 84.4%  | -  | -  | 289  |
| Gibbon (acc opt.)  | 89.2%  | 3.44  | 1.67  | 6  |
| Gibbon (edp opt.)  | 83.4%  | 1.99  | 0.26  | 6  |
| This work  | 91.27%  | 1.35  | 0.28  | 6  |
