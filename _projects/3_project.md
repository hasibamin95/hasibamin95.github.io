---
layout: page
title: Simulation Framework for Analog PIM
description:
img: assets/img/imac-sim/imac-sim-cover.jpg
importance: 3
category: work
giscus_comments: false
---

We propose IMAC-Sim, a circuit-level simulation framework for analog PIM architecture. [GitHub](https://github.com/iCAS-Lab/IMAC-Sim)

<div class="row justify-content-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/imac-sim/imac_flow.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Block diagram of the IMAC-Sim framework.
</div>

We perform design space exploration of analog PIM architecture using IMAC-Sim.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/imac-sim/acc_new.png" title="example image" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            (a) Accuracy
        </div>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/imac-sim/pow_new.png" title="example image" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            (b) Power Consumption
        </div>
    </div>
</div>
<div class="caption">
     The results obtained for the deployment of a 400×120×84×10 DNN model on IMAC with various subarray sizes, memristive technologies, and bitcell types.
</div>

<div class="row justify-content-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/imac-sim/color2.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Accuracy results obtained from IMAC-Sim (a) without parasitics, (b) with parasitics, and (c) with parasitics and partitioning.
</div>

Read the following paper for more information.

- Md Hasibul Amin, Mohammed E. Elbtity, and Ramtin Zand. 2023. IMAC-Sim: A Circuit-level Simulator For In-Memory Analog Computing Architectures. In Proceedings of the Great Lakes Symposium on VLSI 2023 (GLSVLSI '23). Association for Computing Machinery, New York, NY, USA, 659–664. https://doi.org/10.1145/3583781.3590264
