# Credit_Risk_Analysis


## Overview

The purpose of this analysis was to analyze a credit card credit dataset from LendingClub, a peer-to-peer lending services company. Since credit risk is an inherently unbalanced classification problem, different techniques were used to train and evaluate models. The data was encoded and run through oversampling algorithms (RandomOverSampler and SMOTE), an undersampling algorithm (ClusterCentroids), and a combinatiorial approach of over-and undersampling (SMOTEENN algorithm). Then, a comparison was made between two models that aimed to reduce bias (BalancedRandomForestClassifier and EasyEnsembleClassifier) to predict credit risk. Once each model is run, the results are evaluated to determine if they should be used to predict credit risk.


## Results

The following are results of each model. The balanced accuracy score, precision, and recall of each machine learning model.

### RandomOverSampler

![RandomOverSampler](https://github.com/Aleahkita/Credit_Risk_Analysis/blob/main/Images/RandomOversampler.png)

- Balanced accuracy score of ~0.65
- Precision score of 0.99
- Recall score of 0.58


### SMOTE

![SMOTE](https://github.com/Aleahkita/Credit_Risk_Analysis/blob/main/Images/SMOTE.png)

- Balanced accuracy score of ~0.66
- Precision score of 0.99
- Recall score of 0.68


### ClusterCentroids

![ClusterCentroids](https://github.com/Aleahkita/Credit_Risk_Analysis/blob/main/Images/ClusterCentroids.png)

- Balanced accuracy score of ~0.54
- Precision score of 0.99
- Recall score of 0.40


### SMOTEENN

![SMOTEENN](https://github.com/Aleahkita/Credit_Risk_Analysis/blob/main/Images/Combination(Over%26Under).png)

- Balanced accuracy score of ~0.67
- Precision score of 0.99
- Recall score of 0.60



### BalancedRandomForestClassifier

![BalancedRandomForestClassifier](https://github.com/Aleahkita/Credit_Risk_Analysis/blob/main/Images/BalancedRandomForest.png)

- Balanced accuracy score of ~0.79
- Precision score of 0.99
- Recall score of 0.87



### EasyEnsembleClassifier

![EasyEnsembleClassifier](https://github.com/Aleahkita/Credit_Risk_Analysis/blob/main/Images/EasyEnsemble.png)

- Balanced accuracy score of ~0.93
- Precision score of 0.99
- Recall score of 0.94



## Summary

The resampling algorithms (RandomOverSampler, SMOTE, ClusterCentroids, SMOTEENN) all performed poorly with accuracy scores of 0.65, 0.66, 0.54, 0.67 respectively. While resampling algorithms are ideal for imbalanced data, the models are not adequately predicting each class individually. The resampling algorithms also had inadequate recall scores of 0.58, 0.68, 0.40, 0.60 respectively.  
When looking at the models that aimed to reduce bias (BalancedRandomForestClassifier and EasyEnsembleClassifier) there was a significant improvement in both accuracy and recall scores. The accuracy scores were 0.79, 0.93 respectively. The recall scores were 0.87, 0.94 respectively. 
Precision for all models was 0.99.
Based on scores from each model, the EasyEnsembleClassifier is the recommended model to use due to the highest balanced accuracy score (0.93) and recall score (0.94). This means that the model is able to correctly identify class 93% of the time and out of all the loans that actually were high risk, the model predicted that outcome correctly 94% of the time. This model far outperforms the others in terms of overall accuracy and metrics.
