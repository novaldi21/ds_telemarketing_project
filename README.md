# Bank Telemarketing Classification: Project Overview 
* Chose the best algorithm to classifies bank customers to be given telemarketing campaign.
* Data used was Bank Marketing Dataset from UCI Machine Learning Repository consisted with 17 attributes and 45211 records.
* Target attribute is customer acquirement status after telemarketing was given.
* Model building algorithm used were Decision Tree, K-Neirest Neighbour, Logit, Random forest, and Naive Bayes.
* Models were evaluated by looking at their precision, recall, accuracy, and F1-score. 
* SMOTE oversampling was used to handle imbalanced data.
* Seaborn heatmap was used to handle multicollinearity.

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
<br />The data can be seen [here](https://github.com/novaldi21/ds_telemarketing_project/blob/master/bank-full.csv)

## Data Pre-Processing
First, I did a missing values check for each attributes and there are large ammount of it in "contact" and "poutcome". Therefore, those attributes are eliminated.
<br />Secondly, I built a correlation heatmap for numerical attributes to check multicollinearity status in the data. Then, it can be seen that multicollinearity was not present. The figure for the heatmap is can be seen below. 
<br />![](https://github.com/novaldi21/ds_telemarketing_project/blob/master/heatmap.png)
<br />Thirdly, I compare the ammount of "yes" and "no" data in target outcome and there were imbalanced data condition because the ammount of "yes" data was 5289 and "no" data was 39922. Therefore SMOTE oversampling method was used to balance the ammount of them.
<br />Finally, I did categorical encoding for categorical data before model building. I also standardized the numerical data.

## Model Building 

First, I split the data into train and tests sets with a test size of 20%.   

I did a model building by using train and test data with these algorithm: Decision Tree, K-Neirest Neighbour, Logit, Random forest, and Naive Bayes.

I also did a validation by using cross-validation method. Finally, model performances are checked to decide which algorithm was the best.

The python code for the model building process is available [here](https://github.com/novaldi21/ds_telemarketing_project/blob/master/Telemarketing%20new.ipynb)

## Model performance
The model performances are presented. 
*	**Decision Tree** : Precision = 0.91; Recall = 0.91; Accuracy = 0.91; F1-Score = 0.91
*	**K-Nearest Neighbour** : Precision = 0.99; Recall = 0.99; Accuracy = 0.94; F1-Score = 0.94
*	**Logit** : Precision = 0.80; Recall = 0.81; Accuracy = 0.80; F1-Score = 0.80
*	**Random Forest** : Precision = 0.95; Recall = 0.94; Accuracy = 0.95; F1-Score = 0.95
*	**Naive Bayes** : Precision = 0.83; Recall = 0.63; Accuracy = 0.75; F1-Score = 0.71
<br />Based on the model performances, the best algorithm to be used was 	**Random Forest** since it has the best performance in F1-Score

## Model Evaluation
I did model evaluation by doing cross-validation between train and test data. The results shown that the range for accuracy differences between validation was **+/-0.01**
<br />Based on that number, it was concluded that the model produced was valid.

