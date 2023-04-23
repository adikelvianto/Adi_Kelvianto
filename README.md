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
The stages carried out in this project include:
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
This is my undergraduate thesis project, which aims to **develop a fly-over waypoint controller system using deep learning methods**, particularly for the Cirrus Vision SF50 aircraft. Additionally, I am **studying the relationship** between training data and their categorization by the aircraft's roll angle during the mission. This study yielded results showing that the **deep learning model generally improves the aircraft's closeness to the waypoint compared to the PID method, even when using a sliced dataset**. It was also shown that **wider datasets do not guarantee superior results** due to generalizations that the model attempts to make.

The tasks completed in this project are as follows:

* Setting up a **communication** environment between **X-Plane** and **MATLAB/Simulink**.
* **Tuning the PID controller** to enable the Cirrus Vision SF-50 to complete flight missions with minimal oscillation or swaying movement.
* **Creating 10 flight mission data sets through simulation**, with various forms of mission flight paths, and **splitting** each section of the waypoint leg based on the roll angle range, resulting in **four characterized train datasets**.
* **Preprocessing, cleaning, and conducting exploratory data analysis** to select features for the joystick model.
* **Developing four TensorFlow models from four different datasets** and conducting **hyperparameter tuning** using the **Bayesian method** provided by KerasTuner.
* Converting the TensorFlow models so that they can be used in Simulink and validating each model's performance in X-Plane.
* **Analyzing the effects between the train dataset and the deep learning-based controller model performance.**

<p>The video below demonstrates how the aircraft is controlled to follow the waypoint using one of the four deep learning models that were created.</p>

![Alt Text](https://media.giphy.com/media/pdYsJhp7pwwi3Wwjj1/giphy.gif)
![Alt Text](https://media.giphy.com/media/NSXSOpGxszAzsfRpfU/giphy.gif)

## [Neural Style Transfer using AdaIn Method](https://github.com/Artjuna/artjuna-monorepo/tree/main/model/style_transfer)
### June 2022
This is my **capstone project** at **Bangkit Academy 2022**, which was awarded as one of the **top 53** capstone teams in the semifinals out of 433 teams. As part of the machine learning cohort, my task was to create a Neural Style Transfer (NST) model using the AdaIn method by utilizing TensorFlow 2.x. **Neural style transfer** is an optimization technique used to **blend two images** into one image, where the reconstructed image preserves the object from the content image while transferring the style, such as brushstroke, from the style image.

The image dataset I used contains the **"PASCAL VOC"** dataset and a validation set of **"COCO-2017"** as the content image (around **14k** images) and the style image dataset consisting of the **"Best Artwork of All Time"** and **"Wikiart"** datasets (around **13k** images).

What I've done on this project:
* **Processed** around **27k images** to have a size of 224x224, **converted** them to **tfrecords** format to enable **parallelized training**, and **split the dataset** into the train, validation, and test dataset.
* Created a style transfer model using the **AdaIn** method, which consists of an **encoder** model based on sliced **VGG-19** pretrained model, a **decoder** that is essentially the inverse of the encoder model, and an AdaIn function to align statistical features of the content image and style image.
* **Trained the model** with the image datasets for 500 epochs and analyzed the reconstructed image every 10 epochs to observe the performance of the NST model.

</p>This is an example of an image reconstructed based on the model I built.</p>
<p align="center">
 <img width="897" alt="Example Result" src="https://user-images.githubusercontent.com/92104520/185745237-39e97e3d-624e-4e4d-ba90-442dea43182a.png">
</p>

## [Prototype Webiste based Application for Avionic Components Failure Prediction](https://github.com/adikelvianto/Avionic-Components-Failure-Prediction)
### December 2021
This is my **internship** project at **PT. GMF Aeroasia Tbk** for about **4 months**. In this project, I created a **prototype website** to provide **failure prediction** of VHF Omnidirectional Range (VOR) and Multimode Control Panel components using **scikit-learn** library, **HTML, CSS, and Flask**.

What I did in this project are:
* Collected maintenance information from "Internal Component Refurbishment" documents for VOR (19 sub-tests) and Multimode Control Panel components (23 sub-tests) to **create 2 datasets**.
* **Split the datasets** into train, validation, and test datasets and used "**Nested Cross-Validation**" method to get the **best hyperparameters** for each machine learning algorithm used (Decision Tree, Random Forest, Gradient Boosting, Gaussian Naive Bayes, KNN, and MLP).
* **Selected 3** best performing algorithms for both components that gave **the highest accuracy** on the test set to be deployed on the website. 
* Created a website structure using HTML with a total of **5 pages**, designed using CSS, and implemented JavaScript to allow the values stored in each toggle button to be changed when users clicked on them. 
* **Deployed** the website using **Flask API** and **Heroku** platform as a **server**.

The deployed website can be found [**here**](https://avionic-failure-prediction.herokuapp.com/)

## [Cargo Airlines Financial Analysis](https://github.com/adikelvianto/Aglis_Air_Cargo)
### December 2021
This is a **team project** that I completed during my 7th semester at Institut Teknologi Bandung for the **"Aviation System Planning" class**. The assignment required us to create an aviation business from scratch and have it evaluated by experienced professionals in the field. Our team decided to establish a **cargo airline company** named **"Aglis"** that specializes in delivering marine products and general goods. As the **Chief Finance Officer (CFO)**, I was responsible for several tasks, including:

* Finding the **most suitable aircraft** and determining the **required number of aircrafts** to meet the cargo demand.
* Developing a **maintenance schedule** to identify non-operating days and ensure all aircrafts are airworthy.
* Calculating the **cost structure** of the cargo airline company, which includes direct, indirect, and ownership costs.
* Conducting a **profitability analysis** and calculating the **price per kilogram** for each route we served.
* Analyzing the profit earned each year, creating a **10-year cash flow**, and calculating the **Net Present Values (NPV)** and **Net Profit Margin (NPM)** earned.

<p align="center">
 <img width="897" alt="Cost Structure" src="https://user-images.githubusercontent.com/92104520/185748563-0ae2ef8c-3608-45f4-abae-2966ed55ed35.png">
</p>

Final presentation of this project can be found [**here**](https://github.com/adikelvianto/Aglis_Air_Cargo/blob/main/PSA%202021_Aglis_Finale.pptx).
