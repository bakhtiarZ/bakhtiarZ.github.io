---
layout: page
title: "Autonomous Mars Rover"
description: a project to develop a proof of concept mars rover, purposed to autonomously survey complex terrain and relay accurate data. over HTTP.
img: assets/img/marsrover.jpg
importance: 1
category: work
---

This project was part of my 2nd year at Imperial College London. I worked in a group of 6 students and we were tasked to develop a proof of concept rover with 6 seperate subsystems involved. 

These subsystems included:
 - Control: This subsystem was responsible for connecting all the peripherals together and maintining proper overall function of the rover. All routing decisions were made within this subsystem and data transfer over HTTP was also implemented. This subsystem used a dual-core ESP32 with WiFi capabilities.
 - Vision: In order to avoid obstacles and survey the simulated Mars environment, the rover used FPGA based computer vision. Due to the low cost of components and aim of power efficiency, machine learning algorithms were not implemented and instead image processing using digital electronics were implemented.
 - Command: Serving as a simulated 'mission control' for the mars rover, a webserver application was developed. This would communicate with the rover and receive data about the obstacles and terrain it surveyed. This included coordinate locations of hazardous areas and possible extra-terrestrial habitats. In addition, it also had functionality for manual control of the rover and monitoring of its battery.
 - Drive: This subsystem encompassed how the rover moved around and its routing algorithm. The functionality needed was accurate routing via a coordinate or movement instructions.
 - Power and Energy: This section is responsible for supplying the rover, namely the controller, FPGA, and motors with energy. It is also the section responsible for developing a charging station which utilises solar energy. 
 - Radar: The radar subsystem was used to detect any possible metal machinery which would be indicative of advanced life-forms. This was implemented using a doppler radar.


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/rd.PNG" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    A block diagram of the rover's subsystems.
</div>


<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="assets/video/roverdemo.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=false %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <p>This is a short video demo of the Mars Rover in action, the coloured balls represent 'interesting' objects and the rover is moving autonomously to survey the area, reporting accurate data back to the webserver application. It is also possible to control the rover manually via the webserver which is shown in the video.
        During this project, I primarily worked on the control, vision, and drive subsystems. These incorporated a lot of knowledge of hardware design and low level software engineering. One feature the demo does not show is the obstacle avoidance, this was done using the FPGA camera and a routing algorithm.</p> 
        <b>Below are the skills I developed during this project:</b>
        <ul>
        <li> C++ </li>
        <li> Python </li>
        <li> SystemVerilog </li>
        <li> Image processing </li>
        <li> Embedded systems (ESP32) </li>
        </ul>
    </div>
</div>

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/objectdetection.jpg" title="Object Detection" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <p>This is an image of the object detection algorithm, the striped building simulated an obstacle as these are often jagged with harsh edges. The lines shown on the image represent edges being detected using image processing methods. This version of the processed image would count as data and feed into the surveying and routing algorithms.</p> 
    </div>
</div>
