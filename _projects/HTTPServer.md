---
layout: page
title: HTTP Server library
description: A low-latency C++ HTTP server and support library built for high-volume request handling in a performance-sensitive environment.
img: assets/img/httpthumb.jpg
importance: 3
category: pet
---

This project focused on building a low-latency HTTP server library in C++ for handling large request volumes with predictable performance. The work centered on efficient request handling, lightweight parsing, and a design that could scale without introducing avoidable latency.

Key implementation areas included event-driven request processing, socket-level networking, HTTP parsing, response generation, and the surrounding reliability features needed in production-quality infrastructure. Performance work covered concurrency choices, throughput tuning, and general latency-sensitive design decisions.

The project was a useful exercise in systems programming under tight performance constraints and remains one of the projects that shaped my interest in low-level software.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/httpservarchitecture.drawio(1).png" title="Architecture diagram" class="img" %}
    </div>
</div>
<div class="caption">
    Top-level view of the software architecture for the HTTP server library.
</div>
