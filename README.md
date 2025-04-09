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

   # Stacking Ensemble
   Built a 1-layer stacking model with:
   - Base Learners: Decision Tree, Random Forest, Gradient Boosting
   - Meta-Learner: Gradient Boosting Regressor
     
     # Process:
   1. Fit base models on training data.
   2. Generate predictions as input for meta-model.
   3. Fit meta-model on these new inputs.

   ## Kaggle Submission Results:
           Model                Kaggle Private Score (RMSE)
        Gradient Boosting -->     1249.12925 (Best)
        Random Forest -->         ~1255 (approx.)
        Decision Tree -->         Higher error (baseline only)
        Stacked Ensemble -->      2233.13579 (Overfitting)
   - Gradient Boosting Regressor achieved the lowest error and was the best standalone model.
   - Stacked model underperformed due to blending or overfitting issues.

   ##  Key Learnings
   - Gradient Boosting was the most effective single model.
   - Stacking is powerful but must be tuned carefully to avoid poor generalization.
   - Feature selection helps simplify models, but excessive reduction can degrade performance.
   - Cross-validation and leaderboard feedback are crucial in regression tasks.

   ## Future Enhancements
   - Use Advanced Stacking (e.g., out-of-fold predictions)
   - Try XGBoost, LightGBM, or CatBoost
   - Apply log-transform on skewed loss values
   - Explore early stopping in Gradient Boosting
   - Use Blending instead of Stacking to reduce overfitting




   


     


   
   





