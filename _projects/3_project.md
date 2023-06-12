---
layout: page
title: HTTP Server library
description: a project undertaken during my 6 month placement at JP Morgan.
img: assets/img/httpthumb.jpg
importance: 3
category: work
---
<p> As part of a challenging project, I undertook the development of a low latency HTTP server library using C++. The goal of the project was to create a performant and scalable library that could handle high volumes of incoming HTTP requests with minimal latency. </p>

<p>To achieve this, I started by conducting extensive research on existing HTTP server libraries and protocols to understand the best practices and performance optimization techniques. This allowed me to design a robust architecture for the library that would prioritize low latency and high throughput.</p>

<p>The development process involved several key components:</p>

<p><b>Event-driven Architecture:</b> I implemented an event-driven architecture using C++ to handle incoming requests asynchronously. This approach ensured that the server could efficiently handle multiple concurrent connections without blocking or incurring unnecessary overhead.</p>

<p><b>Socket Programming:</b> I utilized C++ socket programming techniques to establish and manage connections with clients. This included handling socket creation, binding, and listening for incoming connections.</p>

<p><b>HTTP Parsing:</b> I implemented a lightweight and efficient HTTP parsing mechanism to extract relevant information from incoming requests. This involved processing request headers, URL parameters, and request bodies.</p>

<p><b>Multithreading:</b> To further enhance performance, I incorporated multithreading techniques to handle concurrent requests efficiently. This allowed the server to process multiple requests in parallel, leveraging the available CPU cores effectively.</p>

<p><b>Response Generation:</b> I designed a response generation module to construct and send appropriate HTTP responses to clients. This involved handling different HTTP status codes, content types, and response headers.</p>

<p><b>Performance Optimization:</b> Throughout the development process, I focused on optimizing the library for low latency and high throughput. This included techniques such as connection pooling, request pipelining, and data compression to minimize latency and improve overall performance.</p>

<p><b>Error Handling and Logging:</b> I implemented robust error handling mechanisms to gracefully handle exceptions and prevent crashes. Additionally, I incorporated logging functionality to record important events and aid in troubleshooting.</p>

<p>During the project, I conducted extensive testing to ensure the library's stability and performance under various scenarios, including high request loads and stress testing. I also collaborated with other developers and received feedback to continuously improve the library's efficiency and usability.</p>

<p>In conclusion, the development of the low latency HTTP server library using C++ was a complex and demanding project. Through careful architectural design, efficient coding practices, and performance optimization techniques, I was able to create a high-performance HTTP server library capable of handling large volumes of requests with minimal latency. </p>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/httpservarchitecture.drawio.png" title="Architecture diagram" class="img" %}
    </div>
</div>
<div class="caption">
    A top level diagram of the software architecture.
</div>
<br><br>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/httpserv.png" title="Work Breakdown Structure diagram" class="img" %}
    </div>
</div>
<div class="caption">
    A diagram of the project layout, this provides an overview of the relevant deliverables.
</div>