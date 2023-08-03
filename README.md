<p align = "center"> 
  <img src = "https://github.com/A-Kutscher/Prediction-of-Product-Sales/assets/135680202/25c003d0-47e8-4887-bf4f-6de6064789eb">
</p>

# **Sales Predictions Dataset**
Author: Amber Kutscher

## **BUSINESS PROBLEM**

The "sales_predictions_2023.csv" file in this repository provides past sales data as well as forecasts for 2023. The CSV-formatted dataset can be utilized for tasks involving sales analysis and forecasting.

For this dataset, there were 8523 rows and 12 columns, respresenting 1559 items spread across 10 Big Mart locations. Using this data, Big Mart hopes to gain insight into what their 2023 forecasted sales are, as well as aid them in determining the items that bring in the most revenue.

## **DATA**

- **Data Source**

    https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/

 - **Data Disctionary**
  
    The columns in the "sales_predictions_2023.csv" dataset are as follows:
  
    ![Data Disctionary for Big Mart Sales Project](https://github.com/A-Kutscher/Prediction-of-Product-Sales/assets/135680202/9bbab3c6-c509-4319-b09b-c55fd559a939)

- **File Structure**

  The repository has the following structure:
  ```
  - Prediction_of_Product_Sales_Amber_Kutscher.ipynb
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
<p align = "center">
  <img src = "https://github.com/A-Kutscher/Prediction-of-Product-Sales/assets/135680202/81085ccf-dbb8-42ad-9b8c-50e14d80dda9)">
</p>

  The countplot above shows that Fruits and Vegetables, as well as Snack Foods are the Item_Type's that make up the largest quantity amongst all Big Mart locations, whereas Breakfast items and Seafood items make up the smallest quantity amongst all Big Mart locations.

> Visualization 2: *Correlations* 
<p align = "center">
  <img src = "https://github.com/A-Kutscher/Prediction-of-Product-Sales/assets/135680202/b3a94116-f311-4234-b2ad-049ce2293483">
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
