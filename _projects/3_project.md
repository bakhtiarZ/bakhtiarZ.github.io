---
layout: page
title: FPGA computation accelerator
description: A hardware based accelerator for functions related to DSP applications. This project was part of my 3rd year at Imperial College London.
img: assets/img/DE1.jpg
importance: 2
category: work
---

<p> This project was part of my 3rd year at Imperial College London. I was tasked to develop a hardware based accelerator for functions related to DSP applications. This project was research focused, prioritising thorough and reasoned investigations of possible performance increases. Another goal of the project was efficiency. The accelerator design was aimed at finding the optimal point where the design had adequate performance and efficiency. Throughout the project, many designs were considered that investigated different points on the Parento front. </p>

<p> The project was split into 3 main parts: </p>
<ul> The first part covered developing a base implementation using a more simple function. Later, processor parameters such as cache sizing, arithmetic unit count, and memory bandwidth were varied to investigate the effects on performance and efficiency. Extra areas of investigation included usage of differnt memories within the SOC, optimsation of the branch predictor, and compiler optimsation tuning</ul>
<ul> The second part regarded mathematical approximations of the function to be computed, these included the taylor & maclaurin series, chebyshev approximations, and lookup implementations of the cosine function. These were initially implemented in software. Extensions included investigations into the precision / performance tradeoff of the approximations and also a software implementation of floating point division. </ul>
<ul> The final part of the project was to implement the entire function and calculation in hardware. This involved heavy use of custom instructions and the programming of a CORDIC block. Investigations into pipelined, folded, and combinatorial implementations were conducted. In addition, large amounts of testbenching and verification was done to ensure an Mean-Squared-Error less than 10^-10. Extensions to this final part included parallelisation in hardware and pipelining of multiple instruction calls.</ul>
<p> Throughout the project, the processor was repeatedly tuned to account for the changes in the accelerator. For instance, once the custom instruction was implemented, the instruction cache could be drastically reduced. This tuning helped keep the resource usage down to a minimum. In the final rendition of the design, there was a 99.95% reduction in latency with only 4.772% resource usage.</p>


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/fpgablockdiagram.PNG" title="Block Diagram" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    A block diagram of the final architecture for the custom instruction. This sat inside a processor with tuned parameters..
</div>