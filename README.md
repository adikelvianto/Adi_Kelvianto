# About Me



# My Projects

## [Analysis of Divvy Company Dataset in 2021 using R]([https://github.com/adikelvianto/Auto_Landing_DL](https://www.kaggle.com/code/adikelvianto29/analysis-of-divvy-2021-dataset-using-r))
### October 2022

## [Development of Auto Landing Deep Learning Model for Boeing 747 Aircraft](https://github.com/adikelvianto/Auto_Landing_DL)
### October 2022
This project aim to create **auto landing deep learning model** using TensorFlow by utilizing **"Flight Data Recorcder"** data. 
* First process done is **preprocessing the FDR data** which have a big size each flight and consisting a lot of noise, until we have dataset for training, validation, and testing.
* There are two models built, elevator model and throttle model, with the step by step process can be shown in following notebook [Build Model - Elevator.ipynb](https://github.com/adikelvianto/Auto_Landing_DL/blob/main/Build%20Model%20-%20Elevator.ipynb), [Build Model - Throttle.ipynb](https://github.com/adikelvianto/Auto_Landing_DL/blob/main/Build%20Model%20-%20Throttle.ipynb)
* The next development of this project is to deploy it to MATLAB/Simulink and X-Plane to see wether this models can do their job as an auto landing control system.

## Result

* [Elevator model](https://github.com/adikelvianto/Auto_Landing_DL/blob/main/model/elevator_model.h5) work **really well** in predicting elevator deflection on landing phase. The predicted and actual trend is very similar, eventhough some of graphs shown the predicted value have **offset** value, but it **never exceed 4 degrees**. Hence, this model could be said well performed. This picture below shown sample of predicted value vs actual test set value for the elevator deflection. 

<p align="center">
<img width="1307" alt="Elevator Comparison" src="https://user-images.githubusercontent.com/92104520/196446972-d92fe034-d835-4562-9993-a1ab18730c35.png">
</p>

* [Throttle model](https://github.com/adikelvianto/Auto_Landing_DL/blob/main/model/throttle_model.h5) also **work well** in terms of following pilot behavior in deflecting 4 units of power lever angle (Since the aircraft have 4 engines). The problem for this model is the prediction value tends to **fluctuate** rather than having constant value to create step input graph. The comparison between model prediction and actual power lever angle value can be seen from this picture below. 

<p align="center">
<img width="897" alt="PLA Comparison" src="https://user-images.githubusercontent.com/92104520/196449142-dda478d9-03d1-4ad6-8ee5-dfe12e6aea59.png">
</p>


## [Deep Learning Based Fly-Over Waypoints Control System for Business Jet Aircraft](https://github.com/adikelvianto/Fly-Over_Waypoints_ANN)
### September 2022
This is my undergradute thesis project, with the goals are to **develop waypoint following controller deep learning model** espescially for **Cirrus Vision SF50** aircraft and **study the relationship between training data** that categorized by aircraft roll angle during the mission. This study give results that deep learning model generally increase closeness of the aircraft to the waypoint compared to the PID method, eventhough the dataset used is a piece of sliced data. It also shown that **wider datasets didn’t guarantee superior results** due to generalizations that model try to made.

What I've done on this project are:
* **Set up communication environment** to be able retrieve data from X-Plane as flight simulator to be processed in MATLAB/Simulink to give control signal back to X-Plane.
* **Tuned PID controller** that allow the choosen aircraft accomplish flight mission with least of oscillation or swaying movement. 
* **Collected** 10 flight **missions data** with various forms of mission flight path and split each section of waypoint leg based on roll angle range resulting into **4 characterized train datasets**.
* **Resampled data frequency, removed outliers, data smoothing, and Exploratory Data Analysis (EDA)** to select features for the model.
* Created TensorFlow base model and did **hyperparameter tuning** from 4 different datasets using **Bayesian Method** that provided by **KerasTuner**. 
* **Convert TensorFlow model** so that it can **be used in Simulink** to **validate** models performance when controlling aircraft **in X-Plane** to accomplish flight mission.  
* **Analyze** effects of train dataset espescially in **roll angle range** to the perfromance of the controller created from 4 different models trained from different dataset. 


## [Neural Style Transfer using AdaIn Method](https://github.com/Artjuna/artjuna-monorepo/tree/main/model/style_transfer)
### June 2022
This is my **capstone project** at **Bangkit Academy 2022** that awarded as **top 53** capstone team **semifinalist** out of 433 teams. My job as machine learning cohort was create Neural Style Transfer (NST) model using AdaIn Method by utilizing TensorFlow 2.x. **Neural style transfer** is an optimization technique used to **blend two images** become one image, where the reconstructed image will **preserve the object from content image**, while **transfering style** such as brushstroke from style image.

Image dataset that i used contain of **"PASCAL VOC"** dataset and validation set of **"COCO-2017"** as content image (arround **14k** images) and style image dataset consisting **"Best Artwork of All Time"** and **"Wikiart"** dataset (arround **13k** images) 

What i've done on this project are: 
* **Processed** arround **27k images** to have size of 224x224, **convert** it to **tfrecords** format to enable **parallelization training**, and **split the dataset** into train, validation and test dataset. 
* Create style transfer model with **AdaIn** method, which consist of **encoder** model that based on sliced **VGG-19** pretrained model, **decoder** that basically inverse of the encoder model also AdaIn function to allign statistical features of content image and style image. 
* **Train models** with those image datasets for 500 epochs and show the reconstructed image every 10 epochs to see performance of NST model. 

<p align="center">
 <img width="897" alt="Example Result" src="https://user-images.githubusercontent.com/92104520/185745237-39e97e3d-624e-4e4d-ba90-442dea43182a.png">
</p>

## [Prototype Webiste based Application for Avionic Components Failure Prediction](https://github.com/adikelvianto/Avionic-Components-Failure-Prediction)
### December 2021
This is my **internship** project at** PT. GMF Aeroasia Tbk**. for about **4 months**. In this project, I created a **website** to give **failure prediction** of VHF Omnidirectional Range (VOR) and Multimode Control Panel components, by using **scikit-learn** library, **HTML, CSS and Flask.**

What I've done on this project are: 
* Collected information regarding maintenance from "Internal Component Refurbishment" documents both for VOR component (19 sub test) and Multimode Control Panel component (23 sub test) to **create 2 datasets**.
* **Split dataset** into train, validation and test dataset and did "**Nested Cross Validation**" method to get **best hyperparameter** for each machine learning algorithm used (Decision Tree, Random Forest, Gradient Boosting, Gaussian Naive Bayes, KNN, MLP).
* **Picked 3** best perform algorithm for both component that give **best accuracy** on test set **to be deployed** on website. 
* Created structure of the website using HTML with total of **5 pages**, designed using CSS and a bit of JavaScript to allow value stored in each toggle button changed when user give a click. 
* **Deployed** this website by using **Flask API** and help of **Heroku** platform as a **server**. 

Result of the deploy website can be found [**here**](https://avionic-failure-prediction.herokuapp.com/)

## [Cargo Airlines Financial Analysis](https://github.com/adikelvianto/Aglis_Air_Cargo)
### December 2021
This is a **team project** done on my 7th semester for **"Aviation System Planning" class**, which requires each team to create an aviation business from raw and will be evaluated by experienced people on this area. In this project, we decided to create a **cargo airline** named **"Aglis"** which focuses on delivering marine products and general goods. In this project, I have a **duty as Chief Finance Officer (CFO)** that conduct several task such as:

* **Find** the **most suitable aircraft** to be used also the **number of aircrafts needed** to serve demand we have.
* Create **maintenance schedule** to determine non operating days and make sure all aircraft is airworthy.
* Calculate **cost structure** of cargo airline company consisting of direct, indirect and ownership costs.
* Conduct **profitability analysis** and **calculate** the **price** we need to give **each kilogram** of cargo for each route we served.
* **Analyze profit** earn each year, create **cash flow** for **10 years period** and calculate **Net Present Values** and **Net Profit Margin** earned.

<p align="center">
 <img width="897" alt="Cost Structure" src="https://user-images.githubusercontent.com/92104520/185748563-0ae2ef8c-3608-45f4-abae-2966ed55ed35.png">
</p>

Final presentation of this project can be found [**here**](https://github.com/adikelvianto/Aglis_Air_Cargo/blob/main/PSA%202021_Aglis_Finale.pptx).
