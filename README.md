# Pizza_sales_analysis

### Project Overview

This data analysis project aims to provide insights into the sales performance of an Pizza selling  company over the past year. By analyzing various aspects of the sales data, we seek to identify trends, make data-driven recommendations, and gain a deeper understanding of the company's performance.

### Data Sources
Pizza Sales Data: The primary dataset used for this analysis is the "Pizza_sales.csv" file, containing detailed information about each sale made by the company.

### Tools

- Excel - Data Cleaning [Download here](https://www.microsoft.com/en-in/microsoft-365/excel) and Creating Reports
- SQL Server - Data Analysis [Download here](https://www.microsoft.com/en-us/sql-server/sql-server-downloads)

### Data Cleaning and Preparation
In the initial data preparation phase, we performed the following tasks:
1.  Data loading and inspection.
2.  Handling missing values.
3.  Data cleaning and formatting.

Exploratory Data Analysis
EDA involved exploring the sales data to answer key questions, such as:

- What is the total revenue?
- What is the average value?
- Total Quantity of Pizza sold?
- Total number of order placed?
- Avg number of Pizza sold per order?

### Data analysis

1. Total Revenue:
  ```sql
SELECT SUM(total_price) AS Total_Revenue FROM pizza_sales;
```
2. Average Order Value
```sql
SELECT (SUM(total_price) / COUNT(DISTINCT order_id)) AS Avg_order_Value FROM pizza_sales
```
3. Total Pizzas Sold
```sql
SELECT SUM(quantity) AS Total_pizza_sold FROM pizza_sales
```
4. Total Orders
```sql
SELECT COUNT(DISTINCT order_id) AS Total_Orders FROM pizza_sales
```
5. Average Pizzas Per Order
```sql
SELECT CAST(CAST(SUM(quantity) AS DECIMAL(10,2)) / 
CAST(COUNT(DISTINCT order_id) AS DECIMAL(10,2)) AS DECIMAL(10,2))
AS Avg_Pizzas_per_order
FROM pizza_sales
```
### Results/Fidings
#### Busiest days 
- ordeers are highest on weekends Friday/saturday evenings
#### Busiest Time
- There are maximum order from 12-01pm and after 5-8 pm
#### sales by category and size
- classic category contributes to maximum sales and total orders
- Large size pizza contributes to maximum sales
#### Best and Worst seller
- Classic delux and chicken Pizza are the best seller and revenue generator
- The Brie carre is at the bottom in both order and revenue
### Recomendations
Based on the analysis, we recommend the following actions:

- Invest in marketing and promotions during weekends to maximize revenue.
- Focus on expanding and promoting products in Calssic Category Pizza .
- Implement a customer segmentation strategy to target high-LTV customers effectively.






