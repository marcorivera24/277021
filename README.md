# Social Media Shares

Team Members:
1) Yaseen Abdulmahdi (277021)
2) Mehrab Teimourpour (273741)
3) Don Mark Tolod (276181)  


**INTRODUCTION**

In this project, we are tasked with helping a social media department analyze the success of their communications. Specifically, we aim to develop a tool that can predict the number of shares on social media given the contents and supposed publication time. To do so, we have been provided with a dataset to use for machine learning.

  

**METHODS**

We have used three models for this project: a Neural Network Regression model implemented in Keras, an XGboost Regression model, and a Random Forest Regressor. For each model, we have performed the following steps:

  

1) Conducted an Explanatory Data Analysis (EDA) with visualization to get a better understanding of the data and identify any potential issues.

2) Generated a training and test set. The test set was only used at the end to evaluate the final model.

3) Pre-processed the dataset by removing outliers and encoding categorical features with one hot encoding.

4) Created a validation set from the training set to analyze the behavior of the model with the default hyperparameters. We then used 10-fold cross-validation to find the best set of hyperparameters for each model.

5) Selected the best architecture for each model using the appropriate metric.

6) Finally, we computed the performances of the test set for each model.

***We used Random Search for hyperparameter tuning in our models.***

  

After selecting the best model, we dropped variables that did not improve the accuracy of the model using Linear Regression and a p-threshold value.

  

**Experimental Design**

For each model, we conducted experiments to demonstrate and validate the effectiveness of our approach. We evaluated each model using the following metrics: Mean Squared Error (MSE), Mean Absolute Error (MAE), and R2 score.

  

**Results**

Before dropping variables, the scores for each model were as follows:

  


| Model Used               | R2    |
|--------------------------|-------|
| Neural Network Regressor | 0.03  |
| Random Forest Regressor  | -0.27 |
| XGboost Regressor        | -0.53 |

After dropping variables and using Linear Regression, the scores for each model improved as follows:

  


| Model Used               | R2   |
|--------------------------|------|
| Neural Network Regressor | 0.07 |
| Random Forest Regressor  | 0.05 |
| XGboost Regressor        | 0.08 |

Overall, the XGboost Regressor performed the best among the three models.

  

**Conclusions**

The main take-away from this project is that the XGboost Regressor was able to achieve the best prediction performance for the number of shares on social media. However, the overall performance of all three models was not particularly strong, with relatively low R2 scores. This suggests that there may be other important factors that we have not considered in our analysis.

There are several potential next steps for future work in this direction. One possibility is to explore different feature engineering techniques or consider additional data sources to improve the predictive power of our models. Another possibility is to try different machine learning algorithms to see if they may be more effective at predicting the number of shares.
