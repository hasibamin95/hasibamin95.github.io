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
| NACIM [1]  | 73.9%  | -  | 1.55  | 59  |
| UAE [2]  | 83%  | -  | -  | 154  |
| NAS4RRAM [3]  | 84.4%  | -  | -  | 289  |
| Gibbon [4] (acc opt.)  | 89.2%  | 3.44  | 1.67  | 6  |
| Gibbon [4] (edp opt.)  | 83.4%  | 1.99  | 0.26  | 6  |
| __Our work__  | __91.27%__  | __1.35__  | __0.28__  | __6__  |

[1] Weiwen Jiang, Qiuwen Lou, Zheyu Yan, Lei Yang, Jingtong Hu, Xiaobo Sharon Hu, and Yiyu Shi. Device-circuit-architecture co-exploration for computing-in- memory neural accelerators. IEEE Transactions on Computers. 2021
[2] Zheyu Yan, Da-Cheng Juan, Xiaobo Sharon Hu, and Yiyu Shi. Uncertainty modeling of emerging device based computing-in-memory neural accelerators with application to neural architecture search. 2021 26th Asia and South Pacific Design Automation Conference (ASP-DAC).
[3] Zhihang Yuan, Jingze Liu, Xingchen Li, Longhao Yan, Haoxiang Chen, Bingzhe Wu, Yuchao Yang, and Guangyu Sun. Nas4rram: neural network architecture search for inference on rram-based accelerators. Science China Information Sciences, 64(6):160407, May 2021.
[4] Hanbo Sun, Zhenhua Zhu, Chenyu Wang, Xuefei Ning, Guohao Dai, Huazhong Yang, and Yu Wang. Gibbon: An efficient co-exploration framework of nn model and processing-in-memory architecture. IEEE Transactions on Computer-Aided Design of Integrated Circuits and Systems, 42(11):4075–4089, 2023.
