# Cryptocurrencies

## Overview of the analysis: 
This analysis uses the credit card credit dataset from LendingClub and applied machine learning to predict credit card risk.  In Python, we used scikit-learn and imbalanced-learn libraries to build and evaluate machine learning models.  The resampling models used were Random oversampling, SMOTE, Undersampling and Combination of over and under sampling (SMOTEENN).  The ensemble models used to reduce bias were Balanced Random Forest Classifier and Easy Ensemble Classifier.  Using the results of the models, we can compare which algorithm results in the best performance.

## Results: 
Each of the resampled models produced a balanced accuracy score and a classification report with precision and recall scores of all six machine learning models. Loan status of 'high risk' vs 'low risk' was used from the dataset as target for prediction, the rest of the dataset was used as features.  The dataset was split to train and test data and calculated with balanced accuracy score, confusion matrix and imbalanced classification report with the below results:

### Deliverable 1

* Balanced accuracy score: 66%
* Precision scores: high risk= 1%; low risk = 100%; Avg = 99%
* Recall scores: high risk = 68%; low risk = 64%; Avg = 64%
* The accuracy is low at 66%.  Even though the average precision score is high in 99%, it is only effective for low risk predictions (100%), not for high risk (1%). The recall or sensitivity is also low for both high and low risk groups with an average of 64%.


### Deliverable 2

![Deliverable2_PCA.png](/Resources/Deliverable2_PCA.png)

### Deliverable 3


![Deliverable3_Kmeans_ElbowCurve.png](/Resources/Deliverable3_Kmeans_ElbowCurve.png)


### Deliverable 4

![Deliverable4_2D_Scatter_cluster.png](/Resources/Deliverable4_2D_Scatter_cluster.png)


![Deliverable4_3D_scatter_clusters.png](/Resources/Deliverable4_3D_scatter_clusters.png)


![Deliverable4_HvplotTable.png](/Resources/Deliverable4_HvplotTable.png)

## Summary:

This loan status data has a disproportionately larger amount of low risk (68,470) than high risk (347).  Using the above resampling methods, the data was changed to be equal count before the Logistric Regression model was used but the results are all low in accuracy with 53 - 66%.  All the precision scores were extremely low in detecting high risks at 1% and low sensitivity with 42 - 66%.  