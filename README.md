# Project 1 Linear Model Analysis Based on `food.csv` Data

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
  $$ Y = \beta_0 + \beta_1 X + \epsilon $$  
   where \( Y \) represents expenses and \( X \) represents income.
   
2. **Parameter Estimation**  
   Estimate the parameters \( \beta_0 \) and \( \beta_1 \) using the ordinary least squares (OLS) method.

## Transformations

Apply the following transformations and analyze their impact on the parameter estimators \( \beta_0 \) and \( \beta_1 \):

   **Multiplying Y by a Number**  
   Transform \( Y \) to \( Y' = cY \) where \( c \) is a constant.



# Project 2: Investigation of the Properties of Maximum Likelihood Estimators for Given Distribution Parameters

## Parameters to Change:
- \(N\) – Length of the data
- \(a_0, b_0\) – Model parameters
- \(\sigma\) – Standard deviation of random components

## Procedure:
1. Generate \(x_1, \ldots, x_N\) from a specified distribution.
2. Generate \(\epsilon_1, \ldots, \epsilon_N\) from a specified distribution.
3. Define \(y_i = a_0 + b_0 x_i + \epsilon_i\).
4. Estimate the model parameters \(y = \alpha + \beta x\) using Ordinary Least Squares (OLS).
5. Repeat steps 1-4 1000 times.

Conduct the above study, for example, with \(a_0 = 1\), \(b_0 = 2\). Consider \(N = 10, 20, 50, 100, 500\) and \(\sigma = 1, 2, 5, 10\). Describe how the obtained results depend on \(N\) and \(\sigma\). Consider uniform distributions on the intervals \([0, 20]\) and \([0, 200]\).

In step 1, use a uniform distribution over a specified interval. In step 2, use the normal distribution \(N(0, \sigma)\). In step 4, investigate whether the residuals have a normal distribution (consider 2 tests) and record the p-values of these tests. Draw box plots and density plots of these values. Calculate the percentage of cases rejecting the null hypothesis in the analyzed tests. In step 1, consider intervals of different widths (and examine the effect of the diversity of the explanatory variable on the obtained results). Repeat the study by generating in step 2 random components from the Student's t-distribution with 3 degrees of freedom (rescaled to have a standard deviation equal to \(\sigma\)).


# Project 3 Impact of Omitting a Significant Variable in Regression Analysis

## Setup:
- **Data Generation**: Generate data satisfying the relationship \( y = b_0 + b_1 x_1 + b_2 x_2 + \epsilon \).
- **Model Estimation**: Estimate parameters using two models:
  1. \( y = \alpha_0 + \alpha_1 x_1 + \alpha_2 x_2 + \epsilon \)
  2. \( y = \beta_0 + \beta_1 x_1 + \epsilon \)

## Analysis Steps:

1. **Data Generation**:
   - Generate \( x_1, x_2 \), and \( \epsilon \) from specified distributions to ensure \( y \) follows the given relationship.

2. **Model Estimation**:
   - **Model 1**: Estimate parameters \( \alpha_0, \alpha_1, \alpha_2 \) using Ordinary Least Squares (OLS).
   - **Model 2**: Estimate parameters \( \beta_0, \beta_1 \) using OLS.

3. **Impact on Parameter Estimates**:
   - Compare estimates \( \alpha_1 \) and \( \beta_1 \).
   - Assess the bias and distribution of estimators for \( \alpha_1 \) and \( \beta_1 \).

4. **Errors of Estimators**:
   - Calculate the standard errors of estimators for \( \alpha_1 \) and \( \beta_1 \).

5. **t-Statistics and Hypothesis Testing**:
   - Perform hypothesis tests:
     - \( H_0: \alpha_1 = b_1 \)
     - \( H_0: \beta_1 = b_1 \)
   - Examine the distribution of the t-statistic under \( H_0 \) and calculate rejection rates of \( H_0 \).

6. **Coefficient of Determination (R-squared)**:
   - Compute \( R^2 \) and adjusted \( R^2 \) for both Model 1 and Model 2.

## Key Observations:

- **Effect on Parameter Estimates**: Compare \( \alpha_1 \) and \( \beta_1 \). Discuss any differences and their implications for model interpretation.
- **Errors of Estimators**: Assess the precision of \( \alpha_1 \) and \( \beta_1 \) estimators using standard errors.
- **t-Statistics and Hypothesis Testing**: Analyze the t-statistics under \( H_0 \) and interpret rejection rates of \( H_0 \).
- **Coefficient of Determination**: Compare \( R^2 \) and adjusted \( R^2 \) values between Model 1 and Model 2 to understand the impact on model fit.

## Conclusion:

Summarize how omitting a significant variable affects the model parameters, hypothesis testing results, and model fit measures. Discuss the practical implications of these findings for regression analysis.

This structured approach will allow for a comprehensive analysis of the consequences of omitting a relevant variable in regression modeling, providing insights into the reliability and interpretation of regression results.



# Project 4 Preliminary Data Analysis for Multiple Regression Model

## Problem Description
The data aim to describe factors influencing a specific outcome in various administrative districts (powiats).

## Dependent and Independent Variables
- **Dependent Variable**: The variable to be explained, possibly related to socioeconomic indicators or health outcomes. It is measured in units that represent the outcome being studied.
- **Independent Variables**: These include demographic, economic, and possibly geographic factors. They are measured in various units depending on the specific variable.

## Basic Descriptive Statistics
- Mean, Standard Deviation, Kurtosis, Skewness for each variable.

## Boxplots and Outlier Analysis
- Boxplots for each variable to visualize distributions and identify outliers. Consider removing extremely atypical observations if necessary.

## Coefficient of Variation
- Calculate and interpret coefficients of variation for variables. Discuss their significance for variable selection in the model.

## Correlation Coefficients
- Compute correlation coefficients to understand relationships between variables. Discuss their importance for variable selection in the model.

## Variable Selection Using Hellwig's Method
- Apply Hellwig's method to identify the best set of explanatory variables.

## Analysis in Different Groups
Perform the above analysis for three groups: all districts, urban districts, and rural districts. Compare results across these groups.

### Handling Outliers:
Consider two scenarios for relationship analysis: including all data and excluding outliers.

### Conclusions:
Summarize the findings regarding the suitability of selected variables for model construction. Discuss whether any variables should be removed based on the analysis results.

# Project 5 Second Stage of Preliminary Data Analysis for Multiple Regression

## Outlier Analysis
1. Conduct analysis for outliers, leverage points, and influential observations using metrics such as Cook's distance, DFFITS, and DFBETA. Consider removing highly atypical observations. Compare results with Project 4.

## Variable Selection Using VIF
2. Utilize Variance Inflation Factor (VIF) to analyze the selection of explanatory variables.

## Stepwise Regression Analysis
3. Perform stepwise regression analysis (based on information criteria and F-statistics) to select explanatory variables for the model.

## Final Selection of Observations and Variables
4. Based on previous analyses, propose the final set of observations and explanatory variables.

## Model Assumptions Verification
5. Verify Gauss-Markov assumptions and assess model correctness for selected variables:
   a. Heteroskedasticity
   b. Autocorrelation of residuals
   c. Linearity of the model
   d. Normality of residuals

6. Propose solutions if Gauss-Markov assumptions are not met (e.g., variable transformation/modification).

## Analysis Across Different Groups
Conduct analysis for three groups: all districts, urban districts, and rural districts. Compare results across these groups.

### Conclusions:
Summarize findings regarding the suitability of selected variables for model construction. Discuss whether any variables should be removed based on the analysis results.
