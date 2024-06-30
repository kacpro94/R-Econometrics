# Linear Model Analysis Based on `food.csv` Data

## Objectives

1. Estimate the parameters of a linear model describing the relationship between expenses (Y) and income (X).
2. Investigate the impact of transformations of the dependent variable (Y) or the independent variable (X) on the values of the model's parameter estimators.
3. Justify the observed results using the formulas for the estimators of the model parameters.

## Data Preparation

1. Load the data from `food.csv`.
2. Explore the dataset to understand its structure and clean the data if necessary.

## Linear Model Estimation

1. **Initial Model**  
   Fit the linear model:  
   \[ Y = \beta_0 + \beta_1 X + \epsilon \]  
   where \( Y \) represents expenses and \( X \) represents income.
   
2. **Parameter Estimation**  
   Estimate the parameters \( \beta_0 \) and \( \beta_1 \) using the ordinary least squares (OLS) method.

## Transformations

Apply the following transformations and analyze their impact on the parameter estimators \( \beta_0 \) and \( \beta_1 \):

1. **Multiplying X by a Number**  
   Transform \( X \) to \( X' = cX \) where \( c \) is a constant.
2. **Adding a Number to X**  
   Transform \( X \) to \( X' = X + c \) where \( c \) is a constant.
3. **Multiplying Y by a Number**  
   Transform \( Y \) to \( Y' = cY \) where \( c \) is a constant.
4. **Adding a Number to Y**  
   Transform \( Y \) to \( Y' = Y + c \) where \( c \) is a constant.
5. **Multiplying X and Y by Numbers**  
   Transform \( X \) to \( X' = c_1X \) and \( Y \) to \( Y' = c_2Y \) where \( c_1 \) and \( c_2 \) are constants.
6. **Adding Constants to X and Y**  
   Transform \( X \) to \( X' = X + c_1 \) and \( Y \) to \( Y' = Y + c_2 \) where \( c_1 \) and \( c_2 \) are constants.

## Analysis

For each transformation, perform the following steps:

1. **Fit the Transformed Model**  
   Fit the linear model to the transformed variables.
2. **Estimate Parameters**  
   Estimate the parameters \( \beta_0 \) and \( \beta_1 \) for the transformed model.
3. **Compare Estimates**  
   Compare the estimates of \( \beta_0 \) and \( \beta_1 \) from the transformed model with those from the initial model.
4. **Theoretical Justification**  
   Use the formulas for the OLS estimators to theoretically justify the observed changes in the parameter estimates.

## Theoretical Justification

### Ordinary Least Squares (OLS) Estimators

The OLS estimators for the linear model \( Y = \beta_0 + \beta_1 X + \epsilon \) are given by:

\[ \hat{\beta}_1 = \frac{\sum_{i=1}^{n} (X_i - \bar{X})(Y_i - \bar{Y})}{\sum_{i=1}^{n} (X_i - \bar{X})^2} \]

\[ \hat{\beta}_0 = \bar{Y} - \hat{\beta}_1 \bar{X} \]

### Effect of Transformations

1. **Multiplying X by a Number**  
   If \( X' = cX \):
   - The slope estimator \( \hat{\beta}_1 \) is affected as it scales by \( 1/c \).
   - The intercept \( \hat{\beta}_0 \) is adjusted accordingly.
   
2. **Adding a Number to X**  
   If \( X' = X + c \):
   - The slope estimator \( \hat{\beta}_1 \) remains unchanged.
   - The intercept \( \hat{\beta}_0 \) adjusts to account for the shift in \( X \).

3. **Multiplying Y by a Number**  
   If \( Y' = cY \):
   - Both the slope \( \hat{\beta}_1 \) and intercept \( \hat{\beta}_0 \) scale by \( c \).
   
4. **Adding a Number to Y**  
   If \( Y' = Y + c \):
   - The slope estimator \( \hat{\beta}_1 \) remains unchanged.
   - The intercept \( \hat{\beta}_0 \) shifts by \( c \).
   
5. **Multiplying X and Y by Numbers**  
   If \( X' = c_1X \) and \( Y' = c_2Y \):
   - The slope \( \hat{\beta}_1 \) scales by \( c_2/c_1 \).
   - The intercept \( \hat{\beta}_0 \) scales by \( c_2 \).
   
6. **Adding Constants to X and Y**  
   If \( X' = X + c_1 \) and \( Y' = Y + c_2 \):
   - The slope estimator \( \hat{\beta}_1 \) remains unchanged.
   - The intercept \( \hat{\beta}_0 \) adjusts to account for the shifts in both \( X \) and \( Y \).

## Summary

- Present the results of the parameter estimates for each transformation.
- Discuss how and why the estimates change based on the transformations.
- Provide theoretical justification for the observed results using the OLS estimator formulas.

By understanding the impact of these transformations, we gain insights into the robustness and sensitivity of the parameter estimators in linear regression models.
