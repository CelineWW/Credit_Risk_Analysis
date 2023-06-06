# Credit Risk Analysis
 **:small_blue_diamond: Supervised Maching Learning :small_blue_diamond: Resampling :small_blue_diamond:**
## Overview
Credit risk can be predicted by some machine learning models. However, the number of good loans is far more than risky loans. The dataset is heavily unbalanced. In this project, credit card credit dataset from LendingClub was splitted into training and testing subset, and then resampled. six machine learning models were fit to training data to predict credit risk. The accuracy of predictions from each model was calculated. Based on the results, the best credit risk prediction model was recommended according to balanced accuracy score, the precision and sensitivity scores of each model.
- Models: 
  - Logistic regression model with random oversampled data
  - Logistic regression model with synthetic minority oversampled(SMOTE) data
  - Logistic regression model with cluster centriod undersampled data
  - Logistic regression model with oversampled and undersampled combination(SMOTEENN) data
  - Balanced random forest classification model
  - Easy ensemble adaptive boosting classification model
- Evaluations:
  - Accuracy score of the model
  - Confusion matrix
  - Imbalanced classification report
  
 ## Results
 ### Models with unscaled dataset
 1. **Naive Random Oversampling Model**
    :arrow_lower_right: 
    - Balanced accuracy score: **65%**
    - Precision of high risk: **1%**
    - Recall(Sensitivity) of high risk: **71%**
   
    ![Naive Random Oversampling Model](https://user-images.githubusercontent.com/105877888/191419580-ea8d49c7-9c61-42d8-9ad4-c53d70b5adfa.png)

 
 2. **SMOTE Model**
    :arrow_lower_right: 
    - Balanced accuracy score: **66%**
    - Precision of high risk: **1%**
    - Recall(Sensitivity) of high risk: **63%**
    
    ![SMOTE Model](https://user-images.githubusercontent.com/105877888/191419600-a5dae719-e96f-4167-859d-011b6456c484.png)

 
 3. **Cluster Centeroids Model**
    :arrow_lower_right: 
    - Balanced accuracy score: **54%**
    - Precision of high risk: **1%**
    - Recall(Sensitivity) of high risk: **69%**
    
    ![Cluster Centroids Model](https://user-images.githubusercontent.com/105877888/191419613-29057895-4a4a-415c-85b4-2f648be5cd08.png)

   
 4. **SMOTEENN Model**
    :arrow_lower_right: 
    - Balanced accuracy score: **62%**
    - Precision of high risk: **1%**
    - Recall(Sensitivity) of high risk: **68%**
    
    ![SMOTEENN Model](https://user-images.githubusercontent.com/105877888/191419624-f5cc523f-09ef-488a-9f27-7878a5f85d33.png)

 
 5. **Balanced Random Forest Model**
    :arrow_lower_right: 
    - Balanced accuracy score: **79%**
    - Precision of high risk: **3%**
    - Recall(Sensitivity) of high risk: **70%**
    
    ![Balanced Random Forest Model](https://user-images.githubusercontent.com/105877888/191419634-b2ac04ef-f3e5-4ccd-97f7-ef512a8bc989.png)

 
 6. **Easy Ensemble Model**
    :arrow_lower_right: 
    - Balanced accuracy score: **93%**
    - Precision of high risk: **9%**
    - Recall(Sensitivity) of high risk: **92%**
    
    ![Easy Ensemble Model](https://user-images.githubusercontent.com/105877888/191419652-5e1ebed0-4f8d-4c52-b48a-02a6f7bdcdc1.png)

### Models with scaled data

- This table shows model performance before and after scaling with StandardScalar (`mean = 0, SD = 1`) .
---

| Model                               | Balanced accuracy score  | Precision of high risk | Recall of high risk | F1 score of high risk | 
|:------                              |:------                   |:------                 |:------              | :------               | 
| **Naive Random Oversampling Model** | 0.84 > `0.66`            | 0.03 > `0.01`          | 0.83 > `0.71`       | 0.06 > `0.02`         |
| **SMOTE Oversampling Model**        | 0.84 > `0.66`            | 0.03 > `0.01`          | 0.81 > `0.63`       | 0.07 > `0.02`         |
| **Cluster Centeroids Undersampling Model** | 0.81 > `0.54`     | 0.02 > `0.01`          | 0.86 > `0.69`       | 0.04 > `0.01`         |
| **SMOTEENN Combined Resampling Model** | 0.85 > `0.62`         | 0.03 > `0.01`          | 0.84 > `0.68`       | 0.06 > `0.02`         |
| **Balanced Random Forest Model**    | 0.79 = `0.79`            | 0.03 = `0.03`          | 0.70 = `0.70`       | 0.06 = `0.06`         |
| **Easy Ensemble Model**             | 0.93 = `0.93`            | 0.09 = `0.09`          | 0.92 = `0.92`       | 0.16 = `0.16`         |
 
---
## Summary
- As shown in the results, Logistic Regression Models with Naive Random Oversampling, SMOTE Oversampling, Cluster Centeroids Undersampling, SMOTEENN Oversampling and Undersampling Combination's accuracy scores are 65%, 66%, 54%, 62% respectively, which means these four resampling logistic regression models have 65%, 66%, 54%, 62% chances to accept that the predictions are correct. In other words, the first four models also have 35%, 34%, 46%, 38% probilities of rejection. Balanced Random Forest Model and Easy Ensemble Model get much higher accuracy scores, which are 79% and 93%. 

- For all six models, the precision of high risk are under 10%. Easy Ensemble Model slightly surpasses the other models. This is a disappointing result, indicating a large number of false positives. Being predicted as high risk with these models only means less than 10% likelyhood of actually having credit fraudulent risk.  

- Feature scaling makes a great benefit for Logistic regression. For this scenario, all model performance are greatly improved after scaling. In contrast, random forest and easy ensemble model do not get any advantages from feature scaling. Because both of these two models are tree-based model and hence does not require feature scaling. 

- Easy Ensemble Model get a higher recall score (92%). The other five models' sensitivity scores are around 80% even after scaled. High sensitivity scores stand for a large portion of potentially high risky loans are detected. 

- Recommendations: Overall, Easy Ensemble Model held the best performance on predicting high risk of customer's credit among six models in this project. Easy Ensemble Model seems got a satisfing accuracy score(93%) and recall of high risk(92%). However, it had a very low precision of high risk cases(9%) at the same time. F1 score(16%) reflected the imbalance between sensitivity and precision. In this credit risk assessment case, we are more concerned about its sensitivity of bad loan (high risk) applications. So Easy Ensemble Model is applicable to the credit risk prediction. At the same time, LendingClub has to be aware of that it is not an ideal model to do the prediction. They might lose a quantity of businesses as a large number of customers were assessed to be high risk whereas they were truely in low risk.

- For the further study, deep learning Neruan Network binary classification can be considered as well in this case. Annomaly detection is not applicable here since it is more suitbale for extremely rare positive cases. While building models, cross validation can be applied to better predict the test results.


