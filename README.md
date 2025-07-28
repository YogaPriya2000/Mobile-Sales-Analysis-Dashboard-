# Mobile-Sales-Analysis-Dashboard-

**Objective**
To analyze and visualize mobile sales data to identify trends, top-performing products, and customer purchasing behavior using interactive dashboards.

**Tools Used**
•	Power BI Desktop
•	DAX (Data Analysis Expressions)
•	Power Query (M Language)

**Key Features of the Dashboard**
•	Sales Overview: Total revenue, profit, Average Price, Transactions and quantity sold
•	Top Products: Best-selling mobiles by units/revenue
•	Customer Segmentation: Buyers categorized by region and brand preference
•	Time Analysis: Sales trend by month/quarter
•	Filters & Slicers: Brand, Category, Region, Month and Date filters for drill-down

**Insights Gained**
•	Apple, Samsung, OnePlus, Vivo, Xiaomi were the top 5 Best-selling brands.
•	A steady sales growth was observed in Q2.
•	North region contributed the highest revenue.
•	Customers prefer mid-range phones over flagship models.


**Data Cleaning & Transformation**
•	Removed duplicates and null values
•	Standardized column names
•	Converted data types (e.g., date format)
•	Created calculated columns and measures using DAX

**DAX Measures Used**
•	‘Sales_Data'[Total_Quantity] = SUM(Sales_Data[Units Sold])
•	'Sales_Data'[Total_Sales] = SUMX(Sales_Data,Sales_Data[UnitsSold]*Sales_Data[Price Per Unit])
•	'Sales_Data'[Transactions] = COUNTROWS(Sales_Data)
•	'Sales_Data'[Average_Price] = AVERAGE(Sales_Data[Price Per Unit])
•	'Sales_Data'[MTD] = TOTALMTD([Total_Sales], Custom_Calender[Date].[Date])
•	'Sales_Data'[Same Period Last Year] = CALCULATE([Total_Sales], SAMEPERIODLASTYEAR(Custom_Calender[Date].[Date]))

**Conclusion**
This dashboard empowers stakeholders with data-driven decisions by showcasing product performance, customer behavior, and market trends in a visually interactive format.

