# Uber vs Lyft Prediction

## Problem Statement:
Two car-hailing firms, **Uber** and **Lyft**, compete for customers and partners. Unlike public transportation, ride costs on Uber and Lyft are not constant. They vary based on factors such as **distance**, **weather conditions**, and the **source** and **destination** of the ride.

## Target Variable Selection:
The target variable, **classification**, was selected to determine the presence or absence of **Chronic Kidney Disease (CKD)**. This binary classification problem is relevant to the medical context, allowing us to measure predictive accuracy and clinical significance.

## Suitable Machine Learning Models:

### 1. **Multivariable Linear Regression**
   - Multiple linear regression estimates the relationship between two or more independent variables and one dependent variable. In this case, we have 21 independent variables and one target variable.
   - The formula for multiple linear regression is:
     \[
     y = \beta_0 + \beta_1 x_1 + \beta_2 x_2 + \dots + \beta_n x_n
     \]
     Where:
     - \( y \) is the target price (dependent variable)
     - \( x_1, x_2, \dots, x_n \) are the independent variables

### 2. **Support Vector Regression (SVR)**
   - SVR fits a hyperplane that covers the majority of data points, unlike linear regression, which fits a line minimizing the error between predicted and real values.
   - **SVR** can be computationally expensive, so only **10%** of the dataset was used for training.

### 3. **Random Forest Regressor**
   - Random Forest is a supervised learning algorithm that uses an ensemble method for regression.
   - Performance metrics include **Mean Squared Error (MSE)** and **\( R^2 \)**.
   - Random Forests perform well on large datasets and can model non-linear relationships between input features and the target variable, making it an ideal choice for this problem.
   - Model parameters used: `n_estimators = 500`, `random_state = 0`, `n_jobs = -1`

## Conclusion and Insights:
- **Uber** is generally **less expensive** than **Lyft** in Boston.
- **Uber** holds a larger market share in the city.
- In the **economical** category, **Lyft** is cheaper than **Uber**, while in the **luxury** segment, **Uber** tends to be less expensive.
- **Distance** and **weather conditions** have a significant impact on pricing.
- Among the models tested—**Support Vector Regression**, **Linear Regression**, and **Random Forest Regressor**—the **Random Forest Regressor** achieved the best accuracy score.
- This model can be used both as a **B2B** and **B2C** solution:
  - **B2B**: Ride-hailing companies like Uber and Lyft (or even new competitors) can use this model to analyze competitor pricing strategies.
  - **B2C**: Customers can use the model to find the most cost-effective ride option.
