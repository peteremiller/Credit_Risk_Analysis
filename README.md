# Credit_Risk_Analysis
## Overview of the Analysis

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, I employed different techniques to train and evaluate models with unbalanced classes. I used imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling to predict credit risk.

Using a CSV credit card credit dataset from LendingClub, a peer-to-peer lending services company, I oversampled the credit card data using the RandomOverSampler and SMOTE algorithms, and undersampled the data using the ClusterCentroids algorithm. Then, I used a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, I compared two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk.

## Purpose of the Analysis
The purpose of this analysis is to determine if any of the six models provide a reliable credit risk predicitve tool using the provided dataset from LendingClub. I will also provide a recommendation concerning one or more of the model's performance. That is, what percentage does it accuractely predict? Each of the models reported an accuracy score and confusion matrix table with four quadrants. The columns of each table represent the predicted high and predicted low risks. The rows of each table repesent the true high and true low risks. The balanced accuracy score represents one way to validate of a model's performanace, but it is not always an appropriate or a meaningful performance metric. There are two additional performance metrics that will also be employed in making my recommendation: precision and sensitivity. Precision, also known as the PPV (positive predictive value) is a measure of how reliable a positive classification is. Precision answers the question: Now that I have a positive result, how likely is it to be true? Likewise, sensitivity, also called recall, represents the measure of how many true results were correctly predicted. Another measure, the F1 score, also caled the harmonic mean, is a single summary statistic of precision and sensitivity. A low F1 score will indicate a predicted pronounced imbalance between sensitivity and precision. 

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
In the first four models we undersampled, oversampled and did a combination of both to try and determine which model is best at predicting which loans are the highest risk. The next two models we resampled the data using ensemble classifiers to try and predict which which loans are high or low risk. In our first four models our accuracy score is not as high as the ensemble classifiers and the recall in the oversampling/undersampling/mixed models is low as well. Typically in your models you want a good balance of recall and precision which is why I recommend the ensemble classifiers over the first four models. It appears that the Easy Ensemble had the best balance of all the models because of it's higher accuracy score and balance of precision and recall scores.
### Recommendation
All models show quite poor predicting results (all of them are lower than the 75th percentile). According to that, I would strongly recommend to improve the LogisticRegression model by using a solver not found in the six models used in this analysis. 
