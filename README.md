# H1N1 VACCINE PREDICTION.

## Project Overview
This project Uses Logistic Regression and Decision Trees Classifiers models to make predictions of whether someone received H1N1_vaccine or not.

## BUSINESS PROBLEM.
The Ministry of Health wants to administer Covid-19 vaccines but they do not know how people will respond. The ministry revisited past data with the information of vaccination cases in late 2009 and early 2010 conducted by the United States. I have been given this data and tasked to predict whether people received H1N1 vaccines according to their backgrounds,opinions and health behaviors.

## OBJECTIVES
The main objectives are:

* To predict how likely individuals are to receive H1N1_vaccine.
* To use Logistic regression modelling to make our predictions
* To model a DecisionTree that provides us with predictions
* To evaluate the performance of our models and come up with the best model.
* Provide insight of how people would react to covid-19 vaccination.

## Data Understanding
For this project, i will be using information from datasets:

* training_set_features.csv- A dataset containing personal information of individuals who responded to the survey about h1n1_vaccination.
* training_set_labels.csv - A dataset containing the label features 0 and 1. 0 for those who received vaccines and 1 for those who didn't.

## Modelling
#### 1. Logistic Regression Modeling 
The model is an imbalanced case since it has **79%** percent of people who never received the vaccine against **21%**  people who received
*In The Modelling process I used Area Under the curve ,ROC and AUC as my evaluation metrics.
##### I made a logistic regression model and came up with the following ROC graph and Confusion Matrix after Tuning the model.

![ROC_conf](https://github.com/user-attachments/assets/6000264a-311e-4b70-9cc2-e863a9058f80)
![LR_conf](https://github.com/user-attachments/assets/7feb368b-b2f0-4125-87f8-47c51423a66d)
#### Logistic Regression Model Evaluation.
In order to end up with the best logistic regression model,
* I tuned my logistic regression model using SMOTE since it is an imbalanced case.
* Looked for the best paramaters for my model and evaluated th model using **ROC AUC** and **Precision**
After evaluating and tuning the logistic regression , 
* It had a ROC AUC score of around **83%**.
* The logistic regression model also provided a testing accuracy score of 83% and a testing precission of **67%**.
* The logistic regression has a higher precission than recall. This works better with our model since it is better to predict one as not being vaccinated while they are ,than predicting them as vaccinated while they aren't.

####2. Decision Tree Classifier Modelling.
* In the decision Tree, I used AUC ROC and Accuracy score as my evaluation metrics.
* I then tuned the model in order to find the best parameters.
 The maximum parameters for the model were:`max_features=55`, `max_depth=2`,`min_samples_split=0.25`,`min_samples_leaf=0.20`.

![DT_ROC](https://github.com/user-attachments/assets/742bd18b-a969-42ca-9e64-a6903b4bbf9e)
![DT_conf](https://github.com/user-attachments/assets/a4e41a72-7c4a-47a7-9284-eb5d02779831)
#### Decission Tree Classifier Model Evaluation
 * After evaluating and tuning the decission tree classifier, it had an ROC AUC of around **80%**
 * The Decission Tree classifier had an accuracy of about **70%**.
## LIMITATIONS.
****The major limitation about this model is that the dataset was imbalanced . Tried using `SMOTE` but it could help improve the results.****

## CONCLUSION.
From the modelling process, I made two models: `logistic regression` and a `decission tree classification` model.
****I Made the following conclusions:****
 * After evaluating and tuning the logistic regression , It had a ROC AUC score of around **83%**.
 * The logistic regression model also provided a testing accuracy score of **83%** and a testing precission of **67%**.
 * The logistic regression has a higher precission than recall.

 * After evaluating and tuning the decission tree classifier, it had an ROC AUC of around **80%**
 * The Decission Tree classifier had an accuracy of about **70%**

## RECOMMENDATION.
Of the two models, it is better to utilize the ****regression model****. The regression model has a higher accuracy score of **83%** and a precission of **67%**. 
* This precission is way better than recall.This is useful in our prediction cases. It is better to predict a person a person as having taken the vaccine than predicting a person that didn't take the vaccine as having taken the vaccine.
* This model can be used in places where one wants to introduce vaccines for the first time.
*  or where a stakeholder wants to begin distributing vaccines due to an emerged virus.









