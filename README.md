# Credit_Risk_Analysis
## Overview
### Purpose
The purpose of this analysis was to use different machine learning models to analyze credit risk and determine which model would be best for accurately identifying loan applicants as being high risk or low risk.

## Results

#### Random Oversampling

![Oversampling](https://github.com/RBarbush84/Credit_Risk_Analysis/blob/main/Resources/Oversampling.png)

* Balanced Accuracy- 63.7%

* High Risk Precision- 1%

* High Risk Recall- 62%

* Low Risk Precision- 100%

* Low Risk Recall- 65%

#### SMOTE

![SMOTE](https://github.com/RBarbush84/Credit_Risk_Analysis/blob/main/Resources/SMOTE.png)

* Balanced Accuracy- 63%

* High Risk Precision- 1%

* High Risk Recall- 62%

* Low Risk Precision- 100%

* Low Risk Recall- 64%

#### Cluster Centroid

![Cluster_Centroid](https://github.com/RBarbush84/Credit_Risk_Analysis/blob/main/Resources/Undersampling.png)

* Balanced Accuracy- 51%

* High Risk Precision- 1%

* High Risk Recall- 59%

* Low Risk Precision- 100%

* Low Risk Recall- 43%

#### SMOTEENN

![SMOTEENN](https://github.com/RBarbush84/Credit_Risk_Analysis/blob/main/Resources/SMOTEENN.png)

* Balanced Accuracy- 65.3%

* High Risk Precision- 1%

* High Risk Recall- 71%

* Low Risk Precision- 100%

* Low Risk Recall- 59%

#### BRFC


* Balanced Accuracy- N/A

* High Risk Precision- N/A

* High Risk Recall- N/A

* Low Risk Precision- N/A

* Low Risk Recall- N/A

#### EEC


* Balanced Accuracy- N/A

* High Risk Precision- N/A

* High Risk Recall- N/A

* Low Risk Precision- N/A

* Low Risk Recall- N/A

## Summary

There were some issues with running the Balanced Random Forest Classification and the Easy Ensemble Classifier, so for the time being they are not included in this analysis.

For the other models tested (Oversampling, SMOTE, Cluster Centroids Undersampling and SMOTEENN), they were all found to have very similar precision scores for both high risk (1%) and low risk (100%) applicants. All of these models were effective at identifying low risk applicants, as all applicants predicted to be low risk were in fact low risk. However, for the applicants predicted to be high risk, only 1% of them actually were high risk.

The recall for these models may be a better indicator of their effectiveness. Looking at recall for the high risk applicants, the SMOTEENN model has the highest recall at 71%, while the oversampling and SMOTE models were both at 62%. However, both oversampling (65%) and SMOTE (64%) outperformed SMOTEENN (59%) in terms of recall for low risk applicants. The cluster centroid undersampling model performed worst of all of these methods for both high risk and low risk recall.

The analysis also measured the total balanced accuracy of the models, and of these, the cluster centroid model was again the worst performing at 51%. The SMOTEENN model had the highest accuracy (65.3%), just above those of the oversampling model (63.7%) and the SMOTE model (63%).

Of these models, I would recommend using the SMOTEENN model because of its total balanced accuracy numbers and high recall for high risk applicants, but it should be noted that the very low precision for high risk applicants is a major drawback and something to look at improving for this model.
