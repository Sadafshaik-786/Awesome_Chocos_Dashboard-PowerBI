# Awesome_Chocos_Dashboard-PowerBI

# 🍫 Awesome Chocolates Sales Report Dashboard

An **interactive sales dashboard** built in **Power BI** to analyze and visualize sales performance for *Awesome Chocolates*.  
This project highlights the use of **DAX, data modeling, and storytelling through visualizations** to uncover key business insights.  

---

## 📊 Dashboard Overview
The dashboard provides a business snapshot with:
- **Total Sales**: 💰 13M  
- **Total Customers**: 👥 466  
- **Avg Sale per Customer**: 📊 28K  
- **Top Product Contribution**: 🏆 5% of total sales  

---

## 🔎 Key Insights
- **Sales Trend by Region (GeoID)**: Identified top-performing regions & market share 🌍  
- **Sales by Salesperson (SPID)**: Bar chart for performance benchmarking 📈  
- **Product Contribution (Pareto Analysis)**: 80/20 rule applied to see top-revenue products 🎯  
- **Customer Volume vs. Sales (Scatter Plot)**: Found high-value vs. low-value products 💡  
- **Top 5 Products (Pie Chart)**: Simplified view with “Others” grouping for clarity 🥧  

---

## ⚙️ Technical Details

### 🔧 Tools & Tech
- **Microsoft Power BI Desktop**  
- **Excel (data source)**  
- **DAX (Data Analysis Expressions)**  

### 📐 DAX Measures
```DAX
-- Total Sales
Total Sales = SUM(Sheet1[Amount])

-- Average Sale per Customer
Avg Sale per Customer = DIVIDE([Total Sales], [Total Customers])

-- Top Product Contribution %
Top Product % =
DIVIDE(
  CALCULATE(
    [Total Sales],
    TOPN(1, VALUES(Sheet1[PID]), [Total Sales], DESC)
  ),
  [Total Sales]
)


