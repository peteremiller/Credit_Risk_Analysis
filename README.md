# Credit_Risk_Analysis
## Overview of the Analysis

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, I employed different techniques to train and evaluate models with unbalanced classes. I used imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using a CSV credit card credit dataset from LendingClub, a peer-to-peer lending services company, I oversampled the data using the RandomOverSampler and SMOTE algorithms, and undersampled the data using the ClusterCentroids algorithm. Then, I used a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, I compared two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk.

## Purpose of the Analysis
Now that I have completed the analysis, the information below highlights the performance of the six models. I will also provide a recommendation on whether any of the models should be used to predict credit risk.

## Results of the Analysis

- ### Native Random Oversampling


<img src="Resources/oversampling1.png">

- ### SMOTE Oversampling Results
<img src="Resources/over_results2.png">

- ### ClusterCentroids Undersampling Results
<img src="Resources/under_results3.png">

- ### SMOTEENN Combination Sampling Results
<img src="Resources/combo_results4.png">

- ### Balanced Random Forest Classifier
<img src="Resources/forest_results5.png">

- ### Easy Ensemble AdaBoost Classifier
<img src="Resources/easy_results6.png">

## Summary of the Analysis
### Recommendation
