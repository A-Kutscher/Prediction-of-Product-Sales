<p align = "center"> 
  <img src = "https://github.com/A-Kutscher/Prediction-of-Product-Sales/assets/135680202/25c003d0-47e8-4887-bf4f-6de6064789eb">
</p>

# Sales Predictions Dataset

The "sales_predictions_2023.csv" file in this repository provides past sales data as well as forecasts for 2023. The CSV-formatted dataset can be utilized for tasks involving sales analysis and forecasting.

## Data Source
Big Mart Sales Prediction 
https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/

For this dataset, there were 8523 rows and 12 columns.

## Data Dictionary

The columns in the "sales_predictions_2023.csv" dataset are as follows:

![Data Disctionary for Big Mart Sales Project](https://github.com/A-Kutscher/Prediction-of-Product-Sales/assets/135680202/9bbab3c6-c509-4319-b09b-c55fd559a939)

## File Structure

The repository has the following structure:
```
- Prediction_of_Product_Sales_Amber_Kutscher.ipynb
- README.md
```

## To prepare this data, the data was cleaned, and the following processes were performed:

### Exploratory Data Analysis
    - During the exploratory data analysis, histograms and boxplots were visualized for each numeric datatype column. 
    - Countplots were visualized for the categorical columns (minus the Item_Identifier column). 
    - And a heatmap was visualized as well, which provided us with details showing the correlation between the numeric datatype columns.
    - These visuals gave a good baseline for all of the numeric and categorical columns for univariate EDA.
    
<p align = "center">
  <img src = "https://github.com/A-Kutscher/Prediction-of-Product-Sales/assets/135680202/81085ccf-dbb8-42ad-9b8c-50e14d80dda9)">
</p>

This countplot shows that Fruits and Vegetables, as well as Snack Foods are the Item_Type's that have the largest quantity amongst all Big Mart locations, whereas Breakfast items and Seafood item make up the smallest quantity amongst all Big Mart locations.

<p align = "center">
  <img src = "https://github.com/A-Kutscher/Prediction-of-Product-Sales/assets/135680202/b3a94116-f311-4234-b2ad-049ce2293483">
</p>

This heatmap further shows that the strongest positive correlation between features is:
- Between the 'Item_MRP' column and the 'Item_Outlet_Sales' column at 0.57 or 57%.
- With the 'Item_Weight' column and the 'Outlet_Establishment_Year' column following closely behind at 0.54 or 54%.
