# Model Comparison

## Overview

Three simple linear regression models and one multiple regression model were developed to identify the factors associated with monthly sales across retail stores. The dependent variable for all models was **Monthly Sales**.

---

## Model Comparison

| Model                   | Dependent Variable | Independent Variable(s)                                                                    | R²                  | Significant Variables                                          | Business Usefulness                                                                                                        | Limitations                                                                                                                                      |
| ----------------------- | ------------------ | ------------------------------------------------------------------------------------------ | ------------------- | -------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Simple Regression 1** | Monthly Sales      | Marketing Spend                                                                            | **0.1672 (16.72%)** | Marketing Spend (p < 0.001)                                    | Shows that higher marketing spend is associated with increased sales. Useful for evaluating marketing investment.          | Explains only a small portion of sales variation and ignores other influencing factors.                                                          |
| **Simple Regression 2** | Monthly Sales      | Footfall                                                                                   | **0.7363 (73.63%)** | Footfall (p < 0.001)                                           | Strong predictor of monthly sales. Useful for understanding the impact of customer traffic on store performance.           | Does not consider marketing, inventory, or regional differences.                                                                                 |
| **Simple Regression 3** | Monthly Sales      | Inventory Availability (%)                                                                 | **0.0131 (1.31%)**  | Inventory Availability (p = 0.0406)                            | Shows a statistically significant positive relationship with sales.                                                        | Very low explanatory power when used alone.                                                                                                      |
| **Multiple Regression** | Monthly Sales      | Marketing Spend, Footfall, Inventory Availability, Region_North, Region_South, Region_East | **0.8074 (80.74%)** | Footfall, Marketing Spend, Inventory Availability, Region_East | Provides the best explanation of monthly sales and allows leadership to evaluate multiple business drivers simultaneously. | Does not include other possible influences such as pricing strategy, promotions, customer demographics, economic conditions, or seasonal trends. |

---

## Comparison of R-Squared Values

The simple regression model using **Marketing Spend** explained **16.72%** of the variation in monthly sales. The **Footfall** model performed substantially better, explaining **73.63%** of the variation, indicating that customer traffic is a major driver of sales. The **Inventory Availability** model explained only **1.31%** of the variation despite being statistically significant.

The **Multiple Regression Model** achieved the highest explanatory power with an **R² of 80.74%**, demonstrating that combining several business factors produces a much stronger predictive model than relying on any single variable.

---

## Significant Variables

The following variables were statistically significant (p < 0.05):

* Marketing Spend
* Footfall
* Inventory Availability
* Region_East (compared to the West reference region)

The following variables were not statistically significant:

* Region_North
* Region_South

These regional variables do not appear to have an independent effect on monthly sales after controlling for the other predictors.

---

## Business Usefulness

The multiple regression model provides the greatest value for decision-making because it evaluates several operational and marketing factors simultaneously. The analysis indicates that:

* Increasing customer footfall is the strongest driver of higher monthly sales.
* Marketing spend has a positive and significant impact on sales.
* Maintaining high inventory availability supports improved sales performance.
* Stores located in the East region perform significantly differently from those in the West region, suggesting that region-specific strategies may be beneficial.

---

## Limitations

Although the multiple regression model performs well, it does not capture every factor influencing monthly sales. Variables such as promotional campaigns, pricing changes, customer demographics, local competition, economic conditions, and seasonal demand were not included. Additionally, regression analysis identifies statistical associations and should not be interpreted as proof of causation.
