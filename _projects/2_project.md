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

\begin{table}[]
\centering
\caption{Performance comparison against different PIM-oriented NAS methods on CIFAR-10 dataset.}
\resizebox{\columnwidth}{!}{%
\begin{tabular}{ccccc}
\hline
\multirow{2}{*}{Method} & PIM & Latency & EDP & Search   \\
       & Accuracy & ($ms$) & ($mJ\times ms$) & time (h)  \\  \hline
NACIM \cite{nacim} & 73.9\% & - & 1.55 & 59  \\
UAE \cite{uae} & 83\% & - & - & 154  \\
NAS4RRAM \cite{nas4rram} & 84.4\% & - & - & 289 \\
%NAX \cite{nax} & 92.7\% & - & 290 & 32      \\
%AnalogNAS \cite{analogNAS} & 92.07\% &  \\
Gibbon \cite{gibbon} (acc opt.) & 89.2\% & 3.44 & 1.67 & 6  \\
Gibbon \cite{gibbon} (edp opt.) & 83.4\% & 1.99 & 0.26 & 6  \\ \hline
CrossNAS ($w_{acc}$=0.99) & 91.27\% & 1.35 & 0.28 & 6\\
%CrossNAS ($w_{acc}$=0.9) & 89.27\% & 0.71 & 0.13 & 5.5\\
CrossNAS ($w_{acc}$=0.8) & 88.09\% & 0.577 & 0.073 & 5\\
%CrossNAS ($w_{acc}$=0.6) & \\
\hline
\end{tabular}}
\label{tab:compare}
\end{table}

| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |

