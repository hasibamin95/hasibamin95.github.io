---
layout: page
title: Reliability-Aware NN Deployment on Analog PIM
description:
img: assets/img/arch.png
importance: 4
category: work
giscus_comments: false
---

We use analog horizontal and vertical partitioning approach for reliability-aware deployment of NN models on PIM hardware.

<div class="row justify-content-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/xbar/partition.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The Xbar-partitioning approach. (a) Horizontal partitioning (H_P = 2), and (b) vertical partitioning (V_P = 2) in an analog IMC array. (c) Parasitic capacitance and resistance model.
</div>

We design custom layouts for different types of memory bitcells.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/xbar/1t1r.png" title="example image" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            (a) 1T-1R
        </div>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/xbar/2t1r.png" title="example image" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            (b) 2T-1R
        </div>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/xbar/1tg1r.png" title="example image" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            (c) 1TG-1R
        </div>
    </div>
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/xbar/2t1rsot.png" title="example image" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            (d) 2T-1R
        </div>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/xbar/3t1r.png" title="example image" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            (e) 3T-1R
        </div>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/xbar/1tg1t1r.png" title="example image" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            (f) 1TG-1T-1R
        </div>
    </div>
</div>

<div class="caption">
    Schematic and layout designs for different bitcells
</div>

We deploy DNN workloads on different crossbar sizes.
<div class="row justify-content-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/xbar/deploy.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Deployment of a 400 × 120 × 84 × 10 DNN on fully-analog IMC architecture with (a) 32 × 32 (b) 64 × 64, (c) 128 × 128 and (d) 256 × 256 subarrays.
</div>

We analyze the proposed approach in terms of accuracy, power consumption, area and signal-to-noise ratio accross different bitcells, technologies and crossbar sizes.

Read the following papers for more information.

- M. H. Amin, M. E. Elbtity and R. Zand, "Xbar-Partitioning: A Practical Way for Parasitics and Noise Tolerance in Analog IMC Circuits," in IEEE Journal on Emerging and Selected Topics in Circuits and Systems, vol. 12, no. 4, pp. 867-877, Dec. 2022, doi: 10.1109/JETCAS.2022.3222966.
- M. Elbtity, A. Singh, B. Reidy, X. Guo and R. Zand, "An In-Memory Analog Computing Co-Processor for Energy-Efficient CNN Inference on Mobile Devices," 2021 IEEE Computer Society Annual Symposium on VLSI (ISVLSI), Tampa, FL, USA, 2021, pp. 188-193, doi: 10.1109/ISVLSI51109.2021.00043.
- Md Hasibul Amin, Mohammed Elbtity, Mohammadreza Mohammadi, and Ramtin Zand. 2022. MRAM-based Analog Sigmoid Function for In-memory Computing. In Proceedings of the Great Lakes Symposium on VLSI 2022 (GLSVLSI '22). Association for Computing Machinery, New York, NY, USA, 319–323. https://doi.org/10.1145/3526241.3530376
- M. H. Amin, M. Elbtity and R. Zand, "Interconnect Parasitics and Partitioning in Fully-Analog In-Memory Computing Architectures," 2022 IEEE International Symposium on Circuits and Systems (ISCAS), Austin, TX, USA, 2022, pp. 389-393, doi: 10.1109/ISCAS48785.2022.9937884.
