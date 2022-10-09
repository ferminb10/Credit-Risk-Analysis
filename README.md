# Credit-Risk-Analysis
## Overview of the Analysis
### Purpose
We're tasked by the client to apply machine learning to solve credit risk as an unbalanced classification problem. In this project, different techniques to train and evaluate models with unbalanced classes were employed using the imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling. The credit card credit dataset from LendingClub, a peer-to-peer lending services company, the data was oversampled using the RandomOverSampler and SMOTE algorithms, undersampled using the ClusterCentroids algorithm, and over- and undersampled using the SMOTEENN algorithm. Then, two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, were compared to predict credit risk. The analysis provided directional feedback to make a recommendation on whether or not they should be used to predict credit risk.

## Results
The results of the accuracy, precision, and recall scores of all six machine learning models are summarized below. For the first four machine learning models, please refer to the credit_risk_resampling.ipynb file for more details. For the last two machine learning models, please refer to the credit_risk_ensemble.ipynb file for more details.

### [RandomOverSampler](https://imbalanced-learn.org/stable/references/generated/imblearn.over_sampling.RandomOverSampler.html)
_____

![image](https://user-images.githubusercontent.com/107658895/194735894-408346a8-aa8a-4339-b823-a9e37c7aabfb.png)

**Figure 1**: Classification report for the RandomOverSampler model.
_____

* **Accuracy Score**: 62.2%
* **High-Risk Precision Score**: 0.01
* **High-Risk Recall Score**: 0.65

### [SMOTE](https://imbalanced-learn.org/stable/references/generated/imblearn.over_sampling.SMOTE.html)
_____

![image](https://user-images.githubusercontent.com/107658895/194735985-12b197ac-d445-44cd-ac34-6697bc762042.png)

**Figure 2**: Classification report for the SMOTE model.
_____

* **Accuracy Score**: 65.8%
* **High-Risk Precision Score**: 0.01
* **High-Risk Recall Score**: 0.63

### [ClusterCentroids](https://imbalanced-learn.org/stable/references/generated/imblearn.under_sampling.ClusterCentroids.html)
_____

![image](https://user-images.githubusercontent.com/107658895/194736178-b0298b82-fc57-4f04-8abd-1947228bbcc3.png)

**Figure 3**: Classification report for the ClusterCentroids model.
_____

* **Accuracy Score**: 54.42%
* **High-Risk Precision Score**: 0.01
* **High-Risk Recall Score**: 0.69

### [SMOTEENN](https://imbalanced-learn.org/stable/references/generated/imblearn.combine.SMOTEENN.html)
_____

![image](https://user-images.githubusercontent.com/107658895/194736095-47cb3bcf-ee31-4538-8bb4-6cc05d4a9410.png)

**Figure 4**: Classification report for the SMOTEENN model.
_____

* **Accuracy Score**: 65.65%
* **High-Risk Precision Score**: 0.01
* **High-Risk Recall Score**: 0.79

### [BalancedRandomForestClassifier](https://imbalanced-learn.org/stable/references/generated/imblearn.ensemble.BalancedRandomForestClassifier.html)
_____

![BalancedRandomForestClassifier_classification_report](https://user-images.githubusercontent.com/80941606/194734077-32092578-5448-4a1d-b13d-0249227634a7.png)

**Figure 5**: Classification report for the BalancedRandomForestClassifier model.
_____

* **Accuracy Score**: 78.78%
* **High-Risk Precision Score**: 0.04
* **High-Risk Recall Score**: 0.67

### [EasyEnsembleClassifier](https://imbalanced-learn.org/stable/references/generated/imblearn.ensemble.EasyEnsembleClassifier.html)
_____

[There was an error with one or many of the imported libaries, so the table could not be output]

**Figure 6**: Classification report for the EasyEnsembleClassifier model.
_____

* **Accuracy Score**: 92.54%
* **High-Risk Precision Score**: 0.04
* **High-Risk Recall Score**: 0.67

## Summary
### Comparison
In summary, the EasyEnsembleClassifier model has the highest accuracy, precision, and recall scores as can be seen in the results section. This makes it the ideal model to use for this credit risk analysis project.

### Recommendation
The EasyEnsembleClassifier model would be the best to use for credit risk analysis; however, since it high-risk precision score is only 0.07, this would not be high enough for real-world use. Moreover, additional research on how to improve upon these models is required.
