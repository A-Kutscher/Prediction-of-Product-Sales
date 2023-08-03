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

----- EXPLAIN PROJECT STEPS AND RESULTS IN SIMPLE TERMS

## **RESULTS**

- To prepare this data, the data was cleaned in order to fix and/or remove any duplicate, inconsistent, or missing values.
- To better understand each data type, the cleaned data was then explored through Exploratory Data Analysis in order to visualize each columns data type, categories, and overall count.

### -Exploratory Data Analysis-
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

--------------Describe final model, report most important metrics, refer to metrics to describe how well the model would solve the business problem.

## **RECOMMENDATIONS**

-----------------Insert recommendations here.

## **LIMITATIONS & NEXT STEPS**

----------------analysis here
