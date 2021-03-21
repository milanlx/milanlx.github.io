---
layout: archive
title: "Project"
permalink: /project/
author_profile: true
youtubeId: detectionVideo
---

{% include base_path %}


Research Projects 
------ 
* *Using Multi-modal Transportation Data For Energy Prediction and Management in Buildings*
  * **motivation**: Urban systems, including transporations and buildings are highly interrelated given the spatial-temporal flow of system users. The change of magnitude of occupancy in one system can be in proportion to the fluctuation in one another. In this project we aim at investigating the edge potential of predicting the energy profile of buildings, from the rich and fine-grained transportation data including realtime traffic flow intensity, and public transit status. The refined prediction would further facilitate energy-efficient demand-based building control. [link](https://www.nsf.gov/awardsearch/showAward?AWD_ID=1637222)


* *Enhancing Vision-based Vehicle Detection and Tracking with Transportation Domain Features*
  * **motivation**: Given the rapid development in visual analytics, data sensing and transmission, an integration of the rich and diverse information would bring new perspective to urban traffic tracking for Intelligent Transportation Systems (ITS), which aims at improving urban mobility, reducing congestion and boosting travel safety by analyzing key traffic parameters including speed, volume, and density. Traditionally, these parameters are mainly inferred from data captured by loop detectors, which is costly and only sparsely deployed in city scale. As an alternative, vision-based inference have been widely applied due to high precision of convolutional models as well as cost effectiveness of camera as sensors. However, the performance of pure vision techniques may be hampered by the high occlusion, low resolution and strong sunlight reflection natures that occur often in transportation environments. Thus, in this series of research the authors explore the effectiveness of fusing domain features captured by existng transportation sensors with vision-based models for traffic parameter inference. Specifically, we have leveraged traffic features with convolutional neural networks to estimate vehicle density and speed (through tracking) separately. Compared with pure visual techniques, it is validated that the inclusion of domain features can improve the overall performance, and we look forward to expanding the model for other transportation related tasks in future. 
 
  * **detection**: The detailed implementation can be found [here](https://milanlx.github.io/files/trans_detection.pdf)


  * **tracking**: to be added. 
{% include youtubePlayer2.html id=page.detectionVideo %}
<p align="center"><img src='/images/tracking_framework.png'></p>


Course Projects 
------ 

Interests
------  
* *Comparing MPC and PID controllers: a simple case*
  * **motivation**: There is a trend that some of the PID controllers are being replaced by more advanced one, i.e., Model predictive controller (MPC). However, in what aspects that MPC would make improvement is not theoretically clear. As a starting point, the following [dicussion](https://github.com/milanlx/milanlx.github.io/blob/master/files/LQR_PID.pdf) aims to reveal the difference between the two controllers on first order systems. (to be continued)   
