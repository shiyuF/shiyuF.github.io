---
layout: page
title: Safer Gap
description: "Safer Gap: A Gap-based Local Planner for Safe Navigation with Nonholonomic Mobile Robots"
img: assets/img/research/safer_gap.png
redirect: https://github.com/ivaROS/SaferGap
importance: 5
category: research
related_publications: feng2023safer
---

This project extends the gap-based navigation technique in Potential Gap by guaranteeing safety for nonholonomic robots for all tiers of the local planner hierarchy, so called Safer Gap. The first tier generates a Bezier-based collisionfree path through gaps. A subset of navigable free-space from the robot through a gap, called the keyhole, is defined to be the union of the largest collision-free disc centered on the robot and a trapezoidal region directed through the gap. It is encoded by a shallow neural network zeroing barrier function (ZBF). Nonlinear model predictive control (NMPC), with Keyhole ZBF constraints and output tracking of the Bezier path, synthesizes a safe kinematically-feasible trajectory. Lowlevel use of the Keyhole ZBF within a point-wise optimization-based safe control synthesis module serves as a final safety layer. Simulation and experimental validation of Safer Gap confirm its collision-free navigation properties.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/research/safer_gap_flowchart.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Hierarchical navigation system with Safer Gap local planner. Red blocks are perception module to generate egocircle. Blue blocks are planning modules. Green block is the control module.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/research/safer_gap_jbg.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/research/safer_gap.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    <b>Left:</b> Bezier trajectory synthesis. p(0) is the robot origin. b(1)1 and b(2)1 are the second and third control points for the first cubic B´ezier curve. Blue lines Ll and Lr are left and right gap sides. Red circle is the largest circular free space in egocircle. Ql and Qr are the left and right intersection points of Gcirc and gap sides. Local waypoint pwpt is inside the inflated safe region Finf to guarantee safety. pcirc is the goal biased point on Ginf,circ. Dashed lines show the Bezier polygons. The combination of brown and cyan paths is the final synthesized path.
    <b>Right:</b> Joined Bezier paths for all gaps. Blue is egocircle L. Yellow are 5 detected gaps. Green points are local waypoints pwpt. Black paths are the synthesized Bezier paths P. Red path is the selected P based on the scoring equation.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/research/safer_gap_real.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Real experiment topview. Three environment densities are shown. The green paths are the robot’s real traces. Robots start from left to the right.
</div>

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="assets/video/research/IROS23BGap.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=false %}
    </div>
</div>
