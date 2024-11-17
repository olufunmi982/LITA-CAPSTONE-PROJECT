# LITA-CAPSTONE-PROJECT
An overview of Incubator hub capstone project
## ANALYSIS OF CAPSTONE PROJECT SALES DATA

### PROJECT OVERVIEW

The Analysis of Capstone Sales data dealt with the overview of the product performance of capstone sales data as it relate with some factors affecting these products.

### DATA SOURSES
- Microsoft Excel (Download Here)
- Capstone sales data set

### Data Cleaning and Preparations

- Data cleaning was performed on Excel and this phase comprises of removal of duplicates, some columns were added and also there are some data types that neede to be changed , all these was done in this stage.

- Microsoft Excel was used for analysis with the aid of excel formulas and functions

- Visualization - the pivot table and pivot charts was used to summarise the reports of the analysis on Excel

### SQL (Structured Query Language)
This model was used to write to write queries for all necessary reports needed, clean data was imported from excel to SQL.

### Power BI, The data used on excel was also imported to Power BI

### DATA EXPLORATORY 
- Thorough data exploratory was done on Excel, SQL and Power BI.

- Some new columns were added in Excel, for example the Revenue column, some other were also added in SQL and Power BI

- Pivot tables and Pivot charts were used to summarise reports on excel

- Power BI visuals was used to present the reports on  power BI

### DATA ANALYSIS

##### The following analysis was done on excel using excel formulas and functions

- To calculate Revenue
```
= F2*G2
```
- To get transaction category
```
=IF(F2<=5,"Low",IF(F2<=10,"Medium","High"))
```
- Total Quantity Sold
```
=SUM(F2:F9922)
```
- Average Quantity Sold
```
=AVERAGE(F2:F9922)
```
- TOTAL SALES
```
=SUM(H2:H9922)
```
- AVERAGE REVENUE
```
=AVERAGE(H2:H9922)
```

### EXCEL REPORTS (PIVOT TABLES AND PIVOT CHARTS)
![Screenshot 2024-11-05 144329](https://github.com/user-attachments/assets/971adab5-7735-4f59-ac61-dc96e0ad09ee)

![Screenshot 2024-11-05 144354](https://github.com/user-attachments/assets/58ec337c-fbd9-447d-838b-e7a818a18ba1)

![Screenshot 2024-11-05 144430](https://github.com/user-attachments/assets/589c7d81-e0d4-43df-921a-bd93d78ef54e)

![Screenshot 2024-11-05 144250](https://github.com/user-attachments/assets/24526778-d1d9-4197-ad4c-92cf3298a850)

![Screenshot 2024-11-05 144537](https://github.com/user-attachments/assets/4508718b-0d39-4f08-9e00-818dcf0fd307)

![Screenshot 2024-11-05 144527](https://github.com/user-attachments/assets/fb7b0a74-1fb0-44c0-a97f-60b82acbc088)


### ANALYSIS ON SQL
- Retrieve the total sales for each product category
```
SELECT Product,SUM(Quantity*UnitPrice) as Total_Sales
FROM [dbo].[Sales Data 2]
GROUP BY Product
```
- Find the number of sales transactions in each region
```
SELECT Region,SUM(Quantity*UnitPrice) as Total_Sales
FROM [dbo].[Sales Data 2]
GROUP BY Region
```
- Find the highest-selling product by total sales value
```
SELECT Product, SUM(Quantity*UnitPrice) as Total_Sales
FROM[dbo].[Sales Data 2]
GROUP BY Product
```
- Calculate total revenue per product
```
SELECT Product,Sum(Revenue) As Total_Revenue
FROM[dbo].[Sales Data 2]
GROUP BY Product
```
- Find the top 5 customers by total purchase amount
```
SELECT Top 5 Customer_Id,SUM(Quantity) AS Total_Purchase
FROM[dbo].[Sales Data 2]
GROUP BY Customer_Id
ORDER BY Total_Purchase DESC
```
- Calculate the percentage of total sales contributed by each region
```
SELECT Region, SUM(Revenue)/SUM(Quantity*UnitPrice)*0.1 AS Percebtage_of_Total_Sales
FROM [dbo].[Sales Data 2]
GROUP BY Region
ORDER BY Percebtage_of_Total_Sales
```
- Identify products with no sales in the last quarter
```
SELECT Product,SUM(Quantity) AS Sales
FROM [dbo].[Sales Data 2]
WHERE MONTH(OrderDate) BETWEEN 10 AND 12 -- Months 10, 11, and 12 (October to December)
GROUP BY Product
```

### SQL REPORTS
![SQL ANALYSIS REPORT 1](https://github.com/user-attachments/assets/9b831e2c-ae14-4764-b432-e9e31d54cafc)

![SQL ANALYSIS REPORT 2](https://github.com/user-attachments/assets/724e7485-e120-4708-bdef-73d88efddfa4)

![SQL ANALYSIS REPORT 3](https://github.com/user-attachments/assets/d2eb1a53-d956-453c-83f4-e7db2e89b471)

![SQL ANALYSIS REPORT 4](https://github.com/user-attachments/assets/a0cc5e3c-7b8b-4d40-bd4b-9736ce1c3b99)



