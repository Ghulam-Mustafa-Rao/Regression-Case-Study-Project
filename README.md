# Regression-Case-Study-Project

Random Forest Regressor Tuning
 We used grid search with cross-validation to find the best settings for the Random Forest Regressor. The best parameters were:
 max_depth: None (no limit on tree depth)
 min_samples_leaf: 4 (each leaf must have at least 4 samples)
 min_samples_split: 10 (minimum 10 samples to split a node)
 n_estimators: 200 (number of trees in the forest)
Results:
 Best RMSE during cross-validation: 0.0681
 Best R² during cross-validation: 0.7523
 Test RMSE: 0.0686
 Test R² Score: 0.8176

Decision Tree Regressor Tuning
 We also tuned a Decision Tree Regressor using grid search. The best parameters were:
 max_depth: 5 (limit tree depth to 5)
 max_features: 'sqrt' (try a square root number of features at each split)
 min_samples_leaf: 4
 min_samples_split: 2
Results:
 Best RMSE during cross-validation: 0.0747
 Best R² during cross-validation: 0.6992
 Test RMSE: 0.0735
 Test R² Score: 0.7906

Top 5 Features (from Feature Importance):
 CGPA - 0.7489
 GRE Score - 0.1396
 TOEFL Score - 0.0360
 SOP - 0.0334
 LOR - 0.0167

Multicollinearity in Linear Regression
 We checked how much the features are related to each other. High relationships between features can cause problems in linear regression, making the results unreliable.
High correlations found:
 GRE and TOEFL Scores: 0.83
 GRE and CGPA: 0.83
 TOEFL Score and CGPA: 0.82
 University Rating and SOP: 0.74
 SOP and LOR: 0.73
 University Rating and CGPA: 0.75
VIF (Variance Inflation Factor) Scores:
 GRE Score: 1477.97 (very high)
 CGPA: 1101.72 (very high)
 TOEFL Score: 1297.29 (very high)
 LOR: 38.07
 SOP: 36.59
 University Rating: 22.24
 Research: 2.77 (acceptable)
Features with VIF over 10 show strong multicollinearity. In this case, GRE Score, CGPA, and TOEFL Score are too similar, which can mess up the linear regression model's results.
Even though our linear regression model performed well (R² = 0.8212), the high multicollinearity makes its predictions less trustworthy.
