---
layout: page
title: Stereo Learning Trajectories
description: "Learning-based collision free trajectories from stereo images"
img: assets/img/research/stereo_learning_sparse_gazebo_2.png
importance: 6
category: research
related_publications: 
---

Deep learning helps trajectory selection in local planner with stereo vision system. The motivation is searching for potential collision-free local trajectories without estimating dense depth image from stereo camera. We use Fine-tune AlexNet to classify local trajectory samples with sensor inputs, stereo image pairs and ego laserscan information.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/research/data_collection_gazebo.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/research/collision-free-left.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/research/collision-free-trajs.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The training data is collected from the Gazebo simulation. Obstacles are randomly spawned in front of the Turtlebot. Trajectories are generated with 51 uniformly distributed departure angles. Then our PiPS (planning in perception space) collision checking algorithm is used to obtain collision-free samples. Stereo image pairs (grayscale), ego laserscan information are collected as the inputs. Trajectories’ lengths are used to compute label for each departure angle. Threshold is set as 4.0m.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/research/stereo_learning_3.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/research/stereo_learning_5.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/research/stereo_learning_sparse_gazebo_2.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

During model training, the training dataset is divided into training set and validation set to tune parameters.

Except for focusing on the testing accuracy, we need to evaluate the approach with our collision checking and navigation strategy. First, the selected trajectories are visualized in the depth image to check the rationality. Then the informed deep learning sampled trajectory will be integrated in the local planner.

In the bottom figure, the colorized departure angles are the output deep network. Different colors represent different confidences. Red means a higher confidence. Top 5 trajectories are generated from the corresponding angles. Then collision checking performs on the selected trajectories.