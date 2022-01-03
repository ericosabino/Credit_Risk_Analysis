# Credit Risk Analysis

## Overview

Loans are an essential part of modern society, used by individuals and businesses for a variety of purposes. They present both, a challenge and an opportunity, for financial institutions and predicting credit risk is of utmost importance for lending institutions. 

Credit risk prediction is an effective way of evaluating whether a potential borrower will repay a loan, particularly in peer-to-peer lending where class imbalance problems are prevalent.

Also, credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, different techniques will be employed to train and evaluate models with unbalanced classes. 

## Technologies used

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, I'll oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, I'll use a combinatorial approach of oversampling and undersampling using the SMOTEENN algorithm. 

Secondly, I'll compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier.

Lastly, I'll compare the performance of these models and determine whether they should be used to predict credit risk.

## Resources
- Jupyter Notebooks
- Python (3.9.7)
- scikit-learn (1.0.1)
- numpy (1.21.2)
- Data Source: [LoanStats_2019Q1.csv](/LoanStats_2019Q1.csv)


## Results

Below the results of each the resampling and Ensembling method ()

### Oversampling
#### Random Oversampling
![](/Images/01.png)

- Precision: 0.99
- Recall: 0.62 
- Balanced Accuracy Score: 0.640324421824783

#### SMOTE 
![](/Images/02.png)

- Precision: 0.99
- Recall: 0.69 
- Balanced Accuracy Score: 0.6514992150524688


#### Undersampling
![](/Images/03.png)

- Precision: 0.99
- Recall: 0.40
- Balanced Accuracy Score: 0.5442369453268994

### Combination (Over and Under) Sampling - SMOTEENN
![](/Images/04.png)
- Precision: 0.99
- Recall: 0.57 
- Balanced Accuracy Score: 0.6449163069955265


## Ensembling Learners

### Random Forest Classifier
![](/Images/05.png)
- Precision: 0.99
- Recall: 0.87 
- Balanced Accuracy Score: 0.6514992150524688

### Easy Ensemble Classifier
![](/Images/06.png)
- Precision: 0.99
- Recall: 0.94 
- Balanced Accuracy Score: 0.931601605553446

## Summary

All the models had precisions of 0.99, but the resampling models had recall rates between 0.40 and 0.69 and Balaanced Accuracy Scores between 0.54 and 0.65.

The Emsembling Learners Methods performed much better, with recall rates of 0.87 and 0.94, and Accuracy Scores of 0.65 and 0.93.

The method that should be used to predict the credit risk is, based on the source dataset, the Easy Ensemble Classifier, which clearly outperforms the other methods with a much higher Accuracy Score.