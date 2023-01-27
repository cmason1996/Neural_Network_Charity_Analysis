# Neural_Network_Charity_Analysis

## Overview

The purpose of this analysis was to take past data from Alphabet Soup's donating history and use it to train a neural network learning model that would then be used to predict whether future investments by the charity would be good financial moves. To accomplish this task that data was preprocessed and then fit to several different iteration of a neural network for the best fit to the data

### Tools Used

* Tensorflow version 2.11.0
* Jupyter Notebook version 6.4.12
* Python version 3.7.13
* Data Used: charity_data.csv

<img width="413" alt="original_network" src="https://user-images.githubusercontent.com/112291888/215143950-87f1f3f3-00fd-43e3-aca4-8af92f2d55d0.png">

## Results

### Data Processing

<a href="https://github.com/cmason1996/Neural_Network_Charity_Analysis/blob/main/AlphabetSoupCharity.ipynb" target="_blank">Click here to view neural network code</a>

* For this analysis we were interested in whether a company would be successful in receiving an investment from Alphabet Soup; therefore our target variable would be the 'IS_SECCESSFUL' column. To do this the values in the column were set equal to 'y'.

* The features of this analysis are all of the other columns in the dataset that can be used to predict whether a company would be successful in receiving an investment from Alphabet Soup. These columns were set equal to 'X'. 

* Variables that are neither targets or features are columns such as 'EIN', and 'NAME' and they were removed before the preprocessing of the data continued. This was done to remove any variales that would skew that data but not give any real value to the fitting of the neural network. 

### Compiling, Training, and Evaluating the Model

<a href="https://github.com/cmason1996/Neural_Network_Charity_Analysis/blob/main/AlphabetSoupCharity_Optimization.ipynb" target="_blank">Click here to view neural network code after optimization</a>

* For the optimization of the model. one of the steps taken was to increase the number of hidden layers in the model from 2 layers to 3. The first layer had 8 neurons, the second layer had 5 neurons, and the third layer had 3 neurons. All three of these layers used the 'relu' activation function. The reason to increase the number of layers was an attempt to increase the accruacy of the model by increasing that layers in which data is processed. Using the 'relu' activation function was done because it allows for an infinite number of positive variables which allows for a greater accuracy in processing data. 

* During the optimization of the model the target accuracy of 75% was not reached. The closest our accuracy got to the target was 64.9% accuracy. While this did not reach the target, it was a marked improvement over the initial accuracy of the model at 52.54%.

* THe steps taken to increase the accuracy of the model were to increase the number of epochs the model trained for, change the activation function from 'relu' to 'tanh', increase the number of hidden layers, drop additional columns of clouding data from the training and test data, and decreasing the number of hidden layers to 1 with 8 neurons. While all of these steps were effective in increasing the accuracy of the model, none of them were able to increase the accuracy to the target level.

## Summary

Overall, the nerual network was able to process the data to some regree of accuracy after several iterations. However, given that this model will be used to predict financial decisions, a higher degree of accuracy would be recommended before instituting and relying on the model in the long term. 

### Recommendations

Going forward, it is recommended to continue the iterations of the model until a higher degree of accuracy is achieved. One of our recommendations would be to try processing the data with both a nerual network and a Linear Regression model and comparing the two results. The reason we would recommend a Lineral Regression model is that is excells at fitting data and returing either a yes or no prediction which is the entire goal of this analysis. 