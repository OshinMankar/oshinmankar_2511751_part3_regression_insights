# Retail Sales Regression Analysis

## Project Overview

This project uses regression analysis to identify the factors most strongly associated with monthly sales across retail stores. The objective is to help the leadership team understand which business variables influence sales performance and provide data-driven recommendations for improving business outcomes.

Both simple linear regression and multiple linear regression models were developed using Microsoft Excel to evaluate the impact of marketing spend, customer footfall, inventory availability, and regional differences on monthly sales.

---

## Business Problem

The retail leadership team wants to understand the key drivers of monthly sales in order to make informed decisions regarding:

* Marketing investment
* Inventory management
* Regional performance
* Resource allocation
* Store performance improvement

The analysis aims to identify which factors have the strongest relationship with monthly sales and support evidence-based business recommendations.

---

## Dataset Description

The dataset contains monthly store-level performance data with the following variables:

* Store ID
* Month
* Region
* Store Type
* Marketing Spend
* Footfall
* Average Discount Percentage
* Staff Count
* Inventory Availability (%)
* Competitor Distance (km)
* Holiday Flag
* Customer Rating
* Monthly Sales
* Monthly Profit

**Dependent Variable**

* Monthly Sales

**Independent Variables**

* Marketing Spend
* Footfall
* Inventory Availability (%)
* Average Discount Percentage
* Customer Rating
* Region (Dummy Variables)

---

## Data Preparation

The dataset was cleaned and prepared before performing regression analysis.

Cleaning activities included:

* Checking for duplicate records
* Handling missing values
* Standardizing categorical values
* Removing extra spaces and formatting inconsistencies
* Creating dummy variables for the Region variable
* Preserving the original dataset while creating cleaned and prepared data sheets

---

## Regression Models Developed

### Simple Regression Models

The following simple regression models were created:

1. Monthly Sales vs Marketing Spend
2. Monthly Sales vs Footfall
3. Monthly Sales vs Average Discount Percentage
4. Monthly Sales vs Inventory Availability
5. Monthly Sales vs Customer Rating

Each model was evaluated using:

* Regression equation
* R-squared
* Coefficient
* P-value
* Business interpretation

---

### Multiple Regression Model

The final regression model included:

* Marketing Spend
* Footfall
* Inventory Availability (%)
* Region_North
* Region_South
* Region_East

Reference Category:

* West Region

The multiple regression model achieved an **R² of 80.74%**, indicating strong explanatory power.

---

## Key Findings

The analysis identified several important business insights:

* **Footfall** was the strongest predictor of monthly sales.
* **Marketing Spend** showed a positive and statistically significant relationship with sales.
* **Inventory Availability** positively influenced sales performance.
* Stores in the **East region** performed significantly differently from the West region after controlling for other variables.
* **Average Discount Percentage** and **Customer Rating** were not strong standalone predictors of monthly sales.

---

## Residual Analysis

Predicted monthly sales and residuals were calculated using the final multiple regression model.

Residual analysis identified stores where:

* Actual sales exceeded model predictions (under-prediction)
* Actual sales fell below model predictions (over-prediction)

This analysis highlighted stores that may require additional investigation and suggested that factors outside the regression model also influence sales performance.

---

## Business Recommendations

Based on the regression analysis, leadership should focus on:

* Increasing customer footfall through targeted marketing and customer engagement initiatives.
* Maintaining effective marketing investment to support sales growth.
* Improving inventory availability to reduce stockouts and maximize sales opportunities.
* Reviewing operational performance in the East region to identify opportunities for improvement.

Variables such as Average Discount Percentage, Customer Rating, Region_North, and Region_South should be interpreted cautiously because they did not consistently demonstrate statistically significant relationships with monthly sales.

---

## Tools Used

* Microsoft Excel
* Excel Data Analysis ToolPak
* Regression Analysis
* Dummy Variable Encoding
* Residual Analysis

---

## Project Structure

```
analysis/
│── regression_workbook.xlsx
│── model_comparison.md
│── residual_analysis.md

outputs/
│── regression_summary.xlsx
│── model_equations.md
│── final_recommendation.md

screenshots/
│── simple_regression_output.png
│── multiple_regression_output.png
│── model_comparison_preview.png
│── residuals_preview.png

README.md
```

---

## Limitations

The regression model identifies statistical associations but does not establish causal relationships. Variables such as promotional campaigns, seasonal demand, pricing strategies, customer demographics, local competition, and economic conditions were not included in the analysis and may also influence monthly sales. Future analyses could incorporate these variables to improve predictive accuracy.

---

## Conclusion

The multiple regression model was selected as the final model because it provided the highest explanatory power (**R² = 80.74%**) and offered the most comprehensive understanding of the factors influencing monthly sales. The findings support data-driven decision-making by highlighting customer footfall, marketing spend, and inventory availability as the primary drivers of sales performance while identifying regional differences that warrant further business investigation.
