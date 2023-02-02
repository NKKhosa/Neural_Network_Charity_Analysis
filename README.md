# Neural Network Charity Analysis

## Overview
An analysis was done on data provided by Alphabet Soup to help determine which investments are most likely to prove successful. Alphabet Soup provided a CSV with funding data from over 34,000 organizations and a deep neural learning model was created to predict the success of an application. 

## Results: 
### Data Preprocessing
#### Target
- the IS_SUCCESSFUL column was the target of this analysis to determine if the funding was used effectively.
#### Features
- APPLICATION_TYPE
- AFFILIATION
- CLASSIFICATION
- USE_CASE
- ORGANIZATION
- STATUS
- INCOME_AMOUNT
- ASK_AMT
#### Dropped
- EIN and NAME were dropped as they are simply identification columns.
- SPECIAL_CONSIDERATIONS was also dropped.

### Compiling, Training, and Evaluating the Model
#### Layers
- Layer 1:
    - 120 neurons were used because its ~3x the input features
    - Rectified Linear Unit (ReLU) activation function was used.
- Layer 2:
    - 60 neurons
    - ReLU activation function
- Layer 3:
    - 30 neurons
    - tanh activation function 
- Output Layer:
    - tanh activation function

#### Model performance
- Target model performance of >75% was not reached.
- 73% accuracy.
- 56% loss

#### Optimization
Optimization was attempted using the following means:
- The SPECIAL_CONSIDERATIONS column was dropped to try and remove a noisy variable.
- An additional hidden layer was added
- Additional nodes were added to the existing hidden layers
- And the activation functions were altered from sigmoid to tanh

However, non of these adjustments improved the accuracy or reduced the loss.

## Summary:

Overall the deep learning model was not very sucessfull in predicting the success of an application. With a max accuracay score of 73% reached, and even that with a high loss value of 56%, the benefits of this model were few. Training the model and changing various components in order to attempt optimization was also quite time-consuming. 

A RandomForest ensemble learning model may prove to be more effective at determining a more meaningful output for this problem as they operate on a similar level to deep learning models, but take significantly less time to train.
