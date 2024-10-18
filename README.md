## Overview
This project aims to develop a predictive model using R to estimate the caloric content of fast food items based on key nutritional factors. The goal is to provide valuable insights for athletes and health-conscious individuals to make better dietary decisions by predicting calorie values from easily accessible nutritional information.

## Features
- **Calorie Prediction Model**: Built using multiple regression techniques to estimate caloric content.
- **Data Preprocessing**: Handling missing values and scaling nutritional data for better model accuracy.
- **Model Evaluation**: Includes statistical tests for model validation and residual analysis.
- **R-Based Implementation**: The project uses R for data manipulation, visualization, and modeling.

## Data
The dataset used for this project contains various nutritional factors such as:
- Serving Size
- Total Fat
- Saturated Fat
- Trans Fat
- Sodium
- Carbohydrates
- Sugars
- Protein

The dataset has been cleaned to handle missing values (e.g., replacing missing Trans Fat values with the mean) and contains a total of 9 variables after preprocessing.

## Model Development
### Steps
1. **Data Exploration**: Initial analysis of data structure and missing values.
2. **Data Cleaning**: Imputation of missing values (e.g., `TransFat`).
3. **Feature Selection**: Stepwise regression was applied to select the most significant variables.
4. **Model Fitting**: Various linear models were tested, and insignificant variables were removed iteratively to improve model accuracy.
5. **Model Evaluation**: 
   - Leverage points analysis.
   - Cook’s distance for influential observations.
   - Variance Inflation Factor (VIF) for multicollinearity detection.
   - Residuals analysis using homoscedasticity tests and Shapiro-Wilk test for normality.

### Final Model
The final model predicts caloric content using the following variables:
- **TotalFat**
- **TransFat**
- **Carbs**
- **Protein**

```r
model <- lm(Calories ~ TotalFat + TransFat + Carbs + Protein, data = calories)
