# E-Commerce Sales Analysis 
## Project Overview
This project focuses on analyzing the sales performance of an e-commerce company during January and February. By examining various aspects of the sales data, the goal is to gain insights into key products, identify significant customers, and assess the overall effectiveness of business operations.
## Data Sources
Sales Data: the primary datasets used for this analisys are the "fact_sales_february.xlsx" file and "fact_sales_january.csv" file containing comprehensive details about each transaction completed by the company. They representing January and February sales respectively. Each contains detailed transactional data about sales. Each record represents a sales invoice with the following key attributes:
- **Invoice:** identifier for each invoice
- **StockCode:** Product identifier for the sold item.
- **Sum of Quantity:** Total quantity of the product sold in the transaction.
- **InvoiceTime:** Timestamp indicating when the sale was made.
- **Sum of Price:** Total price for 1 product unit sold in the transaction.
- **Customer ID:** Identifier for the customer who made the purchase.
- **Country:** Country where the customer is located.
- **StockCode_ID:** Identifier linking to the product details.
- **Status:** Status of the invoice (e.g., successful, canceled).
  
Additional primary dataset is "dim_stock.xlsx" file and it provides detailed information about the products being sold. Each record corresponds to a unique product with the following key attributes:
- **Category_ID.1:** Unique identifier for the product category.
- **Category:** General category of the product.
- **Sub-Category:** Specific subcategory of the product.
- **ProfitRate:** Profit margin for the product, indicating the profitability.
## Tools
- Power Query Editor - Appending sales data from multiple sources into a single table
- Pivot table Excel - Data Analysis
- Pivot chart Excel - Data Visualization
## Data Preparation and Quality Improvement
**1. Appended Sales Data:** Used Power Query Editor to append sales data from multiple sources into a single table for comprehensive analysis.

**2. Created Unique Transaction Identifier:** `Invoice` was not a unique identifier for a transaction. Created a `transaction_id` field by combining `Invoice` and `StockCode` to ensure the uniqueness of each transaction.

**3. Enhanced Data Quality:** Before analyzing data, improved its quality by addressing duplicates, outliers, and misspellings. This step was crucial for accurate and reliable analysis.

**4. Calculated Total Price:** Calculated the total price of each transaction by multiplying the unit price and quantity. Ensured this calculated field is included in my dataset.

**5. Calculated Profit:** Merged the `fact_sales` and `dim_stock` tables to calculate profit. Used the `ProfitRate` from the `dim_stock` table and the total price from the `fact_sales` table for this calculation.
## Analysis Questions
- Total Sales by Country: What is the total profit for each country?
- Sales Trends Over Time: How do sales quantities and prices trend over different time periods?
- Top 10 Best-Selling Products: What are the top 10 best-selling products by quantity?
- Sales Performance by Category: What is the sales performance by product category and sub-category?
- Top Spending Customers: Which customers have the highest total spending?
- Repeat Customers: How many customers have made multiple purchases?
- Order Status Distribution: What is the distribution of order statuses?
- Average Order Value: What is the average order value across all invoices?
- LTV (Lifetime Value): What is the total spending of a customer across all transactions?
- Average Check: What is the average amount spent by a customer per transaction?
## Visualization
- **Trends:** Used line charts to visualize trends over time for sales quantities and prices.
![Trends](https://github.com/user-attachments/assets/ec1d39f2-452b-4e04-955a-3716c5088fdf)

- **Distributions:** Utilized column and bar charts to display distributions such as top-selling products.
![Top 10 Best-Sellings Products](https://github.com/user-attachments/assets/ca3362d9-f857-41f5-a02d-218821ebaf4b)

- **Geographical Distribution:** Employed map charts to illustrate the geographical distribution of total sales by country.
![Total sales by country](https://github.com/user-attachments/assets/4faa2fda-f72f-47cd-8db2-df9584306552)


- **Category Shares:** Used pie charts to show the share of a maximum of three categories, such as the distribution of order statuses.
![Order Status Distribution](https://github.com/user-attachments/assets/6a993b35-1819-4206-b3b1-b9db0e0bbf48)


