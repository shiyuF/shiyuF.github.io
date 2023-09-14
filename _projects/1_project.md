---
layout: page
title: Stixel Navigation
description: Ego-centric Stereo Navigation Using Stixel World
img: assets/img/research/stixel_cc.gif
importance: 1
category: research
related_publications: 9561385
---

This project explores the use of passive, stereo sensing for vision-based navigation. The traditional approach uses dense depth algorithms, which can be computationally costly or potentially inaccurate. These drawbacks compound when including the additional computational demands associated to the sensor fusion, collision checking, and path planning modules that interpret the dense depth measurements. These problems can be avoided through the use of the stixel representation, a compact and sparse visual representation for local free-space. When integrated into a Planning in Perception Space based hierarchical navigation framework, stixels permit fast and scalable navigation for different robot geometries.
Computational studies quantify the processing performance and demonstrate the favorable scaling properties over comparable dense depth methods. Navigation benchmarking demonstrates more consistent performance across high and low performance compute hardware for PiPS-based stixel navigation versus traditional hierarchical navigation.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/research/stixel_nav.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    (a) Stixels overlaid on a robot’s camera view in a simulated environment. Stixels convert 3D geometry to 2D data that can be reduced to 1.5D data. (b) The GPF-X hierarchical navigation system with a stixel-based, perception-space processing.
</div>

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="assets/video/research/StixelNav_record.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=false %}
    </div>
</div>