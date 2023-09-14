---
layout: page
title: Stixel Navigation
description: Ego-centric Stereo Navigation Using Stixel World
img: assets/img/12.jpg
importance: 1
category: work
related_publications: 9561385
---

This project explores the use of passive, stereo sensing for vision-based navigation. The traditional approach uses dense depth algorithms, which can be computationally costly or potentially inaccurate. These drawbacks compound when including the additional computational demands associated to the sensor fusion, collision checking, and path planning modules that interpret the dense depth measurements. These problems can be avoided through the use of the stixel representation, a compact and sparse visual representation for local free-space. When integrated into a Planning in Perception Space based hierarchical navigation framework, stixels permit fast and scalable navigation for different robot geometries.
Computational studies quantify the processing performance and demonstrate the favorable scaling properties over comparable dense depth methods. Navigation benchmarking demonstrates more consistent performance across high and low performance compute hardware for PiPS-based stixel navigation versus traditional hierarchical navigation.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/research/stixel_nav.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>

You can also put regular text between your rows of images.
Say you wanted to write a little bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, *bled* for your project, and then... you reveal its glory in the next row of images.


<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    (a) Stixels overlaid on a robot’s camera view in a simulated environment. Stixels convert 3D geometry to 2D data that can be reduced to 1.5D data. (b) The GPF-X hierarchical navigation system with a stixel-based, perception-space processing.
</div>

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="assets/video/research/StixelNav_record.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=true %}
    </div>
</div>