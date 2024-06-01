# deep-learning-challenge

## Overview of the Analysis

In this challenge, the goal is to use machine learning and neural networks to help the a foundation with a tool to select applicants for funding with the best chance of success in their ventures.

The steps used to complete this challenge are as follows: 
1. Preprocessing the Data:
*  Read in the dataset
*  Drop the EIN and NAME columns
*  Determine unique values for each column
*  For columns with more than 10 unique values, choose a cut off point and combine "rare" values into an 'Other' category
*  Use pd.get_dummies() to encode variables
*  Split the data into test and training datasets using the train_test_split module from sklearn
*  Scale the data


2. Compile, train, and evaluate the model
*  Create a neural network with at least 1 hidden layer
*  Create an output later with the appropriate activation function
*  Check the structure of the model
*  Compile and train the model
*  Create a callback that saves the model's weights every five epochs (this is the model_weights.h5 document)
*  Evaluate the model using the test data to determine the loss and accuracy
*  Save and export results (this is the AlphabetSoupCharity.h5 file)


3. Optimize the model to achieve a target predictive accurary higher than 75%
*  Adjust the input data to ensure no variables or outliers are causing confusion in the model
*  Bring back the 'NAME' column and replace values with less than 150 occurences into the 'Other' category
*  Adding an additional hidden layer
*  Reducing epochs from 100 to 50
*  Once all the steps above were completed, target predictive accurary rose to just over 75%


## Results

The target variable in this model was the 'IS_SUCCESSFUL' variable.

## Summary

Given the 99% accuracy rate, I would recommend that the logistic regression model is used. When reviewing the healthy loan label predictors, both precision and recall are extremely high at 100% and 99% respectively. It would not be a fair recommendation without calling attention to the slight decrease in accuracy when it comes to the high-risk loan labels. The accuracy is slightly lower, coming in at 85% and 91%. In business, being able to correctly predict the high-risk loans is paramount. However, even though these are less accurate than the healthy loan label predictors, I find that these numbers are still acceptable and would move forward with recommending the model. 
