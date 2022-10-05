# Traffic-Sign-Classifier
This is multi-class classification project performed on the German Traffic Sign Benchmark Data to classify traffic signs into 43 classes.

## Introduction
With the advent of technology in the automobile sector, self-driving cars have become a reality for humankind. Autonomous capability can be attained once these vehicles follow traffic rules. So to achieve accuracy in this technology, these vehicles understand the traffic signs like human drivers. There are several different types of traffic signs like speed limits, no entry, traffic signals, turn left or right, children crossing, no passing of heavy vehicles, etc. Traffic signs classification is the process of identifying which class a traffic sign belongs to.

## About the Project
In this Python project, a deep neural network model is build, which can classify traffic signs present in the image into different categories. With this model, we are able to read and understand traffic signs which are a very important task for all autonomous vehicles. Finally, a GUI is made using Tkinter to make predictions.

## Dataset Details
The dataset contains more than 50,000 images of different traffic signs. It is further classified into 43 different classes. The dataset is quite varying, some of the classes have many images while some classes have few images. The size of the dataset is around 300 MB. The dataset has a train folder which contains images inside each class and a test folder which we will use for testing our model.

Link:- https://www.kaggle.com/datasets/meowmeowmeowmeowmeow/gtsrb-german-traffic-sign?datasetId=82373&sortBy=voteCount 

## Pre-requisites
* tensorflow
* keras
* sklearn
* matplotlib
* seaborn
* pandas
* numpy
* pil

## Data Preparation
Image data files from respective directories are resized to 30 x 30 px and stored in a list(data) along with the corresponding labels. After which both the lists are converted into numpy arrays. The data stored in these arrays in then split into X_train, X_test and y_test, y_train in the ratio 80:20 where 80% data is used for training while the 20% data is used for testing purpose. X is the independent variable and y is the dependent variable here.

## Model Building
To classify, a custom CNN(Convolutional Neural Network) is built, which is best for the purposes of image classification. 

We compile the model with Adam optimizer which performs well and loss is “categorical_crossentropy” because we have multiple classes to categorise.
After building the model architecture, we then train the model using model.fit(). I tried with batch size 32 and 64. Our model performed better with 64 batch size. And after 30 epochs the accuracy was stable.

## Model Plot
![image](https://user-images.githubusercontent.com/106440078/194110397-84f1a9bd-9d31-4893-8184-1b95a9bb4f81.png)

## Accuracy Curve
![image](https://user-images.githubusercontent.com/106440078/194111396-37f77a43-e790-464e-bdae-2df7ed3d7959.png)

## Loss Curve
![image](https://user-images.githubusercontent.com/106440078/194111414-6bafd6ac-300c-44aa-a60b-4dc82be404f7.png)

## Predictions
![image](https://user-images.githubusercontent.com/106440078/194110699-80241cdc-1e8f-4163-9ec6-3cde816c218f.png)

## Classification Report
![image](https://user-images.githubusercontent.com/106440078/194110891-83af0fcc-19ab-4004-9e1c-a61f253db3b8.png)

## Validation Results
![image](https://user-images.githubusercontent.com/106440078/194111283-10ecb011-3cff-4a0a-ab14-a0d5a4b9f67d.png)

## Testing Results
![image](https://user-images.githubusercontent.com/106440078/194111046-f3dfa947-31e5-4f3c-aca0-12988a14a9a6.png)

## Tkinter APP Interface
![image](https://user-images.githubusercontent.com/106440078/194128811-6cd2addf-5639-4546-ba45-d96f5ef6350c.png)

