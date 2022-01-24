# Credit Risk Analysis

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company,two new machine learning models to predict credit risk are created using BalancedRandomForestClassifier and EasyEnsembleClassifier, and their results are compared for review which model is better fit.

## Overview of the loan prediction risk analysis:

To create risk predicting model:
  - Firstly, data will be oversampled using the RandomOverSampler and SMOTE algorithm models. 
  - In next step, undersample the data using the ClusterCentroids algorithm models.
  - Next utilizing combinatorial approach of over- and undersampling, data will be resmapled using the SMOTEENN algorithm models.
  - Using the resampled data, two new machine learning models - BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk are created, and       performance of all these models are compared.

## Results:

 **1. Naive Random Oversampling:** Balanced accuracy Score: 67%. The precision for the high_risk positivity is very low  at 1%, with very low F1 score. Thus model doesnot seems to be a good fit.
 
![Results Naive Random Oversampling](https://github.com/div1085/Credit_Risk_Analysis/blob/64693996d98f3fb497950bf919906e50a0049b67/resources/Naive%20Random%20Oversampling.png)


  **2. SMOTE Oversampling:** Balanced accuracy Score: 66%. The precision for the high_risk positivity is very low  at 1%, while overall precision is 99%. With low high_risk F1 score, the model doesnot seems to be a good fit.
  
![Results SMOTE Oversampling](https://github.com/div1085/Credit_Risk_Analysis/blob/64693996d98f3fb497950bf919906e50a0049b67/resources/SMOTE%20Oversampling.png)

 
  **3. Cluster Centroids Undersampling:** Balanced accuracy Score: 54%. The precision for the high_risk positivity is very low  at 1%, while overall precision is 99%.
  
![Results Cluster Centroids Undersampling](https://github.com/div1085/Credit_Risk_Analysis/blob/64693996d98f3fb497950bf919906e50a0049b67/resources/Cluster%20Centroids.png) 

 
  **4. SMOTEENN - Combination (Over and Under) Sampling:** Balanced accuracy Score: 64%. The precision for the high_risk positivity is very low  at 3%, with overall  low F1 score, the model doesnot seems to be a good fit.

![Results SMOTEENN](https://github.com/div1085/Credit_Risk_Analysis/blob/64693996d98f3fb497950bf919906e50a0049b67/resources/SMOTEENN.png)


  **5. Balanced Random Forest Classifier:** Balanced accuracy Score: 78.8%. The precision for the high_risk positivity is very low  at 1%, while overall precision is 99%. Overall F1 score is also high at 93%.
  
![Results Balanced Random Forest Classifier](https://github.com/div1085/Credit_Risk_Analysis/blob/33e4d9239d8d10c084e8e84a97ed610c45e417e9/resources/Balanced%20Random%20Forest%20Classifier.png)  


  **6. Easy Ensemble AdaBoost Classifier:** Balanced accuracy Score: 78.8%. The precision for the high_risk positivity is very low  at 1%, while overall precision is 99%. Overall F1 score is also high at 93%.
  
![Results Easy Ensemble AdaBoost Classifier](https://github.com/div1085/Credit_Risk_Analysis/blob/33e4d9239d8d10c084e8e84a97ed610c45e417e9/resources/Easy%20Ensemble%20AdaBoost%20Classifier.png)


### Summary of the results:
Both the Ensemble models have performed well when compared to models where data was over or under sampled. The ensmble method have overall score of 79%, while all other random sampling models had balanced accuracy scores ranging between 54% to 67%.

### Which model to use?
If choice is pick among these four credit models, one of the ensemble method will do. However, the model needs to be trained on more data with these models to improve the predictibility rate of high risk category, as its more important to predict high risk with high precision compared to low risk.
