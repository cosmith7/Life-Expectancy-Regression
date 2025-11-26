# Life Expectancy Regression Model

**Course:** Machine Learning for the Life Sciences (BSCI238I)  
**Author:** Catherine Smith  
**Semester:** Fall 2025  

---

## Overview

This project develops a machine-learning regression model that predicts **life expectancy** using global health indicators from the **World Health Organization (WHO)** and **United Nations (UN)**.

The model demonstrates:

- Data cleaning and preprocessing  
- Exploratory data analysis (EDA)  
- Correlation-based feature selection  
- Standardization  
- Linear regression using stochastic gradient descent (SGD)  
- Model evaluation with R², MSE, and residual analysis  
- Interpretation of standardized coefficients  

---

## Repository Structure

```text
life-expectancy-regression/
│
├── README.md
├── life_expectancy_regression.ipynb
├── Life Expectancy Data.csv
│
├── results/
│   ├── correlation_matrix.png
│   ├── learning_curve.png
│   └── residual_plot.png
```
## Repository Structure
To run the project, the following Python libraries are required:
* ```pandas```
* ```numpy```
* ```matplotlib```
* ```seaborn```
* ```scikit-learn```

## Methodology
Data Preparation
- Removed missing values
- Selected three strongest predictors based on correlation and interpretability: Adult Mortality, Schooling, Income Composition of Resources

Train/Val/Test Split
- 70% training
- 15% validation
- 15% testing

Feature Scaling
- Standardized predictors using StandardScaler
- Ensures stable gradient descent and comparable coefficient magnitudes

Model
- SGDRegressor (linear regression via stochastic gradient descent)
- Loss: Mean Squared Error
- Learning rate: constant (0.01)

Evaluation Metrics
- Mean Squared Error (MSE)
- R² Score
- Residual analysis

## Key Results

Validation Performance
- Strong correlation between predictions and true values
- Minimal overfitting across epochs

Test Performance
- R² ≈ 0.76
- Model explains ~76% of variation in life expectancy

Coefficient Interpretation (Standardized Space)
- Adult Mortality	-> Strong negative predictor
- Schooling	-> Positive predictor
- Income Composition of Resources	-> Positive predictor

Conclusion
Countries with:
- higher adult mortality tend to have lower life expectancy
- higher educational attainment tend to have longer life expectancy
- greater economic development also see increased life expectancy

## Visualizations

Saved in the results/ folder:
- correlation_matrix.png
- learning_curve.png
- residual_plot.png

## License

This project is for educational purposes as part of the UMD Machine Learning for the Life Sciences course (BSCI238I).
