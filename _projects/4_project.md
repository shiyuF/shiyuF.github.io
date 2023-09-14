---
layout: page
title: Quadrupedal Navigation
description: "GPF-BG: A Hierarchical Vision-Based Planning Framework for Safe Quadrupedal Navigation"
img: assets/img/research/quadNav_real.png
importance: 4
category: research
related_publications: 10160804
---

Safe quadrupedal navigation through unknown environments is a challenging problem. This project proposes a hierarchical vision-based planning framework (GPF-BG) integrating our previous Global Path Follower (GPF) navigation system and a gap-based local planner using B´ezier curves, so called Bezier Gap (BG). This BG-based trajectory synthesis can generate smooth trajectories and guarantee safety for pointmass robots. With a gap analysis extension based on non-point, rectangular geometry, safety is guaranteed for an idealized quadrupedal motion model and significantly improved for an actual quadrupedal robot model. Stabilized perception space improves performance under oscillatory internal body motions that impact sensing. Simulation-based and real experiments under different benchmarking configurations test safe navigation performance. GPF-BG has the best safety outcomes across all experiments.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/research/quadNav_flowchart.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    GPF-BG hierarchical navigation system. The red blocks include perception space. Blue blocks present following and tracking modules. The dashed arrows indicate the option to choose either egocylinder or egocircle for collision checking.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/research/quadNav_bg.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/research/quadNav_epl.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/research/quadNav_erl.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    <b>Left:</b> Bezier trajectory synthesis. p0 is the robot origin. Q1 is the second control point. Blue lines Ll and Lr are left and right gap lines. Red circle is the largest circular free space in egocircle. Ql and Qr are the left and right intersection points of Gcirc and Gtri. L0,1 is the line segment constructed by p0 and Q1, and also represents the robot orientation. L1,l is the line through Q1 and Ql. Local way point pwpt is inside the condensed safe region Fs to guarantee safety. Dashed lines show the B´ezier polygon. Brown is the synthesized trajectory. 
    <b>Middle:</b> Equivalent passing length. (a) lep finding. Black arrow is robot orientation. Blue arrow is gap direction. α is the angle difference between robot orientation and gap direction. D is the distance to the virtual pose. Red line lep is normal to gap direction. (b) An example of lep(α,D). The robot geometry is 0.7m x 0.3m. νd = 0.2m/s, ωd = 0.5rad/s. It shows the dependence on robot orientation.
    <b>Right:</b> Equivalent radial length. (a) The red solid line is ler. Two red dashed curves are the largest and smallest circle arcs that can enclose virtual robot boundary. (b) An example of ler(α,D).
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/research/quadNav_real.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Unitree A1 quadruped navigates an unknown, constrained environment. Depicts robot navigation paths for GPF-BG (green) and TEB (red).
</div>

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="assets/video/research/quadNav.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=false %}
    </div>
</div>
