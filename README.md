# deep-learning-challenge

## Overview of the Analysis

In this challenge, the goal is to use machine learning and neural networks to help the a foundation with a tool to select applicants for funding with the best chance of success in their ventures.

The steps used to complete this challenge are as follows: 

<b>1. Preprocessing the Data:</b>
*  Read in the dataset
*  Drop the EIN and NAME columns
*  Determine unique values for each column
*  For columns with more than 10 unique values, choose a cut off point and combine "rare" values into an 'Other' category
*  Use pd.get_dummies() to encode variables
*  Split the data into test and training datasets using the train_test_split module from sklearn
*  Scale the data


<b>2. Compile, train, and evaluate the model</b>
*  Create a neural network with at least 1 hidden layer
*  Create an output later with the appropriate activation function
*  Check the structure of the model
*  Compile and train the model
*  Create a callback that saves the model's weights every five epochs (this is the model_weights.h5 document)
*  Evaluate the model using the test data to determine the loss and accuracy
*  Save and export results (this is the AlphabetSoupCharity.h5 file)


<b>3. Optimize the model to achieve a target predictive accurary higher than 75%</b>
*  Adjust the input data to ensure no variables or outliers are causing confusion in the model
*  Bring back the 'NAME' column and replace values with less than 150 occurences into the 'Other' category
*  Adding an additional hidden layer
*  Reducing epochs from 100 to 50
*  Once all the steps above were completed, target predictive accurary rose to just over 75%


## Results

<b>Data Preprocessing</b>
The target variable in this model was the 'IS_SUCCESSFUL' variable. All other columns are the feature variables with the exception of the 'EIN' and 'NAME' variables in the original model, and just the 'EIN' variable in the optimized version.

<b>Compiling, Training, and Evaluating the model</b>
The final optimized moel consists of 5 layers, as such: 
* First layer has 10 neurons with the relu activation function
* The second layer has 15 neurons with a sigmoid activation function
* The third layer has 10 neurons with a sigmoid activation function
* The fourth layer has 10 neurons with a relu activation function
* The output layer has 1 neuron with a sigmoid activation function

With the layers described above, I was able to achieve the target model performance. For full transperency, I did make approximately 10 changes and alterations before deciding on this final combination of layers and binning of the 'NAME' column. Most of my earlier optimization models were coming in around 73-74% and I was determined to reach the target performance. I unfortunately did not save these other models but I had tried combinations of adding a fourth and then fifth hidden layer, changing the amount of neurons per each layer, changing the activation functions, adding the 'NAME' column back and binning it, and reducing epochs before I achieved my desired result. 

## Summary

I did reach the target model performance but I would also recommend exploring other options such as a random forest model. Further tweaking could also be done to this current model to achieve better performance as well.
