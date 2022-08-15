# My Portfolio

# Project 1: Fly-over Waypoint Following Control System of Cirrus Vision SF-50 Aircraft using Artificial Neural Network (ANN)
This is my undergradute thesis project, with the goals are to develop waypoint following controller ANN model for Cirrus Vision SF50 aircraft and study the relationship between training data that categorized by aircraft roll angle during the mission. This study give results that ANN model generally increase closeness of the aircraft to the waypoint compared to the PID method. It also shown that wider datasets didn't guarantee superior results due to generalizations that model try to made.

What i've done on this project are 
* Set up communication environment to be able retrieve data from X-Plane as flight simulator to be processed in MATLAB/Simulink to give control signal back to X-Plane.
* Tuned PID controller that allow the choosen aircraft accomplish flight mission with least of oscillation or swaying movement. 
* Collected 10 flight missions data with various forms of mission flight path and split each section of waypoint leg based on roll angle range resulting into 4 characterized train datasets.
* Resampled data frequency, removed outliers, data smoothing, and Exploratory Data Analysis (EDA) to select features for the model.
* Created TensorFlow base model and did hyperparameter tuning from 4 different datasets using Bayesian Method that provided by KerasTuner. 
* Convert TensorFlow model so that it can be used in Simulink to validate models performance when controlling aircraft in X-Plane to accomplish flight mission.  
* Analyze effects of train dataset espescially in roll angle range to the perfromance of the controller created from 4 different models trained from different dataset. 
