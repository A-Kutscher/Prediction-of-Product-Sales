<p align="center"> 
  <img src="https://github.com/A-Kutscher/Prediction-of-Product-Sales/assets/135680202/25c003d0-47e8-4887-bf4f-6de6064789eb">
</p>

# **Sales Predictions Dataset**
Author: Amber Kutscher

## **BUSINESS PROBLEM**

The "sales_predictions_2023.csv" file in this repository provides past sales data as well as forecasts for 2023. The CSV-formatted dataset can be utilized for tasks involving sales analysis and forecasting.

For this dataset, there were 8523 rows and 12 columns, respresenting 1559 items spread across 10 Big Mart locations. Using this data, Big Mart hopes to gain insight into what their 2023 forecasted sales are, as well as aid them in determining the items that bring in the most revenue.

## **DATA**

- **Data Source**

    [DataHack Analytics Vidhya - Big Mart Sales III](https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/)

- **Data Dictionary**

    The columns in the "sales_predictions_2023.csv" dataset are as follows:

    ![Data Dictionary for Big Mart Sales Project](https://github.com/A-Kutscher/Prediction-of-Product-Sales/assets/135680202/9bbab3c6-c509-4319-b09b-c55fd559a939)

- **File Structure**

  The repository has the following structure:
  ```
  - Data
  - Images
  - best-models.joblib
  - Explaining Models with Shap.ipynb
  - Prediction_of_Product_Sales_Amber_Kutscher.ipynb
  - Project 1 - Revisted__Amber_Kutscher.ipynb
  - README.md
  ```

  <center>We will be following the CRISP-DM workflow for our analysis.  

  <p align = "center"> 
  <img src="https://raw.githubusercontent.com/coding-dojo-data-science/Example-Project-Analyzing-Ames-Housing/main/Images/CRISP-DM.png" width=600px> </p>


  <p align = "center"> <a href="https://www.datascience-pm.com/crisp-dm-2">Image Source</a></center> </p>

## **METHODS**

1. Data Cleaning:
 Organize and clean sales data by removing duplicates, handling missing values, and addressing outliers for accurate analysis.

2. Exploratory Data Analysis (EDA):
 Explore the data to understand patterns and relationships between variables. Perform univariate, bivariate, and multivariate analysis to gain insights into sales trends and influencing factors.

3. Regression Models:
 Select relevant features that influence sales and choose an appropriate regression model (e.g., multiple linear regression) based on data characteristics. Evaluate the model's performance using metrics like Root Mean Squared Error (RMSE) and R-Squared (R^2 or R2) to ensure accurate predictions.

 By following these steps, we can calculate the anticipated 2023 sales based on historical data and identified relationships between various factors influencing sales.

## **RESULTS**

### -Exploratory Data Analysis (EDA)-
- During the exploratory data analysis, histograms and boxplots were visualized for each numeric datatype column.
- Countplots were visualized for the categorical columns (minus the Item_Identifier column).
- And a heatmap was visualized as well, which provided us with details showing the correlation between the numeric datatype columns.
- These visuals gave a good baseline for all of the numeric and categorical columns for univariate EDA.

> Visualization 1: *Frequency of Item_Type*
<p align="center">
<img src="https://github.com/A-Kutscher/Prediction-of-Product-Sales/assets/135680202/81085ccf-dbb8-42ad-9b8c-50e14d80dda9)">
</p>

The countplot above shows that Fruits and Vegetables, as well as Snack Foods are the Item_Type's that make up the largest quantity amongst all Big Mart locations, whereas Breakfast items and Seafood items make up the smallest quantity amongst all Big Mart locations.

> Visualization 2: *Correlations*
<p align="center">
<img src="https://github.com/A-Kutscher/Prediction-of-Product-Sales/assets/135680202/b3a94116-f311-4234-b2ad-049ce2293483">
</p>

The heatmap included above further shows that the strongest positive correlation between features is:
- Between the 'Item_MRP' column and the 'Item_Outlet_Sales' column at 0.57 or 57%.
- Closely followed by the 'Item_Weight' column and the 'Outlet_Establishment_Year' column at 0.54 or 54%.

## **MODEL**

### Final Model Description:

The final model selected for this analysis is the Linear Regression Model. It was chosen due to its ability to strike a better balance between overfitting and underfitting compared to the other model options.

### Most Important Metrics:

The key metrics for evaluating the final model's performance are as follows:
- R-squared (R^2) on Training Data: 0.56
- Root Mean Square Error (RMSE) on Training Data: 1139.12
- R-squared (R^2) on Test Data: 0.57
- Root Mean Square Error (RMSE) on Test Data: 1092.76

### Model's Solution to the Business Problem:

The Linear Regression Model demonstrates reasonable generalization to new data, explaining approximately 57% of the target variable's variation. Despite some error, its predictions are consistent and reliable, supporting data-driven decisions for optimizing processes and resource allocation. While room for improvement exists, the model effectively addresses the business problem, providing valuable insights for informed decision-making. Exploring alternative models or enhancing the existing one can further enhance its performance.

## **RECOMMENDATIONS**

To ensure accurate and reliable forecasts, we recommend exploring a range of predictive models. While the linear regression model shows reasonable performance, trying alternative models can unveil implicit patterns for more precise predictions. A comparative approach with multiple models will help us find the best-fit solution, considering data characteristics and the business problem. By leveraging various algorithms, we can enhance accuracy and gain deeper insights. Ultimately, model variation improves robustness and aids in better decision-making for Big Mart.

## **LIMITATIONS & NEXT STEPS**

1. Limitations: The current model struggles with complex patterns. Trying more advanced models could help improve data by creating new features.
2. Next Steps: Experiment with and fine-tune various models, use combination methods, and gather more relevant data. Collaborate with our stakeholders for better insights. Monitor model performance and update it with new data as needed.

## **IMPORTANCES AND COEFFICIENTS**

Linear Regression: *Coefficients*
The top 3 most impactful features are:
1. Outlet_Type_Grocery Store (-1,573.87):
    - This feature has the most significant impact on the target variable.
    - A store classified as "Grocery Store" has a substantial negative effect on the target variable. In this context, it indicates that items sold in grocery stores tend to have much lower sales compared to other types of outlets.

2. Outlet_Type_Supermarket Type3 (1,490.95):
    - Supermarket Type3 is the second most impactful feature with a large positive coefficient.
    - Items sold in "Supermarket Type3" outlets have a substantial positive effect on sales, suggesting that this type of outlet tends to have significantly higher sales compared to other outlet types.

3. Item_Visibility (-316.43):
    - The third most impactful feature is "Item_Visibility."
    - This feature has a significant negative impact on sales. It indicates that as the visibility of an item in a store decreases, the sales tend to increase. This might be counterintuitive, and further analysis is needed to understand why this is the case. It could be due to outliers or specific patterns in the data.

![Linear Regression: Coefficients](Images/lin_reg_coeffs.png)

RandomForestRegressor: *Importances*
The top 5 most important features are:
1. Item_MRP (0.45):
    - This feature has the highest importance score, indicating that it has the most significant impact on the target variable. Item Maximum Retails Price (MRP) is a crucial factor in determining sales.

2. Outlet_Type_Grocery Store (0.19):
    - The type of outlet being a "Grocery Store" is the second most important feature. It suggests that this type of outlet significantly affects sales, likely indicating lower sales compared to other outlet types.

3. Item_Visibility (0.11):
    - Item visibility plays a substantial role in sales. However, it has a negative impact, suggesting that as item visibility increases, sales tend to decrease.

4. Outlet_Type_Supermarket Type3 (0.07):
    - The presence of "Supermarket Type3" is the fourth most important feature. It has a positive impact on sales, indicating higher sales in this type of outlet.

5. Item_Weight (0.05):
    - Item weight is the fifth most important feature, but its impact is relatively smaller compared to the top features. It suggests that the weight of items may have some influence on sales.

![RandomForestRegressor: Importances](Images/randomforest_coeffs.png)

SHAP Bar Plot
- The most important features according to SHAP are:
  - Item_MRP
  - Outlet_Type_Grocery Store
  - Outlet_Type_Supermarket Type3
  - Item_Visibility
  - Item_Weight

- In comparison, the 5 most important features from our original model are:
  - Item_MRP
  - Outlet_Type_Grocery Store
  - Item_Visibility
  - Outlet_Type_Supermarket Type3
  - Item_Weight

As can be seen, the most important features according to both models are the same, however the order is a bit different.

![SHAP Bar Plot](Images/shap_bar_plot.png)

SHAP Dot Plot
As per the SHAP ummary - Dot Plot, the 3 most important features are:
1. "Item_MRP"
    - When the listed price (Item MRP) of a product increases, the model predicts higher overall item outlet sales. This implies that as the price of a product goes up, the model anticipates an increase in the number of units sold for that product.
2. "Outlet_Type_Grocery Store"
    - Products sold in grocery stores have a smaller impact on item outlet sales compared to those sold in supermarkets. In other words, the type of outlet significantly influences the model's predictions, and grocery stores tend to have a lower effect on sales.
3. "Outlet_Type_Supermarket Type3"
    - Among the three types of supermarkets, Supermarket Type3 has the most substantial financial impact on item outlet sales, according to the model. This suggests that Supermarket Type3 stores may be the largest among the three and have the highest influence on the predicted sales of products.

![SHAP Dot Plot](Images/shap_dot_plot.png)