---
layout: page
title: FPGA computation accelerator
description: A custom hardware accelerator for DSP-oriented computation with architectural tuning across approximation, custom instructions, and processor configuration.
img: assets/img/DE1.jpg
importance: 2
category: pet
---

This project focused on building a hardware accelerator for DSP-style computation while exploring the trade-offs between accuracy, latency, and resource usage. Rather than treating the datapath in isolation, I tuned the surrounding processor configuration alongside the accelerator so the overall system stayed efficient.

The work covered software approximations, custom instruction design, and full hardware implementation. I investigated mathematical approximations such as Taylor, Maclaurin, Chebyshev, and lookup-based methods before moving key functionality into hardware with CORDIC-based and custom-instruction implementations.

The final design combined architectural tuning with substantial verification work and delivered a large latency reduction at low resource cost.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/fpgablockdiagram.PNG" title="Accelerator block diagram" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Final custom-instruction architecture integrated into the tuned processor design.
</div>
