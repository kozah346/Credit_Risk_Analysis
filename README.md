# Credit_Risk_Analysis

## Overview of the analysis

The following machine learning analysis is based on a real-world challenge in the form of credit card risk. Credit risk is an unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, this analysis will employ different techniques to train and evaluate models with unbalanced classes including **imbalanced-learn** and **scikit-learn** libraries to build and evaluate models using resampling. Oversampling the data will happen using **RandomOverSampler** and **SMOTE** algorithms and undersampling will use **ClusterCentroids** algorithm. Then, a combinatorial approach of over/undersampling is used by the **SMOTEENN** algorithm. A comparison is then made by two new machine learning models that reduce bias namely, **BalancedRandomForestClassifier** and **EasyEnsembleClassifier**, to predict risk. An evaluation is then done on the perfomance of these models and a written recommendation as to whether they should be used to predict risk. 

## Results

The following models resulted from the analysis with respective balanced accuracy, precision and recall scores respectively: 

1. Naive Random Oversampling had:
    * Balanced accuracy score of 0.68
    * High_risk/low_risk precision scores of 0.01/1.00 respectively.
    * High_risk/low_risk recall scores of 0.68/0.61 respectively.

<img width="1161" alt="Naive Random Oversampling" src="https://user-images.githubusercontent.com/101376325/179428477-b0c1a3e4-2f6b-493d-902b-fe41a415ba5f.png">

2. SMOTE Oversampling had:
    * Balanced accuracy score of 0.62
    * High_risk/low_risk precision scores of 0.01/1.00 respectively.
    * High_risk/low_risk recall scores of 0.61/0.64 respectively.

<img width="1179" alt="SMOTE Oversampling" src="https://user-images.githubusercontent.com/101376325/179428768-3788362f-24ac-4905-9ea2-d98369845b26.png">

3. Undersampling had:
    * Balanced accuracy score of 0.51
    * High_risk/low_risk precision scores of 0.01/1.00 respectively.
    * High_risk/low_risk recall scores of 0.57/0.45 respectively.

<img width="1165" alt="Undersampling" src="https://user-images.githubusercontent.com/101376325/179428877-47e442c0-d507-4e70-bf46-5fcfe7dd9253.png">

4. Combination of Over/UnderSampling had:
    * Balanced accuracy score of 0.65
    * High_score/low_score precision scores of 0.01/1.00 respectively.
    * High_score/low_score recall scores of 0.69/0.62 respectively. 

<img width="1162" alt="Combination (Over:UnderSampling)" src="https://user-images.githubusercontent.com/101376325/179428954-36ec7fec-9e9b-4916-9237-26346b0adcc2.png">

5. BalancedRandomForestClassifier had:
    * Balanced accuracy score of 0.79
    * High_risk/low_risk precision scores of 0.04/1.00 respectively.
    * High_risk/low_risk recall scores of 0.67/0.91 respectively.

<img width="1119" alt="BalancedRandomForestClassifier" src="https://user-images.githubusercontent.com/101376325/179429038-20583992-88f9-4982-8f5a-81b34dc0626b.png">

6.  Easy Ensemble AdaBoost Classifier had:
    * Balanced accuracy score of 0.94
    * High_risk/low_risk precision scores of 0.07/1.00 respectively.
    * High_risk/low_risk recall scores of 0.91/0.94 respectively. 

<img width="1128" alt="Easy Ensemble AdaBoost Classifier" src="https://user-images.githubusercontent.com/101376325/179429223-3d557607-da81-4738-8432-eb5b62df302f.png">

## Summary:
* From the study above, it is safe to conclude that the Easy Ensemble AdaBoost Classifier is the best model to choose for additional credit risk analysis with a balanced accuracy score of 0.94 and recall scores at 0.91 and 0.94 high_score/low_score respectively. 
* To put the scores to persepective, the closer balanced accuracy scores and recall accuracy scores are to 1 the better the model. The Easy Ensemble AdaBoost Classifier is clearly the better model and should be considered for optimization.