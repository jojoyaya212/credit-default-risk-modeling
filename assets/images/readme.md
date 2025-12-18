# Credit Default Risk Modeling

This project presents an **end-to-end credit default risk analysis and modeling pipeline**, focusing on understanding borrower behavior, handling real-world financial data challenges, and building an interpretable classification model for default prediction.

The workflow emphasizes **exploratory data analysis, feature transformation, and model interpretability**, rather than black-box performance.

---

## Project Overview

The objective of this project is to model the probability that a borrower will default, using demographic and financial attributes.  
The analysis mirrors practical credit risk development by prioritizing:

- Data diagnostics before modeling
- Economic interpretation of variables
- Robust handling of skewness and outliers
- Transparent classification decisions

---

## Dataset Description

- Credit card client default dataset
- Binary target variable:
  - `1` = Default
  - `0` = Non-default
- Strong class imbalance, reflecting real consumer credit portfolios

---

## Exploratory Data Analysis

### Distribution of Default

The target variable is highly imbalanced, with non-default observations dominating the sample.  
This motivates careful evaluation beyond raw accuracy.

![Distribution of Default](assets/images/distribution_of_default.png)

---

### Distribution of Outliers

Key numerical variables exhibit heavy skewness and extreme values.  
Rather than removing them blindly, the analysis treats outliers as **potential risk signals**.

![Distribution of Outliers](assets/images/distribution_of_outliers.png)

---

### Variable Descriptions

Categorical variables are decoded and mapped to meaningful economic interpretations, preserving ordinal information where applicable.

![Variable Descriptions](assets/images/variable_descriptions.png)

---

## Feature Engineering

- Numerical features are scaled using Min–Max normalization
- Skewed variables are transformed to improve stability
- Outliers are retained and analyzed rather than removed
- Highly correlated features are addressed using dimensionality reduction

---

## Modeling Approach

- Logistic Regression with regularization
- Class imbalance handled through balanced class weights
- Emphasis on probability estimation and interpretability

---

## Model Interpretation

### Feature Importance

Model coefficients highlight economically intuitive drivers of default risk:
- Repayment delay indicators
- Credit utilization behavior
- Payment consistency

![Feature Importance](assets/images/feature_importance.png)

---

## Model Evaluation

### Confusion Matrix

The confusion matrix illustrates the trade-off between identifying defaulters and avoiding false positives, a key consideration in credit decision-making.

![Confusion Matrix](assets/images/confusion_matrix.png)

---

## Key Insights

- Default risk is strongly driven by recent repayment behavior
- Outliers contain meaningful risk information
- Interpretability is critical for credit modeling
- Threshold choice should align with business costs, not accuracy alone

---

## Disclaimer

This project is for **research and demonstration purposes only**.

- Results depend on data quality and modeling assumptions
- The model is not intended for real-world lending decisions
- Outputs do not constitute financial or credit advice

---

## Author

**Ke Zhang**  
Credit Risk Modeling · Financial Analytics
