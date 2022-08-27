# Neural_Network_Charity_Analysis

## Analysis Overview

The purpose of this analysis was to use neural networks to help the foundation Alphabet Soup predict where to make its investments.

Using our knowledge of machine learning and neural networks, we used the features in the provided dataset to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

We received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization and the goal is to use the data appropriately to create an accurate model for predicting the success of future applicants. 

The assignment consisted of three technical analysis deliverables and a written report:

* Deliverable 1: Preprocessing Data for a Neural Network Model
* Deliverable 2: Compile, Train, and Evaluate the Model
* Deliverable 3: Optimize the Model
* Deliverable 4: A Written Report on the Neural Network Model (README.md)

- - - - 

## Results: Using bulleted lists and images to support your answers, address the following questions.

### Data Preprocessing

#### Which variable(s) are considered the target(s) for your model?

The column IS_SUCCESSFUL is the target for our model. It contains binary data (ie: Y/N) to show if the charity donation was successful.

#### Which variable(s) are considered to be the features for your model?

The remaining columns, minus the columns we dropped (see next question) are considered the features for our model: 

* APPLICATION_TYPE—Alphabet Soup application type
* AFFILIATION—Affiliated sector of industry
* CLASSIFICATION—Government organization classification
* USE_CASE—Use case for funding
* ORGANIZATION—Organization type
* STATUS—Active status
* INCOME_AMT—Income classification
* SPECIAL_CONSIDERATIONS—Special consideration for application
* ASK_AMT—Funding amount requested

#### Which variable(s) are neither targets nor features, and should be removed from the input data?

We should remove the EIN and NAME columns from our input data, as they will not support the accuracy of the model.

### Compiling, Training, and Evaluating the Model

#### How many neurons, layers, and activation functions did you select for your neural network model, and why?

For the original model I created, I chose 2 layers using the ReLu activation function and used the Sigmoid activation function with the output layer. The first layer had 80 neurons and the second layer had 30 neurons. I chose that number of neurons and layers based on the size of the csv being quite a bit larger than other CSVs we’ve been working with in this module. 

#### Were you able to achieve the target model performance?

I was not able to achieve the target model performance (75%) in 4 attempts at creating/adjusting my model. The best I could achieve was 66% when I completed Deliverable 2, before creating the new JN to optimize the model.

#### What steps did you take to try and increase model performance?

To try and increase the model’s performance I did the following:

* Attempt 1: Added an additional layers and increased the neurons for each layer
* Attempt 2: Changed the activation function for the layers from Sigmoid to Tanh
* Attempt 3: Increased the number of epochs used in the training regimen
* Attempt 4: Decreased the number of neurons used in the hidden layers

- - - - 

## Summary + Recommendation: 

#### Summary of the overall results of the deep learning model:

Overall, I would not recommend using the initial model I created, or any of the subsequent models that were based on the original model, as their accuracy only declined from the height of 66%. We may need to spend more time eliminating outliers from the data or dropping unnecessarily columns to see if the model improves, which can be time consuming.

#### Recommendation for how a different model could solve this classification problem, and why:

This data set deals with a large number of entries (rows) but not a large number of columns (features) and we are trying to predict outcomes based on a binary classification. As such, I would recommend using a supervised machine learning model, such as Ensemble’s Random Forest Classifier. It might take more time, but it would likely have a higher accuracy. 
