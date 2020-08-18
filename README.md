# Bank Telemarketing Prediction: Project Overview 
* Created a tool that classifies bank customers to be given telemarketing campaign.
* Data used was Bank Marketing Dataset from UCI Machine Learning Repository consisted with 17 attributes and 45211 records.
* Target attribute is customer acquirement status after telemarketing was given.
* Model building algorithm used were Decision Tree, K-Neirest Neighbour, Logit, Random forest, and Naive Bayes.
* Model evaluated by looking at precision, recall, accuracy, and F1-score. 
* SMOTE oversampling used to handle imbalanced data.
* Seaborn heatmap used to handle multicollinearity.

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
* Target outcome (Customer Acquired)

## Data Pre-Processing
First, I did a checking of missing values for each attributes and there are large ammount of it in "contact" and "poutcome". Therefore, those attributes are eliminated.
<br />Secondly, I built a correlation heatmap to check availability of multicollinearity in the data. Then, it can be seen that multicollinearity was not present. The figure for the heatmap can be seen below. 
<br />![](https://github.com/novaldi21/ds_telemarketing_project/blob/master/heatmap.png)
<br />Thirdly, I compare the ammount of "yes" and "no" data in target outcome and there were imbalanced data condition because the ammount of "yes" data was 5289 and "no" data was 39922. Therefore SMOTE oversampling method was used to balance the ammount of them.
<br />Finally, I did categorical encoding for categorical data before model building. I also standardized the numerical data.

## Model Building 

First, I split the data into train and tests sets with a test size of 20%.   

I did a model building by using train and test data with these algorithm: Decision Tree, K-Neirest Neighbour, Logit, Random forest, and Naive Bayes.

I also did a validation by using cross-validation method. Finally, model performances are checked to decide which algorithm was the best.

## Model performance
The model performances are presented. 
*	**Decision Tree** : Accuracy = 0.57
*	**K-Nearest Neighbour** : Accuracy = 0.57
*	**Logit** : Accuracy = 0.57
*	**Random Forest** : Accuracy = 0.57
*	**Naive Bayes** : Accuracy = 0.57
