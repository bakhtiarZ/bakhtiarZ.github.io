---
layout: page
title: "Latent Diffusion Model Accelerator"
description: A parameterisable FPGA dataflow accelerator for latent diffusion inference with layer-wise post-training quantization.
img: assets/img/diffusionmodeldiagram.png
importance: 4
category: phd
---

This project explores how to reduce latent diffusion inference time by targeting per-step latency rather than only reducing the number of denoising steps. The core idea is a parameterisable dataflow architecture for the U-Net that can be instantiated on one or more FPGAs and tuned against quantization, throughput, and hardware cost.

The work spans both hardware and software. On the model side, I used layer-wise post-training quantization and tracked the trade-off between generative quality and implementation cost. On the hardware side, I developed streaming SystemVerilog components for the main network operators and verified them with cocotb and Verilator before integrating them into the accelerator.

The resulting design was implemented on a Xilinx Alveo U250 running at 222 MHz. In its evaluated configuration, the accelerator achieved performance competitive with high-end GPUs while using a custom streaming architecture tailored to the diffusion workload.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/unetwb.png" title="U-Net block diagram instantiated on the FPGA" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Top-level view of the hardware mapping for the U-Net blocks used by the accelerator.
</div>
