# Allstate Claims Severity Regression Modeling Stacking Ensemble

  ## Problem Statement
  Allstate Insurance aimed to build a model that can predict the severity of insurance claims based on anonymized policyholder and claim features. The challenge was to
  optimize for low error on a continuous regression target (loss), with a heavy focus on feature engineering, ensemble learning, and hyperparameter tuning.

  ## Project Goals
  - Predict the continuous loss value as accurately as possible
  - Compare baseline models (Decision Tree, Random Forest, Gradient Boosting)
  - Build and evaluate a stacked ensemble model
  - Perform feature selection to reduce overfitting and improve performance
  - Submit multiple models to Kaggle and compare leaderboard scores

   ## Dataset Overview
     Training Data: 188,318 rows × 1,192 features
     Test Data: 125,546 rows × 1,192 features
     Target Variable: loss (continuous float value)
     
   ## Data Preprocessing
   - Removed ID column
   - Applied One-Hot Encoding to categorical variables
   - Ensured consistent feature alignment between train and test sets
   - Stratified split for training/validation to maintain distribution

   ## Models Developed
   # Baseline Regressors
     1. Decision Tree
     2. Random Forest
     3. Gradient Boosting
    All models were evaluated using Root Mean Squared Error (RMSE).
    
   # Hyperparameter Tuning
    - Used RandomizedSearchCV to optimize hyperparameters.
    - Evaluation via K-Fold Cross-Validation.


   
   





