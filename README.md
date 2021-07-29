# Credit Card Fraud Detection:
## Data Description-
The dataset contains transactions made by credit cards in September 2013 by European cardholders.
This dataset presents transactions that occurred in two days, where we have 492 frauds out of 284,807 transactions. The dataset is highly unbalanced, the positive class (frauds) account for 0.172% of all transactions.

It contains only numerical input variables which are the result of a PCA transformation. Unfortunately, due to confidentiality issues, we cannot provide the original features and more background information about the data. Features V1, V2, … V28 are the principal components obtained with PCA, the only features which have not been transformed with PCA are 'Time' and 'Amount'. Feature 'Time' contains the seconds elapsed between each transaction and the first transaction in the dataset. The feature 'Amount' is the transaction Amount, this feature can be used for example-dependant cost-sensitive learning. Feature 'Class' is the response variable and it takes value 1 in case of fraud and 0 otherwise.

Data set is available here:-[https://www.kaggle.com/mlg-ulb/creditcardfraud](https://www.kaggle.com/mlg-ulb/creditcardfraud)

## Exploratory Data Analysis-
Exploratory Data Analysis where we will analyze the dataset to find some significant patterns,dealing with missing values and duplicates present in data and distributions of different features in dataset.
The steps in Exploratory data analysis are-

1. Read the data set
2. find shape, info and describe the data set 
3. finding missing values and duplicates
4. Visualize the data set
5. Performed feature scaling-"As we observe the ‘Time’ and ‘Amount’ features need to be scaled before we proceed to build machine learning models."

## Modeling for Prediction

I have used three machine learning models that uses classification algorithm for two-group classification problems.
- Logistic Regression
- Support Vector Classifier
- Random Forest

After separating data into two parts Independent features(X) and dependent feature(y). Split the data set into train data and test data.

After fitting the model, i got high accuracy of models.But is the model good for prediction?**NO**

## Imbalance dataset-

We can see that dependent feature our data set is highly imbalance.
![download](https://user-images.githubusercontent.com/78952426/127499316-c9c3bb9b-96e7-4168-8904-c404d01134de.png)
 When a classifier is trained on a highly imbalance dataset,it has a tendency to pick the patterns in the most popular class and ignore the rest.
 
 For this dataset,99.9% of the data are labelled as 'Not Fraud' and rest are 'Fraud'. So,even if a model classifies everything that it is as 'Not Fraud',the accuracy is going to be high but the model is not good because it is not classifying any of the transaction as 'Fraud'.So,even if model has high accuracy, it is completely useless.
 
## Dealing With Imbalance Dataset-

There are two Sampling techniques to deal with the imbalanced datasets.
1. Under Sampling
2. Over Sampling

**Under Sampling-**

Undersampling refers to a group of techniques designed to balance the class distribution for a classification dataset that has a skewed class distribution. It removes examples from the training dataset that belong to the majority class in order to better balance the class distribution.

**Over Sampling-**
It solves imbalance dataset by oversampling the examples in the minority classes. This can be achieved by simply duplicating examples from the minority class in the training dataset.

I have fitted three models on Under sampled data and Over sampled data.

As the analysis is focused on credit card fraud detection, i have evaluated the performance of the Model based on few metrics listed below:
1. Confusion Matrix
2. Accuracy, Recall, Precision and F1-Score
3. ROC Curve and AUC


## Conclusion-
- In this project i understood how data imbalance is major challenge to deal with during building a model.
- I have learnt techniques to deal with imabalance data set.
- I have compared different classification algorithm for making predictions.






