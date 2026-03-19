# PowerBI-Lab-Work_3

[Click here to view PDF](./CABUSAS_PATHRICK_Power_BI_Laboratory_Work_Activity_3.pdf)

# Part 1: Review the Merged Dataset Guide Questions

1. Is the dataset in flat-table format?
   
Yes, the dataset is in flat-table format all data is stored in a single table with rows and columns, where each row represents one order.

2. Which columns describe customers?
   
CustomerID, CustomerName, City, and Region describe the customers.

3. Which columns represent transactions?

OrderID, OrderDate, and SalesAmount represent the transactions.

# Part 2: Identify Fact and Dimension Tables Guide Questions

1. Why must dimension tables contain unique keys?
   
 Dimension tables must have unique keys so that each record can be correctly identified and matched when linking to the fact table. Without unique keys, relationships between tables will be inaccurate or won't work at all.
 
2. What problems occur if duplicates exist in DimCustomer?
   
 If duplicates exist in DimCustomer, Power BI won't be able to create a proper one-to-many relationship with FactSales, causing errors in reports and incorrect results  for example, a customer's sales being counted multiple times.

# Part 3: Define Primary & Foreign Keys Guide Questions

1. What is a primary key?
   
A primary key is a column that uniquely identifies each row in a table. In the image, CustomerID is the primary key in DimCustomer and OrderID is the primary key in FactSales meaning no two rows can have the same value in those columns.

2. Why is CustomerID a foreign key in FactSales?
   
CustomerID is a foreign key in FactSales because it doesn't uniquely identify rows in that table instead, it references the primary key in DimCustomer to link each sales transaction to its corresponding customer. It creates the relationship between the two tables.

# Part 4: Create Relationships Guide Questions

1. Why should relationships flow from dimension to fact?
   
So that filters from dimension tables (like customer or region) correctly flow into the fact table, allowing accurate slicing and analysis of sales data.

2. What happens if the relationship is Many-to-Many?
   
It causes ambiguous matches, leading to incorrect totals, double counting, and unreliable reports.

# Part 5: Validate the Data Model Guide Questions

1. Did sales aggregate correctly per customer?
   
 Yes, sales aggregated correctly each customer shows their total SalesAmount, meaning the relationship between DimCustomer and FactSales is working properly.
 
2. What would happen if relationships were missing?
   
Without relationships, SalesAmount would show the same grand total for every customer instead of their individual totals, making the report completely inaccurate.

# Enhancement Activities Introduction to DAX Create Measures Guide Questions

1. What is a DAX measure?
   
A DAX measure is a formula written in Data Analysis Expressions (DAX) that calculates values dynamically based on the context of your report, like filters or slicers.

2. Difference between SUM and AVERAGE?

   
SUM adds all values together to give a total, while AVERAGE divides the total by the number of records to give the mean value.

3. Why use measures instead of calculated columns?
   
Measures calculate results dynamically at report runtime based on filters and context, making them more efficient and flexible. Calculated columns are computed row by row and stored in the table, consuming more memory.

# 2. Monthly Sales Growth Guide Questions

1. What is time intelligence in DAX?
   
 Time intelligence in DAX refers to functions that perform calculations based on time periods, such as year-to-date, month-over-month, and previous month comparisons.
 
2. Why is a date table required?
   
 A date table is required because time intelligence functions like TOTALYTD and PREVIOUSMONTH need a continuous, unbroken sequence of dates to calculate correctly across time periods.
 
3. How does PREVIOUSMONTH help analyze trends?
   
 PREVIOUSMONTH retrieves the total from the previous month so you can compare it to the current month, making it easy to see whether sales are growing or declining over time.
 
4. What insights can YTD Sales provide?
   
YTD Sales shows the cumulative total from the start of the year up to the current date, helping businesses track overall progress toward annual sales targets.























