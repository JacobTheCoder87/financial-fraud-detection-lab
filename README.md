# financial-fraud-detection-lab

![Financial Fraud Detective](../images/fraud_detective.png)

## Project Overview

In this project, we are analyzing a large dataset for financial banking transactions. Our goal is to identify and flag as much fradulent cases as possible, while minimizing false positives as much as we can. The challenge of this problem is the class imbalance of our dataset, where there would be overwhelmingly more non-fraudulent transactions than there are fradulent. 

For this project we will be utilizing supervised learning method using Ensemble Methods.

## 01 Exploratory Data Analysis

In the early stages of the EDA process. I noticed that the data was right skewed. Many of the datapoints were difficult to see. There were many outliers in this dataset. I was originally thinking about removing the outliers. However, when I started conducting bivariate analysis I noticed that those outliers were especially important, since most outliers were flagged as being a fradulent transaction. When I thought about it, it makes a lot of sense. Most scammers wouldn't want to scam you out of 10 or 20 dollars, they often go for thousands of dollars at once so its more likely for higher transaction numbers to be fradulent. I've also discovered there are few columns which are not needed in the dataset.

## 02 Data Wrangling

In the second step I cleaned and exported the data, dropping unneccessary columns and data in order to prepare us for the third step which is building predictive models.

## 03 Modeling

Using ensemble method and randomtreeclassifier, I was able to achieve an accuracy score of over 90%.


