# Rent Control Home Price Estimator: Iowa Policy Model

## Project Overview

This project aims to create a **home price estimator model** to support rent control policy development in Iowa. The goal is to provide policymakers with an **accurate, interpretable, and cost-effective** model that can help set fair and balanced rental prices, benefiting both tenants and landlords. The model will help bridge the gap between affordable housing and reasonable profits for landlords, ensuring that rent control policies are based on real market data rather than speculation.

### What if Public Officials Had the Power to Estimate Home Values?

**Answer:** By using a home price estimator model, public officials can effectively bridge the gap between **too high** and **too low** rent controls.

- **Renters** pay fair rent that aligns with market conditions.
- **Landlords** benefit from **lower tenant turnover**, as rental prices stay competitive and fair.
- The model helps address the **housing crisis** by ensuring that rent control policies are grounded in data and lead to balanced, sustainable pricing.

This model brings clarity and transparency to the rent control debate, providing a solution that benefits all stakeholders—tenants, landlords, and citizens.

## Problem Statement

In Iowa, rent control is a contentious issue. There is currently no rent control policy in place, but the debate centers around finding the right balance. A rent control floor that is too low can discourage housing supply and maintenance, while one that is too high can leave housing unaffordable for tenants. An **accurate home price estimator** can ground policies on **hard data** and create a transparent, effective model that appeals to voters, ultimately facilitating a rent control measure on the ballot.

## Project Objectives

- **Accurate Model**: Create a home price estimator that predicts housing prices based on various factors, with model accuracy measured by metrics like RMSE, R2 score, and MAE.
- **Interpretable Model**: Ensure the model is transparent and can be easily understood by policymakers, voters, and stakeholders, fostering trust and confidence.
- **Cost-Effective**: Design a model that relies on as little amount of features to implement, allowing voters to see the benefits without a heavy financial burden on the state.

## Dataset Overview

The dataset used for this project contains over 80 housing-related features from kaggle. Below you will find the data dictionary for the features used in my selected model.


| Feature               | Type        | Dataset          | Description                                                                                               |
|-----------------------|-------------|------------------|-----------------------------------------------------------------------------------------------------------|
| overall_qual          | object     | <train_cleaned.csv>    | Overall quality rating of the house, typically on a scale from 1 (poor) to 10 (excellent).               |
| age                   | int         | <train_cleaned.csv>    | The age of the house (in years) since it was built till it was sold.                                                      |
| total_bath            | float         | <train_cleaned.csv>    | The total number of bathrooms in the house, including full and half bathrooms.                            |
| total_sf              | float       | <train_cleaned.csv>    | The total square footage of the house.                                                                   |
| totrms_abvgrd         | int         | <train_cleaned.csv>    | The total number of rooms above ground (does not include basement rooms).                                |
| remodel_age           | int         | <train_cleaned.csv>    | Sale date minus remodel year.                                          |
| fireplaces            | int         | <train_cleaned.csv>    | The number of fireplaces in the house.                                                                   |
| neighborhood_<name>    | object      | <train_cleaned.csv>    | Binary indicator for the presence of the home in a specific neighborhood (e.g., 1 if in neighborhood, 0 if not). |
| exter_qual            | object     | <train_cleaned.csv>    | The quality of the house's exterior, rated as "Ex" (excellent), "Gd" (good), "TA" (typical/average), "Fa" (fair), "Po" (poor). |
| bsmt_qual             | object     | <train_cleaned.csv>    | The quality of the basement, rated as "Ex" (excellent), "Gd" (good), "TA" (typical/average), "Fa" (fair), "Po" (poor). |
| sale_type             | object | <train_cleaned.csv>    | The type of sale, such as "WD" (Warranty Deed), "New" (New Construction), "COD" (Court Officer Deed), etc. |
| functional            | object     | <train_cleaned.csv>    | The functionality of the house’s design, rated as "Typ" (typical), "Min1" (minor issues), "Min2" (major issues), "Maj1" (major issues), "Maj2" (more severe issues), or "Sev" (severe issues). |
| exterior_1st          | object | <train_cleaned.csv>    | The primary exterior material of the house, such as "Vinyl", "Wood", "Cement", "Brick", etc.              |
| garage_finish         | object     | <train_cleaned.csv>    | The finish quality of the garage, rated as "Fin" (finished), "RFn" (rough-finished), or "Unf" (unfinished). |
| kitchen_qual          | object     | <train_cleaned.csv>    | The quality of the kitchen, rated as "Ex" (excellent), "Gd" (good), "TA" (typical/average), "Fa" (fair), or "Po" (poor). |



## Model Approach

1. **Exploratory Data Analysis (EDA)**:
   - Visualizations: Correlation maps, box plots for categorical variables, and bar charts.
   - Summary statistics to understand relationships between features and target prices.

2. **Model Training and Evaluation**:
   - We use regression models, including Linear Regression, Random Forest, and Gradient Boosting, to predict housing prices.
   - Model performance is evaluated using metrics like RMSE, R2 score, and MAE to ensure accuracy.

3. **Interpretability**:
   - Feature importance analysis to understand which features contribute most to price predictions.

4. **Visualization**:
   - **Correlation Heatmap**: Display the relationships between features and how they influence home prices.
   - **Boxplots and Bar Charts**: Visualize distribution of prices across different neighborhoods, and identify trends.
   - **Actual vs. Predicted Scatter Plot**: Compare predicted home prices to actual prices to visually assess the model's performance.
   - **Model Performance Metrics**: RMSE, R2, MAE values.

## Results

The final model provides highly accurate price predictions and demonstrates **high transparency** through visualizations and interpretability tools.

- **Key Metrics**:
  - RMSE: 26229.24420716645
  - R2 Score: 0.8842091294065451
  - MAE: 18230.364137750785

## Policy Implications

This model will directly support the development of a rent control policy in Iowa by providing **clear evidence** of fair home prices across various neighborhoods. By using this model, policymakers can implement a rent control measure that benefits both tenants and landlords, ensuring affordable housing without stifling development or investment.

## Conclusion

Our model is the most ideal tool to establish reasonable rent control thresholds in Iowa. It satisfies all the **successful metrics** for rent control policy development:

- **Interpretable**: The model provides transparency, allowing policymakers and voters to understand how it works and how it reaches its conclusions.
- **Accurate**: The model is built to predict housing prices with high accuracy, ensuring that rent control policies are grounded in real, market-driven data.
- **Cost-Effective**: The model is designed to be affordable to implement, making it a practical choice for policymakers looking to adopt rent control without significant financial burden.

With this model in place:

- **Renters** pay **fair rent** that is in line with market conditions.
- **Landlords** benefit from **lower tenant turnover**, as rental prices stay competitive and reasonable.

By leveraging this model, Iowa can implement a rent control policy that balances the needs of both tenants and landlords while addressing the broader housing crisis.

## Next Steps

1. **Model Improvement and Tuning**  
   - **Hyperparameter Tuning:** Continue experimenting with various machine learning algorithms such as XGBoost, Random Forest, or Gradient Boosting, and optimize their hyperparameters to improve model performance.
   - **Feature Selection:** Investigate the possibility of reducing the feature set through techniques like Recursive Feature Elimination (RFE) or feature importance methods to simplify the model while maintaining high accuracy.


2. **Model Evaluation and Comparison**  
   - **Test with Additional Datasets:** Test the model on new datasets or different splits to evaluate its robustness and ensure it can be generalized to real-world data.
   - **Metric Analysis:** Expand the evaluation of the model by using additional metrics like Precision, Recall, or F1-Score for better insights into prediction quality. 