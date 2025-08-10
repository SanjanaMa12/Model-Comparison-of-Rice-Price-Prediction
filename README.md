# Model-Comparison-of-Rice-Price-Prediction
This project compares two statistical models(**Linear Regression** and **Ridge Regression**)for predicting rice prices in Sri Lanka using historical economic and agricultural data.

# Project Objective
The main goal of this project is to:
  Analyze the relationship between rice price and various economic/agricultural factors.
  Compare the performance of Linear Regression and Ridge Regression models.
  Understand the impact of multicollinearity on model stability.


# Dataset Description
 **Target Variable:** `price` (rice price)
 
 **Predictors:**  
   Producer prices from Anuradhapura, Kurunegala, Polonnaruwa  
   Agricultural production  
   Fuel price  
   Exchange rate  
   Monetary indicators (`m0`, `m1`, `m2`, `m2b`)

# Tools Used

**Google Colab** for analysis

 **Python Libraries:**
   `pandas`, `numpy`, `matplotlib`, `seaborn`
   `sklearn.linear_model`, `statsmodels`

# Modeling Approach
1. **Linear Regression**
2. **Ridge Regression (alpha = 1.0)**

# Visualizations

1.Correlation Heatmap
  Showed strong relationships between several features (e.g., monetary variables and producer prices).

2.VIF Plot
  Revealed high multicollinearity (especially among monetary variables).
  Justifies the use of Ridge Regression to stabilize the model.

3.Residual Analysis
  Residuals were randomly scattered, supporting assumptions of linearity.
  Slight spread in residuals suggests minor variance inconsistency.

# Histogram & Q-Q Plot of Residuals
  Residuals were close to normally distributed.
  Confirms model assumptions are mostly met.

# Actual vs. Predicted Prices
  Both models closely predicted rice prices.
  Very small difference between Ridge and Linear models.

# Coefficient Comparison Plot
  Ridge Regression slightly reduced coefficient sizes.
  Helps prevent overfitting in presence of multicollinearity.


# Model Performance

| Model              | Mean Squared Error (MSE) | R² Score |
|-------------------|--------------------------|----------|
| Linear Regression | 13.97                    | 0.99075  |
| Ridge Regression  | 13.97                    | 0.99075  |

**Conclusion:** 
Both models performed almost equally well. Ridge Regression improved model stability but had a minimal effect on accuracy due to the default alpha (1.0). A larger alpha could increase its regularization effect.
This project shows that:
  **Both models accurately predict rice prices.**
  
  **Multicollinearity is present**, but Ridge Regression helps reduce its effect.
  
    Model assumptions are generally satisfied.
    This approach could support future price forecasting or policymaking.

    
    (Linear Regression is not suitable for this dataset due to the presence of multicollinearity among the predictor variables, which can lead to unstable coefficient estimates and reduced predictive         reliability. Ridge Regression improved model stability by reducing the impact of highly correlated features, but further optimization can be achieved by using Lasso Regression. Lasso not only handles multicollinearity but also performs feature selection by shrinking some coefficients to zero, which can simplify the model and potentially improve predictive accuracy. Therefore, for more reliable and     interpretable predictions of rice prices, Lasso Regression is recommended over simple Linear Regression.)



