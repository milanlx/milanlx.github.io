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
  * **Motivation**: Urban systems, including transporations and buildings are highly interrelated given the spatial-temporal flow of system users. The change of magnitude of occupancy in one system can be in proportion to the fluctuation in one another. In this project we aim at investigating the edge potential of predicting the energy profile of buildings, from the rich and fine-grained transportation data including realtime traffic flow intensity, and public transit status. The refined prediction would further facilitate energy efficiency for demand-based building control [link](https://www.nsf.gov/awardsearch/showAward?AWD_ID=1637222). 

      <p align="center"><img width="650" height="225" src='/images/transResearch/motivation.png'></p>
      
   * **Correlation analysis**: Firstly, regression analysis was conducted to find and justify the most important factors from transportation domain. By implementing real-time data processing pipeline on 10G transportation dataset from public transit and inrix, we pre-selected citywide traffic features together with historical building electricity to build the spatial-temporal model. By further fine-grained analyzing in different time-of-day and day-of-week scale, it is validated that traffic features have significant impact on building electricities during weekdays, and the inclusion of these covariate can boost prediction performance especially during special event. In all, the fused model achieved a R2 of 0.91, which improved 18% when compared with baseline. The details of the project can be found [here](https://milanlx.github.io/files/trans_to_building_baseline.pdf)

      
      <p align="center">
          <img src="/images/transResearch/feature_weekday.png" width="45%" />
          <img src="/images/transResearch/example_weekday.png" width="45%" /> 
      </p>
      
  * **Spatial-temporal Graph Neural Network**: features including impact of time-of-day, day-of-week, etc. 


      <p align="center">
          <img src="/images/transResearch/gnn_outline.png" width="45%" />
          <img src="/images/transResearch/gnn_model.png" width="45%" /> 
      </p>



* *Enhancing Vision-based Vehicle Detection and Tracking with Transportation Domain Features*
  * **Motivation**: Intelligent Transportation Systems (ITS) are critical components to strengthen travel safety, reduce congestion and improve urban mobilities. The reliability of the system rely on spatial-temporal analytics of key traffic parameters such as density, volume, and speed, which are inferred from sensors including loop detectors and cameras using computer vision. However, the former sensors suffer from high initial costs, and the latter may deteriorate in high occlusion and large perspective cases. Thus, in this series of research we explore the effectiveness of fusing features captured by existing transportation sensors and vision-based models for traffic parameter inference. Specifically, we have leveraged domain features with convolutional neural networks to estimate vehicle density and speed (through tracking) separately. Compared with pure visual techniques, it is validated that the inclusion of domain features improves the overall performance, and we look forward to expanding the model for other transportation tasks in future.
 
  * **Detection**: To esimate the density of vehicles, we implemented a model with CNN+rLSTM module for image inputs, and LSTM module for processed transportation features including location of buses and average traffic speed. Compared with pure vision-based detection model YOLO, we have reduced the MAE from 0.73 to 0.27, and justified the effectiveness of domain features. The detailed implementation can be found [here](https://milanlx.github.io/files/trans_detection.pdf). 


  * **Tracking**: The speed estimation problem is tackled by tracking-by-detection framework. Basically, we have fine-tuned YOLO with self-labelled data as detector, and adopted Deepsort framework as tracker. However, we used LSTM network trained with transportation features instead of the Kalman filter as the state estimation module. Tested on one hour's data, it is validated that the fused model improved MOTP from 78.5% to 80.6%, and MOTA from 65.7% to 68.3% respectively. A sample result is attached below. 
                                 <p align="center"><img width="910" height="470" src='/images/tracking_framework.png'></p>
                                                   {% include youtubePlayer2.html id=page.detectionVideo %}


Course Projects 
------------- 
* *Object Counting by Leveraging CNN and LSTM with Multi-Source of Input*
  - Designed and implemented a framework by leveraging CNN, LSTM and residual layer for vehicle counting, given input images suffering from low framerate, low resolution, high occlusion and large perspectives. 
  - Trained and validated the model on TRANSCOS dataset with ~1200 images, evaluated the effectiveness of various data augmentation tricks such as flipping, cropping, and adjusting contrast/brightness. 
  - Attained a 4.47 MAE that is comparable to state-of-the-art models. The full report can be found [here](https://milanlx.github.io/files/10707_project.pdf). 

* *Regression Analysis*
  - Investigated patterns and developed classification models that help to refine advertising strategies for regular check-ups in less developed countries. The full report is listed [here](https://milanlx.github.io/files/36707_project3.pdf). Essentially,
  - A random forest model is chosen to rank the importance of covariates that motivate regular check-ups.
  - A logistic regression model is implemented to identify key features and reference likelihood of the people that can be potentially persuaded for check-up. 

