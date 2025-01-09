### **Overview**

This project is aimed at creating a **Retail Sales Dashboard** for a fictional retail company using data analysis techniques, DAX formulas, and Power BI. The dashboard will provide key insights into **sales performance**, **customer behavior**, and **inventory management** to optimize operations and increase revenue.

The dashboard is designed with three main sections:

1. **Sales Overview**
2. **Customer Insights**

Each section will display key metrics and trends through interactive visualizations, which will help stakeholders make informed decisions.

### **Key Learning Objectives**

- **Data Analysis in Retail**: Gain an understanding of how to analyze retail sales data and translate that into actionable insights.
- **Dashboard Design**: Learn how to design a clean and intuitive dashboard layout to visualize complex data in an easily digestible manner.
- **DAX Formulas**: Master DAX calculations for key metrics such as average spend per customer, revenue by product category, etc.
- **Data Visualization Best Practices**: Understand which types of visualizations (charts, tables, KPIs) are best suited for different insights.
- **Power BI**: Develop skills in creating interactive dashboards using Power BI.

### **Outline of Questions in Categories**
#### **Sales Insights**
1. **What are the total sales over time (monthly, weekly)?**
2. **Which products and categories generate the most revenue?**
3. **Which stores perform best in terms of revenue and transaction volume?**
#### **Customer Insights**
4. **Who are the top customers contributing to sales?**
5. **What is the average spend per customer by location?**
6. **How is customer loyalty distributed across locations?**
#### **Operational Efficiency**
7. **What is the payment method distribution (e.g., cash, credit, digital wallets)?**
8. **Which regions or stores experience low sales performance?**
9. **How are discounts affecting sales trends?**
#### **Inventory Insights**
10. **Which products are running low on stock and need reordering?**
11. **Are there products with surplus stock or low demand?**


### **Solution Plan as Tables**

|**Page**|**Focus**|**Sections**|**Questions Answered**|
|---|---|---|---|
|**Page 1**|**Sales Overview**|KPIs, Sales Trends, Category Revenue, Top Products|Total sales, transaction volume, average spend, top categories, and products|
|**Page 2**|**Customer Insights**|KPIs, Customer Segments, Top Customers, Regional Analysis|Top customers, average spend, customer loyalty, regional performance|
|**Page 3**|**Inventory & Operations**|KPIs, Stock Status, Payment Methods, Product Turnover|Stock at risk, overstocked products, payment methods, product turnover|

Average Spend per Customer( Calculates the average amount spent per customer. )
```
DIVIDE(SUM(Sales[TotalSales]), DISTINCTCOUNT(Sales[CustomerID]), 0)
```
Total Sales by Category( Sums total sales for each product category. )
```
SUMX(FILTER(Sales, Sales[Category] = "CategoryName"), Sales[TotalSales])
```
