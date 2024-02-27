# financial-fraud-detection-lab

![Financial Fraud Detective](fraud_detective.png)

## Project Overview

In this project, we are analyzing a large dataset for financial banking transactions. Our goal is to identify and flag as many fradulent cases as possible, while minimizing false positives as much as we can. The challenge of this project is the class imbalance of our dataset, where there would be an overwhelmingly more non-fraudulent transactions than there are fradulent. 

For this project we will be utilizing supervised learning method using Ensemble Methods.

The original dataset contained over a million rows. It was too computationally heavy to complete this project without access to cloud based resources. For this project I've decided to use a sample of only 50,000 from the original dataset.

## 01 Exploratory Data Analysis

During the early stages of the EDA process I noticed that our data is right skewed. Many of the datapoints were difficult to see. I was originally thinking about removing all of the outliers. However, when I started conducting bivariate analysis I noticed that the outliers were actually important. This is because most of the outliers were flagged as being a fradulent transaction. When I thought about it, it makes a lot of sense. Most scammers wouldn't want to scam you out of 10 or 20 dollars, they often go for thousands of dollars at once. It is more likely for higher transaction numbers to be fradulent vs non fradulent. I've also discovered there are few columns which are not needed in the dataset. 

Another interesting point about our dataset is that we were given two columns. One is isFraud, and the other isFlaggedFraud. When conducting a bivariate analysis on both columns using a heatmap, I noticed that there were high colerations between both columns detecting non fradulent cases, but isFlaggedFraud failed to detect many of the actual isFraud cases.

## 02 Data Wrangling

In the second step I cleaned and exported the data, dropping unneccessary columns and data in order to prepare us for the third step which is building predictive models. I decided specifically to drop the names in our dataset which includes columns such as "nameOrig" and "nameDest". I've also decided to transform my type column into a numerical label. 

## 03 Modeling

Finally, I've decided to train a few models with our sample dataset using Decision Tree, RandomForestClassifier and finding the best possible hyperparameters using GridSearchCV, RandomSearchCV. 

1. Decision Tree Classifier
![Decision Tree](DecisionTreeClassifierResults.png)

We achieved an accuracy score of 99.91%. 

Grid Search CV
![Grid Search](GridSearchCV.png)

2. Random Forest Classifier
![Random Forest](RandomForestClassifier.png)

Random Search CV
![Random Forest](RandomSearchCV.png)



