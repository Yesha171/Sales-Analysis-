
# Project Title

Sales Analysis

## Problem Statement

This project aims to transition from static internet sales reports to dynamic and interactive dashboards to enhance the analysis of sales performance. The dashboard will enable users to explore and visualize sales data comprehensively, focusing on products sold, customers, time trends, and performance against budget.

### Steps followed 

- Step 1 : Load data into Ms-SQL.
- Step 2 : Extracted data from Calendar, Customers, InternetSales and Product tables.

Snap of Calendar table ,

 Cleaned data and added new column named MonthShort. Given new column name by using alias.

![Snap_1]![Calendar Sales](https://github.com/user-attachments/assets/1cdd7b5e-0313-420f-a1a0-50dd10cd0254)

Snap of Customer table ,

 Cleaned data and given new column name by using alias.Added new column new Full Name. Use Case statement to identify the gender column. And by using the Left Join - joined the table DimGeography to DimCustomer for Customer City column.
  
![Snap_2]![Customer Sales](https://github.com/user-attachments/assets/bb6c8116-d3b4-4724-9ba3-e72065a9abc1)
 

Snap of InternetSales table ,

 Cleaned data and arranged data by using where clause. By using last 4 digits of the OrderDateKey and subtracting it from present year to get the data of last 3 years of the given data.

![Snap_3]![InternetSales Sales](https://github.com/user-attachments/assets/5c6fb898-de0f-49cf-98fb-9330ac78ea92)

Snap of Product table ,

 Cleaned data and given new column name by using alias. Used ISNULL function for product status to know which product is outdated or current. By using the Left Join - Joined 3 tables DimProduct table, DimProductSubcategory table and DimProductCategory table.

![Snap_4]![Product Sales](https://github.com/user-attachments/assets/c5827973-0a63-4a98-83cc-2ac3a7949d26)

- Step 3 : Loaded all the different tabled in Power BI to create dashboard. 
- Step 4 : Create relationship between tables.

![Snap_5![Relationship table](https://github.com/user-attachments/assets/b87d4701-b654-45f1-b375-e62964f917c0)

- Step 5 : By using new measures created 4 new measures named Budget Amount, Sales, Sales - Budget and Sales / Budget Amount. 

     Budget Amount = SUM(FACT_Budgets[Budget])

     Sales = SUM(FACT_InternetSales[SalesAmount])

     Sales - Budget = [Sales] - [Budget Amount]

     Sales / Budget Amount = DIVIDE([Sales], [Budget Amount])

- Step 6 : Added six different slicers named "Year", "MonthShort", "Customer City", "Sub Category", "Category" and "Product Name" to filter the data and see different results for analysis on all the three pages. 

Sales Overview:
![Snap_6]![Sales Overview](https://github.com/user-attachments/assets/31432aaa-a999-453f-b7e8-da6114a84ff5)

The dashboard highlights strong sales performance, with total sales of 22,239,730, surpassing the budget by 1,139,730. Bikes dominate sales, contributing 95.32% (21M), while the top product, Mountain-200 Black, generated 1,371,420. Key customer Jordan Turner led with 15,999 in sales, followed by other high-performing customers.

Geographically, sales are concentrated in European regions like the UK, Germany, and the Netherlands. Monthly trends show peaks in March, July, and December, often exceeding the budget. The dashboard also offers filters by category, product, city, and time, allowing deeper insights into performance.

Customer Details:
![Snap_7]![Customer Details](https://github.com/user-attachments/assets/a8c43276-ebb4-4ac6-8934-34f62dc58c9e)

The Customer Details dashboard provides a breakdown of sales performance by customer, region, and time.

Overall Performance: Total sales reached 22,239,730, exceeding the budget of 21,100,000. Sales consistently align with or surpass the budget across most months, with peaks in March, July, and December.

Top Customers: The leading customer is Jordan Turner with sales of 15,999, followed by Maurice Shan (12,910) and Janet Munoz (12,489). Other key contributors include Lisa Cai (11,469) and Lacey Zheng (11,248).

Geographical Insights: Sales are concentrated in North America and Europe, with prominent cities driving revenue. This suggests strong customer engagement in these regions.

Monthly Breakdown by Customer: A heatmap reveals individual customer contributions by month. Significant sales spikes are seen in December, especially for Jordan Turner and Marco Lopez.

Product Details:
![Snap_8]![Product Details](https://github.com/user-attachments/assets/3f21b776-c2aa-444d-be5e-7afefc1d7c2c)

The Product Details dashboard provides a comprehensive view of sales performance across product categories and time.

Overall Performance: Total sales are 22,239,730, surpassing the budget of 21,100,000. Sales trends align with or exceed the budget across the year, peaking in March, July, and December.

Top Products: The leading product is Mountain-200 Black, generating 1,371,420, followed by other Mountain-200 variants and Road-250 models. These products dominate sales, with the top 5 contributing over 6 million combined.

Category and Product Insights: The Clothing category generated 339,773, with notable contributions from items like AWC Logo Cap (19,688) and Long-Sleeve Logo Jerseys. The heatmap highlights steady monthly contributions from various products.

Geographical Insights: Sales are strongest in North America and Europe, as indicated by the map visualization. High-performing regions show consistent demand across products.

Conclusion:
The dashboards highlight a strong performance, with sales of 22,239,730, exceeding the budget by 1,139,730, driven primarily by Bikes (95.32% of sales) and top products like Mountain-200 Black. Key customers, such as Jordan Turner, and regions like North America and Europe were major contributors. Seasonal peaks in March, July, and December boosted revenue, while the Clothing category added 339,773, with standout items like AWC Logo Cap. To sustain growth, the business should focus on top customers, expand in high-performing regions, leverage seasonal trends, and explore opportunities in underperforming categories like Accessories. The outlook remains strong.
