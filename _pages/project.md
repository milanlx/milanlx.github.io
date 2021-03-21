---
layout: archive
title: "Project"
permalink: /project/
author_profile: true
youtubeId: detectionVideo
---

{% include base_path %}


Research Projects 
--------------
* *Using Multi-modal Transportation Data For Energy Prediction and Management in Buildings*
  * **motivation**: Urban systems, including transporations and buildings are highly interrelated given the spatial-temporal flow of system users. The change of magnitude of occupancy in one system can be in proportion to the fluctuation in one another. In this project we aim at investigating the edge potential of predicting the energy profile of buildings, from the rich and fine-grained transportation data including realtime traffic flow intensity, and public transit status. The refined prediction would further facilitate energy-efficient demand-based building control. [link](https://www.nsf.gov/awardsearch/showAward?AWD_ID=1637222)


* *Enhancing Vision-based Vehicle Detection and Tracking with Transportation Domain Features*
  * **motivation**: Given the rapid development in visual analytics, data sensing and transmission, an integration of the rich and diverse information would bring new perspective to urban traffic tracking for Intelligent Transportation Systems (ITS), which aims at improving urban mobility, reducing congestion and boosting travel safety by analyzing key traffic parameters including speed, volume, and density. Traditionally, these parameters are mainly inferred from data captured by loop detectors, which is costly and only sparsely deployed in city scale. As an alternative, vision-based inference have been widely applied due to high precision of convolutional models as well as cost effectiveness of camera as sensors. However, the performance of pure vision techniques may be hampered by the high occlusion, low resolution, large perspective and strong sunlight reflection natures that occur often in transportation environments. Thus, in this series of research the authors explore the effectiveness of fusing domain features captured by existng transportation sensors with vision-based models for traffic parameter inference. Specifically, we have leveraged traffic features with convolutional neural networks to estimate vehicle density and speed (through tracking) separately. Compared with pure visual techniques, it is validated that the inclusion of domain features can improve the overall performance, and we look forward to expanding the model for other transportation related tasks in future. 
 
  * **detection**: The detailed implementation can be found [here](https://milanlx.github.io/files/trans_detection.pdf)


  * **tracking**: The speed estimation problem is tackled by traking-by-detection framework. Basically, we have fine-tuned YOLO with self-labelled data as detector, and adopted Deepsort framework as tracker. However, we used LSTM network trained with transportation features instead of the Kalman filter as the state estimation module. A sample of the result can be found in the video below. 
                                 <p align="center"><img width="910" height="470" src='/images/tracking_framework.png'></p>
                                                   {% include youtubePlayer2.html id=page.detectionVideo %}


Course Projects 
------------- 
* *Object Counting by Leveraging CNN and LSTM with Multi-Source of Input*
  * Designed and implemented a framework by leveraging CNN, LSTM and residual layer for vehicle counting, given input images suffering from low framerate, low resolution, high occlusion and large perspectives. 
  * Trained and validated the model on TRANSCOS dataset with ~1200 images, evaluated the effectiveness of various data augmentation tricks such as flipping, cropping, and adjusting contrast/brightness. 
  * Attained a 4.47 MAE that is comparable to state-of-the-art models. The full report can be found [here](https://milanlx.github.io/files/10707_project.pdf)

