---
layout: page
title: "Latent Diffusion Model Accelerator"
description: a project to develop a data-flow design aimed to be instantiated over one or multiple FPGAs with the goal of reducing diffusion model inference latency by speeding up per step computations. (Ongoing)
img: assets/img/diffusionmodeldiagram.png
importance: 1
category: work
---

This project is my final year project for my MEng Electronic and Information Engineering degree at Imperial College London. It aims to reduce the inference latency of diffusion models by targetting the per timestep latency. This will be done by instantiating an optimial and parameterised data-flow design that implements the denoising neural network (U-Net). This work is done in assosciation with the DeepWok Lab (https://deepwok.github.io/).

The abstract for this project is as follows:

Diffusion models achieve state of the art image synthesis and boast powerful generative capabilities.
In particular, Latent Diffusion Models [1] are capable of generating high-resolution images that
beat alternative methods [2]. However, diffusion models suffer from a long and iterative generation
process which consumes a great deal of computational resources. There has been a strong effort
to reduce this computational need by reducing the number of iterations (or sampling steps) the
diffusion model must undergo, but there has been limited work in reducing per-step latency. This
project encompasses the development of the custom hardware and software used to accelerate
Latent Diffusion Model inference within a tolerable loss in generative quality. A significant goal of
the work is to develop open-source hardware and software in order to encourage global collaboration
to aid the goal of efficient computation. The development of this open-source accelerator will be
the first of its kind and could lead to more research being conducted. This aspect is inspired by
projects such as lowRisc [3] and the MASE [4] repository which are open-source projects with a
focus on quality, efficiency, and robustness of the components developed

Due to the large complexity of the project, it cannot be fully described in this portfolio. But a diagram for the top level design is below. Overall, many components were developed in SystemVerilog and verified using CocoTB with Verilator. The highly optimised data-streaming design using a quantised latent diffusion model achieved a 4x performance improvement against competing GPUs with a tolerable loss of generative quality.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/unet.png" title="U-Net to be implemented" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    An accurate system level diagram of the indivudal layers within the neural network. These will be instantiated on the FPGA.
</div>


