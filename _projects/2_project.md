---
layout: page
title: Potential Gap
description: "Potential Gap: A Gap-Informed Reactive Policy for Safe Hierarchical Navigation"
img: assets/img/research/pgap.png
importance: 2
category: research
related_publications: pgap
---

<a href="https://github.com/ivaROS/PotentialGap"><b>GitHub Link</b></a>

This project considers the integration of gap-based local navigation methods with artificial potential field (APF) methods to derive a local planning module, called potential gap, for hierarchical navigation systems. Central to the construction of the local planner is the use of sensory-derived local free-space models that detect gaps and use them for the synthesis of the APF. Trajectories derived from the APF are provably collision-free for idealized robot models. The provable property is lost when applied to more realistic models. A set of algorithm modifications correct for these errors and enhance robustness to non-ideal models, in particular a nonholonomic robot model. Integration of the potential gap local planner into a hierarchical navigation system provides the local goals and trajectories needed for collision-free navigation through unknown environments. Monte Carlo experiments in benchmark worlds confirm the asserted safety and robustness properties.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/research/pgap.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/research/pgap_flowchart.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Hierarchical Navigation System information flow with global planner modules (gray boxes) and local planner modules (blue boxes).
</div>

A presentation video is <a href="https://www.youtube.com/watch?v=OyAR_DvAh_I&list=PPSV">here</a>.
