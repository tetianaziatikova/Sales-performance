# E-Commerce Sales Analysis 
## Project Overview
This project focuses on analyzing the sales performance of an e-commerce company during January and February. By examining various aspects of the sales data, the goal is to gain insights into key products, identify significant customers, and assess the overall effectiveness of business operations.

## Key Insights:
- **Key products**

  - **Top Sellers:** Home Decor and Laptops are the most popular products, accounting for nearly 60% of total sales.
  - **Moderate Demand:** Furniture and Headphones show significant sales, though less pronounced than the top two.
  - **Niche Products:** Smartphones and Haircare Products have much lower sales figures, indicating a more niche market interest.

- **Key customers**
  
  - **United States** stands out as the most profitable country, significantly contributing to total profits. It also houses the highest-spending customers, indicating a strong market potential.
  - **Poland** follows with a solid profit, supported by mid-range top spenders, suggesting opportunities for growth and marketing strategies aimed at these consumers.
  - **Ireland**, while lower in profit, still represents a potential market, and high-value customers.

- **Key customers**
  
  - **Operational Efficiency:** The high success rate of order processing indicates robust operational efficiency. However, the few unsuccessful orders highlight the need for ongoing monitoring and improvement of processes.
  - **Customer Spending Behavior:** AOV and AC reflect how much customers are willing to spend per order and per transaction. With AOV at 502 units and AC at 24 units, there is room for improvement in increasing both metrics. Strategies like targeted marketing, product recommendations, and enhancing the customer experience can help.
  - **Customer Lifetime Value:** A high LTV of 47,572 units shows strong customer loyalty and suggests that investing in customer acquisition can yield long-term benefits. This is a strong indicator of potential profitability.

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
- Top 10 Spending Customers: Which customers have the highest total spending?
- Repeat Customers: How many customers have made multiple purchases and Top 10 Repeat Customers?
- Order Status Distribution: What is the distribution of order statuses?
- Average Order Value: What is the average order value across all invoices?
- LTV (Lifetime Value): What is the total spending of a customer across all transactions?
- Average Check: What is the average amount spent by a customer per transaction?
## Visualization
- **Total Sales by Country:** The table provides a breakdown of profit by country, which can be used to analyze the profitability across different regions.
<img width="317" alt="Total Sales by Country" src="https://github.com/user-attachments/assets/ab214f0e-ac13-473d-b6da-c73ef56a2899">

Top three Countries by Profit: United States leads with a substantial margin, generating $53,534 in  profit, which represents the highest profitability among all listed countries. Poland follows with
$33,915, indicating strong performance in this region as well. Ireland is in third place with $12,648. And aditionaly the Table with Profit by top 10 Country and all Category where the higher profit marked with a darker color.

<img width="510" alt="Profit by Top 10 Country and Category" src="https://github.com/user-attachments/assets/84691020-b9a1-494a-b2fc-d6b438da7376">

- **Geographical Distribution:** Employed map charts to illustrate the geographical distribution of total sales by country.
<img width="551" alt="Total sales by country_" src="https://github.com/user-attachments/assets/e3997598-3eaa-45e8-a947-fcd37169b418">


- **Trends:** Used line charts to visualize trends over time for sales quantities and prices. 
<img width="486" alt="Trends_2" src="https://github.com/user-attachments/assets/646cac41-e31e-48d6-a4ed-848643bc2607">

In analyzing the sales data for 2010, there is a clear fluctuation in sales quantities and average prices over time. The total sales quantity for the period reached 460,506 units, with an average price of $3.80. Most daily prices remained steady at $3; however, certain days saw significant price spikes, such as January 8th and January 29th, when the price rose to $6 and $14, respectively. These price increases appear isolated and do not consistently correlate with sales quantity, suggesting that demand may have been influenced more by external factors rather than price alone. Days with exceptionally high quantities, like January 21st (72,914 units), maintained the typical low average price of $3. Overall, the data indicates stable demand with occasional quantity peaks and rare price fluctuations, which may point to specific promotional events or demand surges.

- **Distributions:** Utilized column and bar charts to display distributions such as top-selling products.
<img width="615" alt="Top 10 Best-Sellings Products_2" src="https://github.com/user-attachments/assets/048191d2-ec6c-4b75-a979-c090b7707828">

The top 10 best-selling products reveal that Home Decor and Laptops dominate sales, with 134,810 and 126,312 units sold, making up nearly 60% of total sales. Furniture follows with 72,149 units, while Headphones and Skincare Products sold 38,066 and 16,273 units, respectively. Sports Equipment and Accessories also show demand with 13,316 and 11,352 units sold. Smartphones and Haircare Products sold fewer units, at 7,023 and 4,824, suggesting more niche interest. This highlights strong consumer focus on home goods and electronics.

- **Top 10 Spending Customers:**
<img width="536" alt="Total 10 Spendigs Customers" src="https://github.com/user-attachments/assets/d49a5034-1b43-43b2-87a6-e8cfc47bb747">

The top-spending customers show a significant range in total expenditure, with the highest individual spending reaching over 35 million units. Customer IDs such as 13902 and 18102 stand out, having spent 35.9 million and 12.5 million units, respectively. Mid-range top spenders include customers 16029 and 14646, with expenditures in the range of 2.6 to 6.3 million units.

- **Repeat Customers:** Used pivot table in Excel to calculate general number of Repeat Customers. There are 29960 such Customers. Aditionaly Top 10 Repeat Customers shown on the graph.
<img width="537" alt="Repeat Customers for 16 years" src="https://github.com/user-attachments/assets/75dd0be2-495b-43be-ab53-f1d4c80470b0">

## Сalculations
- **Order Status Distribution:** The distribution of order statuses reveals a high success rate for orders. Out of a total of 29,999 orders, 29,923 were successful, and only 76 were unsuccessful. This means that 99.75% of orders were completed successfully, while 0.25% were not. This high success rate indicates efficient order processing, though the small percentage of unsuccessful orders suggests potential areas for improvement to further enhance reliability.

- **Average Order Value:** Used pivot table and functions in Excel to calculate Average Order Value (AOV). AOV = Total Revenue / Number of Orders. For this case it is 502 units.

- **Lifetime Value:** Used pivot table and functions in Excel to calculate Lifetime Value (LTV). LTV = Average customer lifetime (years) * Average purchase * Average number of purchases per year. LTV = 47572 units.
  
- **Average Check:** Used pivot table and functions in Excel to calculate Average Check (AC). AC = Total income / Number of transactions (transaction_id). AC = 24 units.
<img width="525" alt="Calculation" src="https://github.com/user-attachments/assets/50d624db-1d52-49ae-aa63-657d14034b3d">

These three metrics (AOV, LTV and AC) are important for business analysis. They allow you to understand how customers interact with your products, how much they spend, and what strategies can be effective to increase revenues.
  


