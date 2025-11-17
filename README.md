# R-Project 1: Superstore Sales, Profit & Forecasting Analysis (R)


This project analyzes the **Superstore dataset (2011–2014)** to uncover insights about sales, profit, product performance, customer segments, and regional trends using **R**.  
It includes extensive **data cleaning**, **EDA visualizations**, **correlation analysis**, **boxplots**, and **ARIMA forecasting** for predicting 2015 sales and profit.

* **Dataset:** Superstore Dataset (Kaggle, 2011–2014)  
* **Tools:** R, tidyverse, ggplot2, corrplot, treemap, forecast  
* **Techniques:** Data wrangling, bar charts, scatterplots, density plots, tree maps, correlation matrices, boxplots, time-series forecasting  
* **Goal:** Understand the superstore’s historical performance and forecast next-year trends.

---

### 📁 Dataset Overview

The dataset contains 24+ columns including:

- **Sales, Profit, Discount, Quantity, Shipping Cost**  
- **Category, Sub-Category, Shipping Mode**  
- **Market, Region, Segment**  
- **Order & Ship Dates**

<div align="center">
  <img src="images/superstore_datatypes_details.png" width="650"/>
  <p><em>Datatypes descriptions of the dataset.</em></p>
</div>

---

### 🧹 Data Cleaning & Preparation

#### ✔ Checked data types and structure  
#### ✔ Identified missing values  
Only “Postal Code” contains NA values — removed for analysis.

#### ✔ Created a clean dataset `new_superstore`  
Contains only rows/columns with **no missing values**.

<div align="center">
  <img src="images/superstore_na_check.png" width="600"/>
  <p><em>NA inspection and clean dataset creation.</em></p>
</div>

---

### 📊 Orders & Customer Behavior

#### Total Orders by Market, Region, Ship Mode & Segment

<div align="center">
  <img src="images/superstore_orders.png" width="600"/>
  <p><em>Total Orders by Market, Region, Ship Mode & Segment</em></p>
</div>

- **APAC** and **Central** region show the highest order volumes.

---

### 💰 Sales & Profit by Market & Region

<div align="center">
  <img src="images/superstore_sales.png" width="600"/>
</div>


- **APAC** market and **Central** region perform best  
- **Canada** shows significantly lower sales & profit.

---

### 📦 Product Category & Subcategory Analysis

#### Orders by Category / Subcategory

<div align="center">
  <img src="images/superstore_category_counts.png" width="600"/>
</div>

Top subcategories with highest order count:

- **Binders** (12%)  
- **Storage**  
- Lowest: **Tables** (~2%)

#### Pie Chart of Subcategory Orders

<div align="center">
  <img src="images/superstore_pie_subcat.png" width="550"/>
</div>

---

### 🧭 Sales & Profit by Category / Subcategory

<div align="center">
  <img src="images/superstore_sales&profits_subcategory.png" width="600"/>
</div>


**Top findings:**

- **Phones** → highest sales  
- **Copiers** → highest profit  
- **Tables** → incurred losses  

---

### 🌳 Treemap Visualization

<div align="center">
  <img src="images/superstore_treemap.png" width="650"/>
  <p><em>Sales treemap by Category → Sub-Category</em></p>
</div>

---

### 🔍 Scatterplots

<div align="center">
  <img src="images/superstore_scatter.png" width="600"/>
</div>

Observations:

- Sales vs Shipping Cost → **positive relationship**  
- Sales vs Profit → **weak linear relationship**  
- Discount heavily reduces profit  

---

### 📈 Density Plots

<div align="center">
  <img src="images/superstore_density.png" width="600"/>
</div>

- Sales & Discount → right-skewed  
- Profit → slightly left-skewed  
- Quantity → peak around 1–2 units  

---

### 🔗 Correlation Analysis

<div align="center">
  <img src="images/superstore_corrplot.png" width="650"/>
</div>

Key relationships:

- Sales ↔ Shipping Cost → **strong positive correlation**  
- Profit ↔ Discount → **negative correlation**  

---

### 📦 Boxplots

<div align="center">
  <img src="images/superstore_box_sales.png" width="600"/>
</div>

<div align="center">
  <img src="images/superstore_box_quantity.png" width="600"/>
</div>

- Many outliers in Sales / Quantity / Discount  
- Quantity ranges from **1 → 14**  

---

### 📅 Monthly & Annual Trends

#### Annual Sales / Profit (2011–2014)

<div align="center">
  <img src="images/superstore_annual_sales&profits.png" width="600"/>
</div>

Both Sales & Profit show **yearly upward trends**.

---

#### 📆 Monthly Sales / Profit

<div align="center">
  <img src="images/superstore_monthly_sales.png" width="600"/>
</div>

<div align="center">
  <img src="images/superstore_monthly_profit.png" width="600"/>
</div>

---

### 🔮 ARIMA Forecasting (2015)

Using monthly aggregated data:

- Fitted **Auto ARIMA** for Sales & Profit  
- Forecasted next 12 months  
- Confidence interval shown in grey

<div align="center">
  <img src="images/superstore_arima_sales.png" width="650"/>
</div>

<div align="center">
  <img src="images/superstore_arima_profit.png" width="650"/>
</div>

**Forecast Insight:**  
➡ 2015 sales and profit will continue rising, with seasonality similar to previous years.

---

### 🧠 Key Insights

- **APAC + Central** regions drive the most revenue  
- **Phones** (Technology) generate the highest sales  
- **Copiers** generate the highest profit  
- **Tables** consistently lose money  
- Discount negatively impacts profit  
- Yearly performance improves steadily  
- ARIMA forecast predicts **continued growth** in 2015  

---

### 🧠 Skills Demonstrated

- R data cleaning & wrangling  
- Visual analytics (bar charts, scatterplots, boxplots, density plots)  
- Correlation analysis & treemaps  
- Time series modeling with ARIMA  
- Interpreting patterns & forecasting future performance  


