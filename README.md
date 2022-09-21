# Credit Risk Analysis
## Overview
Credit risk can be predicted by some machine learning models. However, the number of good loans is far more than risky loans. The dataset is heavily unbalanced. In this project, credit card credit dataset from LendingClub was splitted into training and testing subset, and then resampled. six machine learning models were trainned and fitted to data to predict credit risk. Based on the results, the best credit risk prediction model was recommended according to balanced accuracy score, the precision and recall scores of each model.
- Models: 
  - Logistic regression model with random oversampled data
  - Logistic regression model with synthetic minority oversampled(SMOTE) data
  - Logistic regression model with cluster centriod undersampled data
  - Logistic regression model with oversampled and undersampled combination(SMOTEENN) data
  - Balanced random forest model
  - Easy ensemble model
- Evaluations:
  - Accuracy score of the model
  - Confusion matrix
  - Imbalanced classification report
  
 ## Results
 1. **Naive Random Oversampling Model**
 
    :arrow_lower_right:  
   
    ![Naive Random Oversampling Model](https://user-images.githubusercontent.com/105877888/191419580-ea8d49c7-9c61-42d8-9ad4-c53d70b5adfa.png)

 
 2. **SMOTE Model**
 
    :arrow_lower_right: 
   
    ![SMOTE Model](https://user-images.githubusercontent.com/105877888/191419600-a5dae719-e96f-4167-859d-011b6456c484.png)

 
 3. **Cluster Centeroids Model**
 
    :arrow_lower_right: 
   
    ![Cluster Centroids Model](https://user-images.githubusercontent.com/105877888/191419613-29057895-4a4a-415c-85b4-2f648be5cd08.png)

   
 4. **SMOTEENN Model**
 
   :arrow_lower_right: 
   
   ![SMOTEENN Model](https://user-images.githubusercontent.com/105877888/191419624-f5cc523f-09ef-488a-9f27-7878a5f85d33.png)

 
 5. **Balanced Random Forest Model**
 
    :arrow_lower_right: 
   
    ![Balanced Random Forest Model](https://user-images.githubusercontent.com/105877888/191419634-b2ac04ef-f3e5-4ccd-97f7-ef512a8bc989.png)

 
 6. **Easy Ensemble Model**
 
    :arrow_lower_right: 
   
    ![Easy Ensemble Model](https://user-images.githubusercontent.com/105877888/191419652-5e1ebed0-4f8d-4c52-b48a-02a6f7bdcdc1.png)

