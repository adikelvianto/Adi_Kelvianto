# My Portfolio

## [Analysis of Divvy Company Dataset in 2021 using R](https://www.kaggle.com/code/adikelvianto29/analysis-of-divvy-2021-dataset-using-r)
### October 2022

This is a case study in which I positioned myself as a **junior data analyst** on the **marketing analytics team** at **Cyclistic (Divvy)**. My **responsibility** was to extract **insights from historical data** and **develop new marketing strategies**, with the goal of converting casual riders into annual members. All work was conducted **using the R programming language**, and the details are as follows:

* Defined the **business problem** to be solved.
* **Gathered, ensured the credibility of, and cleaned** the historical data from Divvy company. (**January - December 2021**)
* Created **custom metrics** and **analyzed** the statistical summary of the dataset.
* Conducted **analysis** based on **several metrics** to understand the **differences** between **casual** and **member** riders.
* **Provided four recommendations** to the company regarding their marketing strategy in order to **convert casual riders into annual members based on the insights derived from the data**.

![image](https://user-images.githubusercontent.com/92104520/198869067-995e6c60-9c41-4e18-ba55-cab457f09cbd.png)


## [Development of Auto Landing Deep Learning Model for Boeing 747 Aircraft](https://github.com/adikelvianto/Auto_Landing_DL)
### October 2022
This project aims to create an **auto-landing deep learning model** using TensorFlow by utilizing **"Flight Data Recorder"** data. 
* Preprocessed **Flight Data Recorder (FDR)** data, which consisted of a total of **20GB CSV files**; **split** the dataset for training, validation, and testing.
* Conducted Exploratory Data Analysis and built **an elevator model** and **a throttle model** using **TensorFlow** and **KerasTuner** to conduct hyperparameter tuning.
* The next stage of development for this project is to **deploy** it to **MATLAB/Simulink and X-Plane** to see whether these models can perform their job as an auto-landing control system.

Here are some **comparisons** between **model prediction** values and **actual values**, for **both** the elevator and throttle models.

<p align="center">
<img width="1307" alt="Elevator Comparison" src="https://user-images.githubusercontent.com/92104520/196446972-d92fe034-d835-4562-9993-a1ab18730c35.png">
</p>
<hr>

<p align="center">
<img width="897" alt="PLA Comparison" src="https://user-images.githubusercontent.com/92104520/196449142-dda478d9-03d1-4ad6-8ee5-dfe12e6aea59.png">
</p>


## [Deep Learning Based Fly-Over Waypoints Control System for Business Jet Aircraft](https://github.com/adikelvianto/Fly-Over_Waypoints_ANN)
### September 2022
This is my undergradute thesis project, with the goals are to **develop fly over waypoints controller system using deep learning method** espescially for **Cirrus Vision SF50** aircraft and **study the relationship between training data** that categorized by aircraft roll angle during the mission. This study give results that deep learning model generally increase closeness of the aircraft to the waypoint compared to the PID method, eventhough the dataset used is a piece of sliced data. It also shown that **wider datasets didn’t guarantee superior results** due to generalizations that model try to made.

What I've done on this project are:
* **Set up communication environment** between **X-Plane** and **MATLAB/Simulink**.
* **Tuned PID controller** that allow Cirrus Vision SF-50 accomplish flight mission with least of oscillation or swaying movement. 
* **Created** 10 **flights mission** data through **simulation** with various forms of mission flight path and split each section of waypoint leg based on roll angle range resulting into **4 characterized train datasets**.
* Preprocessed, Cleaned, and did Exploratory Data Analysis to **select features** for the **joystick model**.
* **Develop** 4 **TensorFlow model** from 4 different datasets and did hyperparameter tuning using **Bayesian Method** that provided by **KerasTuner**. 
* **Converted TensorFlow model** so that it can **be used in Simulink** and **validate** each model performance in **X-Plane**. 
* **Analyzed** effects between **train dataset** and deep learning-based controller **model performance**. 

<p> This video shown below, show how aircraft being controlled to follow the waypoint based on 1 of 4 deep learning model created.</p>

![Alt Text](https://media.giphy.com/media/pdYsJhp7pwwi3Wwjj1/giphy.gif)
![Alt Text](https://media.giphy.com/media/NSXSOpGxszAzsfRpfU/giphy.gif)

## [Neural Style Transfer using AdaIn Method](https://github.com/Artjuna/artjuna-monorepo/tree/main/model/style_transfer)
### June 2022
This is my **capstone project** at **Bangkit Academy 2022** that awarded as **top 53** capstone team **semifinalist** out of 433 teams. My job as machine learning cohort was to create Neural Style Transfer (NST) model using AdaIn Method by utilizing TensorFlow 2.x. **Neural style transfer** is an optimization technique used to **blend two images** become one image, where the reconstructed image will **preserve the object from content image**, while **transfering style** such as brushstroke from style image.

Image dataset that I used contain of **"PASCAL VOC"** dataset and validation set of **"COCO-2017"** as content image (arround **14k** images) and style image dataset consisting **"Best Artwork of All Time"** and **"Wikiart"** dataset (arround **13k** images) 

What I've done on this project are: 
* **Processed** arround **27k images** to have size of 224x224, **convert** it to **tfrecords** format to enable **parallelization training**, and **split the dataset** into train, validation and test dataset. 
* Created style transfer model using **AdaIn** method, which consist of **encoder** model that based on sliced **VGG-19** pretrained model, **decoder** that basically inverse of the encoder model also AdaIn function to allign statistical features of content image and style image. 
* **Trained model** with those image datasets for 500 epochs and analyze the reconstructed image every 10 epochs to see performance of NST model. 

<p>This is an example of image reconstruced based on model that I built.</p>
<p align="center">
 <img width="897" alt="Example Result" src="https://user-images.githubusercontent.com/92104520/185745237-39e97e3d-624e-4e4d-ba90-442dea43182a.png">
</p>

## [Prototype Webiste based Application for Avionic Components Failure Prediction](https://github.com/adikelvianto/Avionic-Components-Failure-Prediction)
### December 2021
This is my **internship** project at **PT. GMF Aeroasia Tbk**. for about **4 months**. In this project, I created a **prototype website** to give **failure prediction** of VHF Omnidirectional Range (VOR) and Multimode Control Panel components, by using **scikit-learn** library, **HTML, CSS and Flask.**

What I've done on this project are: 
* Collected information regarding maintenance from "Internal Component Refurbishment" documents both for VOR component (19 sub test) and Multimode Control Panel component (23 sub test) to **create 2 datasets**.
* **Split dataset** into train, validation and test dataset and did "**Nested Cross Validation**" method to get **best hyperparameter** for each machine learning algorithm used (Decision Tree, Random Forest, Gradient Boosting, Gaussian Naive Bayes, KNN, MLP).
* **Picked 3** best perform algorithm for both component that give **best accuracy** on test set **to be deployed** on website. 
* Created structure of the website using HTML with total of **5 pages**, designed using CSS and a bit of JavaScript to allow value stored in each toggle button changed when user give a click. 
* **Deployed** the website by using **Flask API** and help of **Heroku** platform as a **server**. 

Result of the deploy website can be found [**here**](https://avionic-failure-prediction.herokuapp.com/)

## [Cargo Airlines Financial Analysis](https://github.com/adikelvianto/Aglis_Air_Cargo)
### December 2021
This is a **team project** done on my 7th semester for **"Aviation System Planning" class**, which requires each team to create an aviation business from raw and will be evaluated by experienced people on this area. In this project, we decided to create a **cargo airline** named **"Aglis"** which focuses on delivering marine products and general goods. In this project, I have a **duty as Chief Finance Officer (CFO)** that conduct several task such as:

* **Found** the **most suitable aircraft** to be used also the **number of aircrafts needed** to serve the cargo demmand.
* Created **maintenance schedule** to determine non operating days and make sure all aircraft is airworthy.
* Calculated **cost structure** of cargo airline company consisting of direct, indirect and ownership costs.
* Conducted **profitability analysis** and **calculated price** per kilogram for each route we served.
* **Analyzed profit** earn each year, created **cash flow** for **10 years period** and calculated **Net Present Values** and **Net Profit Margin** earned.

<p align="center">
 <img width="897" alt="Cost Structure" src="https://user-images.githubusercontent.com/92104520/185748563-0ae2ef8c-3608-45f4-abae-2966ed55ed35.png">
</p>

Final presentation of this project can be found [**here**](https://github.com/adikelvianto/Aglis_Air_Cargo/blob/main/PSA%202021_Aglis_Finale.pptx).
