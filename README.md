# Predict-Loan-Repayment
supervised classification model


### Process

## Step 1: Data Preparation

tep 1: Data Preparation
How did you prepare the dataset? What errors did you have to handle
The data preparation steps carried out on the loan prediction dataset are as follows:
1. Dealing with missing values:
Out of the 122 columns available to work with, 67 columns contained missing values. A script was written to calculate the count of missing values per columns. Hence, columns with more than 100,000 missing values (49 columns) were dropped. Missing values in other columns with minimal amount of missing values was filled with the median.

2. Encoding:
In the dataset there are a number of categorical features. These features were encoded into a useable format using LabelEcncoder

3. Feature Engineering:
Feature engineering was also carried out to obtain features that will impact the model. Variance threshold was used to obtain features with zero variance (of which there was none). Pearson's correlation coefficient was then used to obtained correlated features, of which 9 of them were dropped.


4. Standardization:
The dataset was then normalized using MinMaxScaler to make it fir for modelling

5. Dealing with imbalanced data
An oversampling technique was carried out on the target feature using SMOTE so as to deal with the problem of imbalanced dataset.


## Step 2: Model

What model(s) did you decide to build? Why did you chose it/them? 
Two Machine Learning algorithms were used to train the model. The first algorithm is Catboost.

### Step 3: Evaluation

How does your model perform? Can you trust this model?
The algorithm had an ROC curve score of 0.954 on the training set, while the second algorithm used was RandomForest with an ROC curve score of 0.9575 on the training set. The the RandomForest performed better and the prediction on the testing set was saved in Final Submission



## About this project

Loan-Prediction-Project
Many people struggle to get loans due to insufficient or non-existent credit histories. And, unfortunately, this population is often taken advantage of by untrustworthy lenders.

Home Credit strives to broaden financial inclusion for the unbanked population by providing a positive and safe borrowing experience. In order to make sure this underserved population has a positive loan experience, Home Credit makes use of a variety of alternative data--including telco and transactional information--to predict their clients' repayment abilities.

In this project, a machine learning predictive model was built to help Home Credit unlock the full potential of their data. This will ensure that clients capable of repayment are not rejected and that loans are given with a principal, maturity, and repayment calendar that will empower their clients to be successful.


## Outcomes

From the result of the predictive model, it can be inferred most of the customers in context will not receive a loan based on their historical data, as about 75% of the population had a prediction probability close to zero. 



