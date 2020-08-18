# Bank Telemarketing Prediction: Project Overview 
* Created a tool that classifies bank customers to be given telemarketing campaign
* Data used was Bank Marketing Dataset from UCI Machine Learning Repository consisted with 17 attributes and 45211 records.
* Model building algorithm used are K-Neirest Neighbour, Naive Bayes, Decision Tree, Logit, and Random forest.
* SMOTE oversampling used to handle imbalanced data
* Seaborn heatmap used to handle multicollinearity

## Code and Resources Used 
**Python Version:** 3.7  
**Packages:** pandas, sklearn, seaborn, matplotlib

## Attributes
Attributes to classify customers to be given telemarketing are following:
*	Age
*	Job
*	Marital Status
*	Education Status
*	Default (Credit ownerships) 
*	Average annual balance
*	Housing mortgage
*	Private loan
*	Contact type
*	Months of last contact 
*	Days of last contact
*	Duration of last contact
*	Ammount of contact in campaign
*	Days of contact before the last contact
* Ammount of contact in previous campaign
* Campaign outcome
* Target outcome

## Model Building 

First, I transformed the categorical variables into dummy variables. I also split the data into train and tests sets with a test size of 30%.   

I tried Decision Tree classifier with entropy approach and maximum three dept of 3. I also evaluated them using accuracy rate. I chose decision tree classifier because my goal was to build a simple model that is easy to visualize.

## Model performance
The Decision Tree model performance is presented. 
*	**Decision Tree** : Accuracy = 0.57
The performance is relatively low because the small sample size and it was imbalanced between the sample size and the ammount of the attributes.

## Decision Tree Visualization
Decision tree visualization is presented below
![alt text](https://github.com/novaldi21/ds_attrition_project/blob/master/attrition.png "Decision Tree")

From the picture, it can be seen that employees that are predicted will get attrition are employees with monthly income below $.2057.5 
