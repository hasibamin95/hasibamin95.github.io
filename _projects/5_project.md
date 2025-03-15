---
layout: page
title: Approximate TPU
description:
img: assets/img/APTPU.png
importance: 5
category: work
giscus_comments: false
---

We design approximate arithmetic units for highly-efficient implementation of Tensor Processing Units. Specifically, we design custom pre-approximate units (PAU) and approximate processing elements (APEs). We perform design space exploration with different approximate MAC units.

<div class="row justify-content-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/APTPU.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The APTPU architecture including five main components: weight/IFMAP memories, FIFOs, controller, pre-approximate units (PAUs), and approximate processing elements (APEs).
</div>

Read the following papers for more information.

- M. E. Elbtity, P. S. Chandarana, B. Reidy, J. K. Eshraghian and R. Zand, "APTPU: Approximate Computing Based Tensor Processing Unit," in IEEE Transactions on Circuits and Systems I: Regular Papers, vol. 69, no. 12, pp. 5135-5146, Dec. 2022, doi: 10.1109/TCSI.2022.3206262
- Mohammed E Elbtity, Md Hasibul Amin, Hossam Hassan, et al. Design Automation and Quantitative Analysis of Approximate Arithmetic Circuits. TechRxiv. October 07, 2024.


