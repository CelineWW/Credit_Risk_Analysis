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
  - The accuracy score of the model
  - Confusion matrix
  - Imbalanced classification report
