---
layout: page
title: "Autonomous Mars Rover"
description: A multi-subsystem rover platform combining embedded control, FPGA vision, and autonomous navigation over a networked control stack.
img: assets/img/marsrover.jpg
importance: 1
category: pet
---

This project was a proof-of-concept autonomous rover designed to navigate cluttered terrain, identify points of interest, and report structured data back to a remote control application. The system combined embedded control, FPGA-based vision, motion planning, and networked telemetry in a single platform.

I primarily worked on the control, vision, and drive portions of the system. That included coordinating peripherals around an ESP32-based controller, building image-processing pipelines for obstacle detection on FPGA hardware, and integrating the routing logic used for autonomous movement.

The project was a strong systems exercise in balancing hardware, low-level software, and real-world integration constraints across a team-built platform.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/rd.PNG" title="Rover subsystem diagram" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    High-level breakdown of the rover subsystems and their interfaces.
</div>

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="assets/video/roverdemo.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=false %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <p>The demo shows autonomous surveying and remote supervision through the control interface. The rover reports detected objects and can also be switched into manual control when needed.</p>
        <p>The vision pipeline used FPGA image processing to detect edges and obstacles in real time, feeding those signals into the navigation and surveying stack.</p>
    </div>
</div>
