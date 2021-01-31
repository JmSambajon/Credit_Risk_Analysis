# Credit_Risk_Analysis

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, you’ll need to employ different techniques to train and evaluate models with unbalanced classes. Imbalanced-learn and scikit-learn libraries will be used to build and evaluate models using resampling.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, RandomOverSampler and SMOTE algorithms is used to oversample the data, and the ClusterCentroids algorithm is used to under sample the data. Then, a combinatorial approach of over- and undersampling using the SMOTEENN algorithm will be used. Next, two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, will be compared to predict credit risk. The performance of these models will then be evaluated and will help create a written recommendation on whether they should be used to predict credit risk.

Here are the model results:

## Naive Random Oversampling

* Balanced accuracy score:		66.1%
* High Risk Precision score:		0.01
* High Risk Recall (sensitivity) score:	0.70
* Low Risk Precision score:		1.00
* Low Risk Recall (sensitivity) score:	0.62

## SMOTE Oversampling

* Balanced accuracy score:		65.8%
* High Risk Precision score:		0.01
* High Risk Recall (sensitivity) score:	0.63
* Low Risk Precision score:		1.00
* Low Risk Recall (sensitivity) score:	0.68

## Undersampling

* Balanced accuracy score:		65.8%
* High Risk Precision score:		0.01
* High Risk Recall (sensitivity) score:	0.68
* Low Risk Precision score:		1.00
* Low Risk Recall (sensitivity) score:	0.41

## Combination (Over and Under) Sampling

* Balanced accuracy score:		64.8%
* High Risk Precision score:		0.01
* High Risk Recall (sensitivity) score:	0.72
* Low Risk Precision score:		1.00
* Low Recall (sensitivity) score:	0.57

## Balanced Random Forest Classifier
*Balanced accuracy score:		78.8%
* High Risk Precision score:		0.03
* High Recall (sensitivity) score:	0.70
* Low Risk Precision score:		1.00
* Low Recall (sensitivity) score:	0.87

## Easy Ensemble AdaBoost Classifier
* Balanced accuracy score:		93.1%
* High Risk Precision score:		0.09
* High Risk Recall (sensitivity) score:	0.92
* Low Risk Precision score:		1.00
* Low Risk Recall (sensitivity) score:	0.94

## Summary
Of the 6 models, the Easy Ensemble AdaBoost Classifier has the highest accuracy score of 93.1%, then the Balanced Random Forest Classifier with an accuracy score of 78.8% The other 4 models range from 64.8% to 66.1% which averages out to 65.63% . All 6 models have a perfect low risk precision score of 1. The model with the best high risk precision score is the Easy Ensemble AdaBoost Classifier with a score of 0.09. The Easy Ensemble AdaBoost Classifier also has the best high risk and low risk recall (sensitivity) score of 0.92 and 0.94, respectively.  Based on these results, the Easy Ensemble AdaBoost Classifier model is the best model to use since it has the best accuracy, precision and recall (sensitivity) scores. While this is the best model to use, be aware the High Risk Precision score precision is still very low.