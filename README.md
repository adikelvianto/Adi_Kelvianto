# My Portfolio

# [Project 1: Fly-over Waypoint Following Control System of Cirrus Vision SF-50 Aircraft using Artificial Neural Network (ANN)](https://github.com/adikelvianto/Fly-Over_Waypoints_ANN)
This is my undergradute thesis project, with the goals are to develop waypoint following controller ANN model for Cirrus Vision SF50 aircraft and study the relationship between training data that categorized by aircraft roll angle during the mission. This study give results that ANN model generally increase closeness of the aircraft to the waypoint compared to the PID method. It also shown that wider datasets didn't guarantee superior results due to generalizations that model try to made.

What i've done on this project are:
* Set up communication environment to be able retrieve data from X-Plane as flight simulator to be processed in MATLAB/Simulink to give control signal back to X-Plane.
* Tuned PID controller that allow the choosen aircraft accomplish flight mission with least of oscillation or swaying movement. 
* Collected 10 flight missions data with various forms of mission flight path and split each section of waypoint leg based on roll angle range resulting into 4 characterized train datasets.
* Resampled data frequency, removed outliers, data smoothing, and Exploratory Data Analysis (EDA) to select features for the model.
* Created TensorFlow base model and did hyperparameter tuning from 4 different datasets using Bayesian Method that provided by KerasTuner. 
* Convert TensorFlow model so that it can be used in Simulink to validate models performance when controlling aircraft in X-Plane to accomplish flight mission.  
* Analyze effects of train dataset espescially in roll angle range to the perfromance of the controller created from 4 different models trained from different dataset. 

# [Project 2: Neural Style Transfer using AdaIn Method](https://github.com/Artjuna/artjuna-monorepo/tree/main/model/style_transfer)
This is my capstone project at Bangkit Academy 2022 that awarded as top 53 capstone team semifinalist out of 433 teams. My job as machine learning cohort was create style transfer (NST) model using AdaIn Method by utilizing TensorFlow 2.x. Neural style transfer is an optimization technique used to blend two images become one image, where the reconstructed image will preserve the object from content image, while transfering style such as brushstroke from style image.

Image dataset that i used contain of "PASCAL VOC" dataset and validation set of "COCO-2017" as content image (arround 14k images) and style image dataset consisting "Best Artwork of All Time" and "Wikiart" dataset (arround 13k images) 

What i've done on this project are: 
* Processed arround 27k images to have size of 224x224, convert it to *.tfrecords format to enable parallelization training, and split the dataset into train, validation and test dataset. 
* Create style transfer model with AdaIn method, which consist of encoder model that based on sliced VGG-19 pretrained model, decoder that basically inverse of the encoder model also AdaIn function to allign statistical features of content image and style image. 
* Train models with those image datasets for 500 epochs and show the reconstructed image every 10 epochs to see performance of NST model. 

# [Project 3: Avionic Components Failure Prediction Deployed on Website](https://github.com/adikelvianto/Avionic-Components-Failure-Prediction)
This is my internship project at PT. GMF Aeroasia Tbk. for about 3 months. In this project, i created a website to give failure prediction of VHF Omnidirectional Range and Multimode Control Panel components, by using scikit-learn library, HTML, CSS and Flask.

What i've done on this project are: 
* Collected information regarding maintenance from "Internal Component Refurbishment" documents both for VOR component (19 sub test) and Multimode Control Panel component (23 sub test).
* Split dataset into train, validation and test dataset and did "Nested Cross Validation" method to get best hyperparameter for each machine learning algorithm used (Decision Tree, Random Forest, Gradient Boosting, Gaussian Naive Bayes, KNN, MLP).
* Picked 3 best perform algorithm for both component that give best accuracy on test set to be deployed on website. 
* Created structure of the website using HTML with total of  5 pages, designed using CSS and a bit of JavaScript to allow value stored in each toggle button changed when user give a click. 
* Deploy this website by using Flask API and help of Heroku platform as server. 

Result of the deploy website can be found on this link.
[Avionics Component Failure Predicion](https://avionic-failure-prediction.herokuapp.com/)
