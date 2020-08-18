# Bank Telemarketing Prediction: Project Overview 
* Created a tool that classifies bank customers to be given telemarketing campaign
* Data used was Bank Marketing Dataset from UCI Machine Learning Repository consisted with 17 attributes and 45211 records.
* Target attribute is customer acquirement status after telemarketing was given.
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
* Target outcome (Customer Acquired)

## Data Pre-Processing
First, I did a checking of missing values for each attributes and there are large ammount of it in "contact" and "poutcome". Therefore, those attributes are eliminated.
<br />Secondly, I built a correlation heatmap to check availability of multicollinearity in the data. Then, it can be seen that multicollinearity was not present. The figure for the heatmap can be seen below. 
![](https://github.com/novaldi21/ds_telemarketing_project/blob/master/heatmap.png)
<br />Thirdly, I compare the ammount of "yes" and "no" data in target outcome and there were imbalanced data condition because the ammount of "yes" data was 5289 and "no" data was 39922. Therefore SMOTE oversampling method was used to balance the ammount of them.
<br />Finally, I did categorical encoding for categorical data before model building. I also standardized the numerical data.

## Model Building 

First, I transformed the categorical variables into dummy variables. I also split the data into train and tests sets with a test size of 30%.   

I tried Decision Tree classifier with entropy approach and maximum three dept of 3. I also evaluated them using accuracy rate. I chose decision tree classifier because my goal was to build a simple model that is easy to visualize.

## Model performance
The Decision Tree model performance is presented. 
*	**Decision Tree** : Accuracy = 0.57



