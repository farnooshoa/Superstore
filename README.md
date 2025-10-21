#  Superstore Sales Analysis


## Project Overview
This project explores the **Superstore dataset** to uncover insights about sales, profit, and customer behavior across different regions, categories, and time periods.  
It demonstrates an end-to-end **data analysis workflow** — from cleaning and feature engineering to visualization and interpretation.

---

##  Objectives
- Clean and prepare the Superstore dataset for analysis  
- Create new business metrics:
  - **Profit Margin (%)**
  - **Revenue per Customer**
- Explore key questions:
  - Which regions and categories generate the most profit?
  - How do sales and profit change over time?
  - Which products or segments perform best?
- Build clear visualizations for storytelling and decision support.

---

## Tools & Libraries
- **Python**
- **pandas** – data manipulation  
- **NumPy** – numerical computation  
- **Matplotlib / Seaborn** – data visualization  
- **Jupyter / Colab** – notebook environment

---

##  Data Cleaning
1. Checked and handled missing values  
2. Converted `Order Date` and `Ship Date` to datetime  
3. Fixed categorical and numeric data types  
4. Added new calculated fields:
   ```python
   df['Profit Margin'] = (df['Profit'] / df['Sales']) * 100
   revenue_per_customer = df.groupby('Customer Name')['Sales'].sum()
   df['Revenue per Customer'] = df['Customer Name'].map(revenue_per_customer)

