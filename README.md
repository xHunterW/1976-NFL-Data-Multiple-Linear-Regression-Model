# 1976-NFL-Data-Multiple-Linear-Regression-Model
This project models 1976 NFL team win totals using multiple linear regression and a transparent, reproducible workflow applicable to modern NFL datasets.

# Includes:
- Raw Dataset
- Cleaned team-level 1976 features (offense/defense/efficiency-style stats) and a target of wins.
- An analysis notebook/script that builds, diagnoses, and validates the model.
- A final report pdf that summarizes the goals, methods, analysis and conclusions.

# Methods Overview
Feature selection: Starting from a full (null) model, perform transformations where required, then compare models via stepwise search. Selection is guided by out-of-sample criteria (PRESS), parsimony (AIC/BIC), statistical significance, domain logic, and multicollinearity checks (VIF). Correlation plots help avoid redundant predictors.

Model diagnostics: Residuals vs. fitted and by key predictors to assess linearity and homoscedasticity; Q–Q plots for normality; leverage and Cook’s distance to identify influential observations; VIF to monitor collinearity. Sensitivity analyses show how the fit changes when high-influence points are removed.

Predictability evaluation: Train/test split to estimate generalization; report RMSE on the holdout set. Compute PRESS and PRESS-RMSE as an additional cross-validated error check. Optionally include k-fold CV for robustness and 95% prediction intervals for new teams.

Bootstrap testing: Nonparametric bootstrap (e.g., B=1000) of the rows to assess coefficient stability. Report bootstrap means, standard errors, and percentile CIs; compare with model estimates to judge parameter reliability and variable selection stability.

# Outputs
- Final model summary with selected features and coefficients
- Diagnostics and influence plots
- Test-set performance metrics and PRESS
- Bootstrap coefficient summaries

# Report to be updated to include subsequent years, spanning 2000 to present.
