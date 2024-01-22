---
layout: page
title: "Latent Diffusion Model Accelerator"
description: a project to develop a data-flow design aimed to be instantiated over one or multiple FPGAs with the goal of reducing diffusion model inference latency by speeding up per step computations. (Ongoing)
img: assets/img/diffusionmodeldiagram.png
importance: 1
category: work
---

This project is my final year project for my MEng Electronic and Information Engineering degree at Imperial College London. It aims to reduce the inference latency of diffusion models by targetting the per timestep latency. This will be done by instantiating an optimial and parameterised data-flow design that implements the denoising neural network (U-Net). 

This project is my largest to date and is not completed yet. Here is an excerpt from my interim report that introduces the problem scenario. In the following weeks, as the project is completed, this page will be filled with relevant implementation details and results.

*My project encompasses the development of a parameterised hardware design for the time dependant neural
network used within diffusion models and other score based generative models. The goal of this design is
to reduce latency in diffusion model inference. Furthermore, by implementing extensive parameterization,
automated generation of specific hardware designs is possible*


And below is a top level figure which describes the U-Net which will be developed in hardware. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/unet.png" title="U-Net to be implemented" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    An accurate system level diagram of the indivudal layers within the neural network. These will be instantiated on the FPGA.
</div>


