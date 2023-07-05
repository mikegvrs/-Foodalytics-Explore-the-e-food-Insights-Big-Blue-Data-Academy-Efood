# -Foodalytics-Explore-the-e-food-Insights-Big-Blue-Data-Academy-Efood
The code i provided  is an analysis of a dataset related to customer segmentation in the eFood market. Let's break down the steps:

1. Data Loading: The code starts by loading a CSV file named 'data extract for customer segmentation efood market.csv' into a Pandas DataFrame called 'df'. It then displays the first 10 rows of the DataFrame using the head() function.

2. Data Exploration: The code further explores the DataFrame by providing information about the columns, their data types, and the presence of missing values. It also calculates the percentage of missing values in each column.

3. Data Cleaning: To remove missing observations, the code drops rows where the 'items_sold' column has null values using the dropna() function. It then replaces any remaining null values in the DataFrame using the fillna() function.

4. On certain columns, the code applies some data transformations. The "product_price" and "items_sold" columns are multiplied to determine the total sales for each row, which is then recorded in the "total_sales" column. The to_datetime() function is used to convert the "order_timestamp" and "registered_at" fields to datetime format. In addition, it uses the astype() function to change the 'items_sold' column's data type from string to integer.

5. Exploratory Data Analysis (EDA): The code conducts several analyses to explore different aspects of the data:

   Unique Items: It counts the different values in the "product_name" column to calculate how many unique items there are in the dataset.

   Products Count: The value_counts() method is used on the 'product_name' column to display the number of products in the dataset.

   Customer Transactions: A DataFrame called "customer_counts" is used to calculate the average number of transactions per customer. The top 25 customers with the most transactions are then represented graphically using a 
   horizontal bar plot.

   Total sales for each item: The order_value for each product is added up once the data is grouped by "product_name." The outcomes are shown and recorded in a Series with the name "product_sales."

   Top 10 Products by Total Sales: It further analyzes the total sales per product by sorting the 'product_sales' Series and creating a bar plot to visualize the top 10 products based on total sales.

6. Market Basket Analysis / Association Rules: The code performs market basket analysis to find associations between customers and the products they purchase. It uses the 'arules' function.The result is stored in a 
   DataFrame named 'df_rules' and saved as a CSV file.

7. Percentage of Orders by Top 10 Users: The code calculates the percentage of orders contributed by the top 10 users in each city. It filters the cities with more than 1000 orders, groups the data by city and user, and 
   calculates the number of orders and total purchase amount. It then calculates the percentage of each user's orders to the total orders of their city. The results are displayed in a bar plot.

8. Cohort Analysis: The code performs cohort analysis to analyze customer behavior over time. It creates the 'cohort' and 'order_month' variables based on the 'order_timestamp' column. It then aggregates the data per 
   cohort and order month, counts the number of unique customers in each group, and creates a cohort pivot table. The resulting retention matrix is visualized using a heatmap.

9. RFM (Recency, Frequency, Monetary) Analysis: The code conducts RFM analysis to segment customers based on their recency, frequency, and monetary value. It calculates the recency,frequency, and monetary metrics for each 
   customer, assigns them to corresponding segments, and creates a summary DataFrame. The results are displayed in tabular format.

10. Patterns: This code analyzes the sales data over time, identifies the top product categories based on total sales, and visualizes the trends in total sales and purchase patterns for these categories. Additionally, it 
    provides insights into the total number of unique orders in the dataset.


   Overall, the code performs various data analysis tasks, including data cleaning, exploration, visualization, market basket analysis, cohort analysis, and RFM analysis, to gain insights into customer behavior and 
   product sales in the eFood market.


