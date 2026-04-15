---
layout: page
title: SimonSays
description: A multiplayer rehabilitation game using FPGA-based motion sensing and Python gameplay logic to make physiotherapy more engaging.
img: /assets/img/s2.jpg
importance: 3
category: pet
---

SimonSays is a multiplayer game built around motion-driven interaction for rehabilitation settings. The aim was to make repetitive physiotherapy exercises more engaging by combining a competitive game loop with custom sensing hardware and real-time feedback.

The project used an FPGA-based controller with accelerometers and DSP logic to capture and interpret movement, while the game itself was implemented in Python. The resulting system blended embedded hardware, signal processing, and gameplay design into a single interactive application.

It was a good example of using hardware to support a non-traditional computing application: not just raw performance, but responsiveness, physical interaction, and a better user experience for a specific audience.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/s2.jpg" title="Title screen" class="img" %}
    </div>
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/s1.jpg" title="Gameplay example" class="img" %}
    </div>
</div>
<div class="caption">
    Example screens from the game and its motion-guided interaction flow.
</div>
