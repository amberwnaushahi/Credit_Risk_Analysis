![image](https://github.com/amberwnaushahi/Credit_Risk_Analysis/blob/main/Resources/credit-risk-header.jpg)

# Credit Risk Analysis

## Overview

Loans are an essential part of modern society, used by individuals and businesses for a variety of purposes. They present both, a challenge and an opportunity, for financial institutions and predicting credit risk is of utmost importance for lending institutions. Credit risk prediction is an effective way of evaluating whether a potential borrower will repay a loan, particularly in peer-to-peer lending where class imbalance problems are prevalent. 

## Techniques Used

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. **Machine learning** contributes significantly to credit risk modeling applications by providing a better fit for the nonlinear relationships between the explanatory variables and default risk. Machine learning can process a large amount of data to arrive at a single decision - whether to approve a loan application or not. 

As part of this assignment, we will use machine learning to **predict credit risk** using different techniques to train and evaluate models with unbalanced classes. We will use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, we will use the following models and evaluate which is better at predicting credit risk:
* Oversample the data using the RandomOverSampler and SMOTE algorithms
* Undersample the data using the ClusterCentroids algorithm. 
* Use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. 
* Compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. 

For each technique, we will:
* resample the dataset
* view the count of the target classes
* train a logistic regression classifier
* calculate the balanced accuracy score
* generate a confusion matrix
* generate a classification report.

## Resources
* Data Source: LoanStats_2019Q1.csv
* Software: Python 3.9.6, Conda 4.10.3, Imbalanced-learn 0.8.1, Scikit-learn 1.0.1

## Results:

* **OverSampling: Random Over Sampler**
  * Balanced Accuracy Score: 0.66
  * Precision: 0.99
  * Recall: 0.6

![image](https://github.com/amberwnaushahi/Credit_Risk_Analysis/blob/main/Resources/Naive%20Oversampling.PNG)

* **OverSampling: SMOTE**
  * Balanced Accuracy Score: 0.66
  * Precision: 0.99
  * Recall: 0.69
 
 ![image](https://github.com/amberwnaushahi/Credit_Risk_Analysis/blob/main/Resources/SMOTE%20Oversampling.PNG)
  
* **UnderSampling: ClusterCentroids**
  * Balanced Accuracy Score: 0.54
  * Precision: 0.99
  * Recall: 0.4
 
 ![image](https://github.com/amberwnaushahi/Credit_Risk_Analysis/blob/main/Resources/Undersampling.PNG)
 
* **Combinatorial: SMOTEENN**
  * Balanced Accuracy Score: 0.64
  * Precision: 0.99
  * Recall: 0.4
  
 ![image](https://github.com/amberwnaushahi/Credit_Risk_Analysis/blob/main/Resources/Combination.PNG)
  
* **BalancedRandomForestClassifier**
  * Balanced Accuracy Score: 0.79
  * Precision: 0.99
  * Recall: 0.87
  
 ![image](https://github.com/amberwnaushahi/Credit_Risk_Analysis/blob/main/Resources/Balanced%20Forest%20Classifier.PNG)
   
* **EasyEnsembleClassifier**
  * Balanced Accuracy Score: 0.93
  * Precision: 0.99
  * Recall: 0.94
 
 ![image](https://github.com/amberwnaushahi/Credit_Risk_Analysis/blob/main/Resources/Easy%20Ensemble.PNG)

Using the features importance, we were also able to identify the following features as most important in determining the credit risk:

![image](https://github.com/amberwnaushahi/Credit_Risk_Analysis/blob/main/Resources/Top%20Features.PNG)

## Summary: 

The objective of this analysis is to determine credit risk accurately. It is more important to minimize false negatives i.e. identifying high risk applications as low risk versus false positives i.e. identifying lower risk applications are higher risk as false negatives can lead to a higher number of defaults while false positives would cost the business potential profits. It is crucial to have a higher recall in the predictions to minimize the risk.

Based on this and the results of the various models, it appears that the **Easy Ensemble Classifier** is the best model to consider as it gives the highest recall, along with the balanced accuracy score and precision. The business should use this model for credit risk predictions to minimize its risk.



