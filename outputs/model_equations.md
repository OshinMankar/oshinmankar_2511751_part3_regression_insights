The categorical variables Region and Store Type were converted into dummy variables using one-hot encoding. For Region, West was selected as the reference category, so dummy variables were created for North, South, and East. For Store Type, Airport was selected as the reference category, and dummy variables were created for Mall, High Street, and Residential. One category from each variable was omitted to avoid the dummy variable trap, which causes perfect multicollinearity in regression models.

# Model Equations

## 1. Simple Regression Equations

### Model 1: Marketing Spend

**Equation**

[
560777.35 + 2.13 × Marketing Spend
]

**Coefficient Explanation**

* **Intercept (560,777.35):** Represents the estimated monthly sales when marketing spend is zero.
* **Marketing Spend (2.13):** A one-unit increase in marketing spend is associated with an average increase of approximately **2.13 units** in monthly sales. This indicates that higher marketing investment is generally associated with higher sales.

---

### Model 2: Footfall

**Equation**

[
446410.5829 + 35.3 × Footfall
]

**Coefficient Explanation**

* **Intercept (446,410.58):** Represents the estimated monthly sales when customer footfall is zero.
* **Footfall (35.68):** Each additional customer visiting the store is associated with an average increase of approximately **35.68 units** in monthly sales, making footfall a strong driver of sales performance.

---

### Model 3: Inventory Availability

**Equation**

[
484814.26 + 2217.83 × inventory_availability_pct
]

**Coefficient Explanation**

* **Intercept (484,814.26):** Represents the estimated monthly sales when inventory availability is zero.
* **Inventory Availability (2,217.83):** A one percentage-point increase in inventory availability is associated with an average increase of approximately **2,217.83 units** in monthly sales, indicating that maintaining product availability supports higher sales.

---

## 2. Multiple Regression Equation

The final multiple regression model combines several business factors to predict monthly sales.

**Equation**

[
Predicted Sales = 167465.0014−64890.8082(Region_North−88660.9736(Region_South−93638.3756(Region_East)+1.166639942(MarketingSpend)+33.97310595(Footfall)+2561.266053(Inventoy Availability)
]

---

## 3. Explanation of Each Coefficient

### Intercept

The intercept (**167,465.00**) represents the estimated monthly sales for a store in the **West region** (reference category) when all numerical variables are zero. Although this situation is unlikely in practice, it serves as the baseline for the model.

### Marketing Spend (+1.1666)

Marketing spend has a **positive relationship** with monthly sales. Increasing investment in marketing is associated with higher sales while keeping other factors constant.

### Footfall (+33.9731)

Footfall has the **strongest positive effect** on monthly sales. Every additional customer visiting the store is associated with an increase of approximately **33.97 units** in monthly sales, making customer traffic the most important driver in the model.

### Inventory Availability (+2561.27)

Inventory availability has a **positive relationship** with sales. Stores with higher product availability are expected to achieve higher monthly sales because customers are more likely to find the products they need.

### Region_North (-64,890.81)

Stores located in the North region are predicted to have lower monthly sales than stores in the West region after accounting for the other variables. However, this variable was **not statistically significant**, so the difference should be interpreted with caution.

### Region_South (-88,660.97)

Stores in the South region are estimated to have lower monthly sales than those in the West region. The result was only **marginally significant**, indicating that the difference is uncertain.

### Region_East (-93,638.38)

Stores in the East region are expected to have lower monthly sales than stores in the West region after controlling for marketing spend, footfall, and inventory availability. This variable was **statistically significant**, suggesting a meaningful regional difference.

---

## 4. Explanation of Dummy Variables

The variable **Region** is categorical and cannot be used directly in regression analysis. Therefore, it was converted into dummy variables.

| Region | Region_North | Region_South | Region_East |
| ------ | ------------ | ------------ | ----------- |
| North  | 1            | 0            | 0           |
| South  | 0            | 1            | 0           |
| East   | 0            | 0            | 1           |
| West   | 0            | 0            | 0           |

Each dummy variable indicates whether a store belongs to a specific region.

---

## 5. Reference Category Used

The **West region** was selected as the **reference category**.

It is represented by **0, 0, 0** across all region dummy variables. Using one region as the reference avoids the dummy variable trap (perfect multicollinearity) and allows the model to compare the other regions directly against the West region.

---

## 6. Final Model Selected

The **Multiple Regression Model** was selected as the final model for the analysis.

**Independent Variables**

* Marketing Spend
* Footfall
* Inventory Availability (%)
* Region_North
* Region_South
* Region_East

**Dependent Variable**

* Monthly Sales

---

## 7. Reason for Selecting the Final Model

The multiple regression model was selected because it provided the **highest explanatory power**, with an **R² of 80.74%**, meaning it explains approximately **81% of the variation** in monthly sales.

Unlike the simple regression models, which evaluate one factor at a time, the multiple regression model considers several business drivers simultaneously. This provides a more realistic understanding of store performance by measuring the combined influence of marketing investment, customer footfall, inventory availability, and regional differences.

From a business perspective, the analysis shows that **footfall is the strongest driver of monthly sales**, followed by **marketing spend** and **inventory availability**. The model also identifies that stores in the **East region** perform differently from the reference region, suggesting that regional strategies may be required.

Overall, the multiple regression model provides the most reliable basis for business decision-making because it captures multiple operational factors and offers stronger predictive accuracy than any individual simple regression model.
