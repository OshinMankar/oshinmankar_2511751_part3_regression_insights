# Residual Analysis

## Predicted Sales and Residuals

Predicted monthly sales were calculated using the final multiple regression model. Residuals were then computed using the following formula:

**Residual = Actual Monthly Sales − Predicted Monthly Sales**

A positive residual indicates that the actual monthly sales exceeded the model's prediction (under-prediction), while a negative residual indicates that the actual monthly sales were lower than the predicted value (over-prediction).

---

## Top 5 Records with the Largest Positive Residuals

| Rank | Store ID |   Residual |
| ---- | -------- | ---------: |
| 1    | STR-1028 | 111,695.73 |
| 2    | STR-1026 | 102,501.81 |
| 3    | STR-1051 |  97,177.57 |
| 4    | STR-1032 |  96,450.79 |
| 5    | STR-1064 |  95,251.58 |

### Business Interpretation

These stores generated significantly higher monthly sales than predicted by the regression model. This suggests that they benefited from factors not included in the analysis, such as effective local promotions, strong customer loyalty, favorable store locations, exceptional customer service, or seasonal demand. The model under-predicted sales for these stores, indicating that additional business variables could improve prediction accuracy.

---

## Top 5 Records with the Largest Negative Residuals

| Rank | Store ID |    Residual |
| ---- | -------- | ----------: |
| 1    | STR-1017 | -155,312.65 |
| 2    | STR-1012 | -134,687.08 |
| 3    | STR-1009 | -122,981.86 |
| 4    | STR-1001 | -117,850.30 |
| 5    | STR-1023 | -111,704.58 |

### Business Interpretation

These stores recorded substantially lower monthly sales than predicted by the model. The over-prediction may be due to operational challenges, lower customer demand, increased local competition, temporary disruptions, or other external factors that were not captured by the available variables. These stores may require further investigation to identify the reasons for their lower-than-expected performance.

---

## Model Performance Assessment

The final multiple regression model achieved an **R² of 80.74%**, indicating that it explains a large proportion of the variation in monthly sales and provides strong predictive performance. However, the presence of large positive and negative residuals for a small number of stores shows that the model cannot capture every factor affecting sales.

Overall, the model appears to perform well across most stores, but it **under-predicts** sales for some high-performing stores and **over-predicts** sales for certain lower-performing stores. These prediction errors suggest that additional variables—such as promotional campaigns, pricing strategies, customer demographics, competitor activity, local economic conditions, and seasonal effects—could further improve the model's accuracy.

Residual analysis confirms that while the regression model is suitable for identifying the major drivers of monthly sales, it should be used as a decision-support tool rather than as a perfect predictor of individual store performance.
