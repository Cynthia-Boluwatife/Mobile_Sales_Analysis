Mobile-Sales-Analysis

## Overview:
**This is the sales report for Mobile Sales Product**
 
---

## Contents
[Project Overview](#Project-Overview)  |  [Dataset Source](#Dataset-Source)  |  [Tools used](#Tools-Used)  |  [Table Outlay](#Table-Outlay)  |  [Query Language](#Query-Language)  |  [Visuaization](#Visualization)

---
## Project Overview
> >This project analyzes the sales of Mobile Sales Products to uncover insights on sales distribution by various attributes such as Brands, Customer Gender and Payment Method, Using pivot tables, I explored metrics like Total Revenue Sales by Payment Method, Total Revenue Sales by Gender and their prefered Payment Method, Total Unit Sold by Payment Method and Total Unit sold by Gender, This analysis helps to understand the key factors driving sales in the dataset provided.

##  Dataset Source  
www.kaggle.com/dataset

## Tools Used  
+ **Power BI**
+ **Excel**  
+ **SQL**


## Table Outlay:

First Four Records:

|TransactionID| Date |MobileModel |Brand |Price |UnitsSold |TotalRevenue |CustomerAge |CustomerGender |Location |PaymentMethod
|----------------|----------------|----------------|----------------|----------------|----------------|----------------|----------------|----------------|----------------|----------------|
|79397f68-61ed-4ea8-bcb2-f918d4e6c05b |1/6/2024 |direction |Green Inc |1196.95 |85 |28002.8 |32 |Female |Port Erik |Online|
|4f87d114-f522-4ead-93e3-f336402df6aa |4/5/2024 |right |Thomas-Thompson |1010.34 |64 |2378.82 |55 |Female |East Linda |Credit Card|
|6750b7d6-dcc5-48c5-a76a-b6fc9d540fe1 |2/13/2024 |summer |Sanchez-Williams |400.8 |95 |31322.56 |57 |Male |East Angelicastad |Online|
|7da7de95-f772-4cc2-bce0-b0873f98233e |4/17/2024 |keep |Greer and Sons |338.6 |79 |31159.75 |46 |Other |East Kevin |Cash|

## Query Language
Some of teh query languages to retrieve records are displayed here

```SQL

---1. categorizing the data into silver,gold,diamond---

SELECT Price,
CASE
WHEN Price <= 500 THEN 'Silver' WHEN Price >= 500 THEN 'Gold'
ELSE 'Diamond'
END AS 'Ranking'
FROM [dbo].[mobile_sales];
---2. Retriving all female customer that bought goods with Price above 900 ---

SELECT CustomerGender,Price FROM  [dbo].[mobile_sales]
WHERE CustomerGender = 'Female' AND Price > 900;

---3. Retriving the sales by payment method arranging from largest to smallest amount---

SELECT PaymentMethod,SUM (TotalRevenue) AS Sales
FROM [dbo].[mobile_sales]
GROUP BY PaymentMethod
ORDER BY Sales DESC;

---4. Retrive the most expensive brand---

SELECT MAX (Price) AS Price,Brand FROM [dbo].[mobile_sales cvs]
GROUP BY Brand
ORDER BY Price DESC;

---5.How many brands are there---

SELECT COUNT (DISTINCT Brand) AS Num_of_Brand FROM [dbo].[mobile_sales];
```

## Visualization
### Pivot Tables

<img width="1621" height="692" alt="MOBILE DATASET PIVOT TABLE (EXCEL)" src="https://github.com/user-attachments/assets/0554b252-556a-4c96-b979-2feef888403e" />


### Charts

<img width="2185" height="1090" alt="MOBILE DATASET EXCEL VISUAL" src="https://github.com/user-attachments/assets/5ffde887-0bb0-410e-a6ef-e1ea35a33381" />


### SQL SINGLE VISUALS

<img width="1855" height="851" alt="SQL QUERY SHEET (Mobile dataset)" src="https://github.com/user-attachments/assets/6d79f439-8230-46e6-b9e2-bb0410179b00" />


### PowerBI Dashboard


### PowerBI Single Visual

#### Total Sales By customers


#### Total Sales By Age Category


#### Total Sales By Level of Preferred Payment Method, and Customer Gender


[View_my_Linkedin Profile](https://www.linkedin.com/in/cynthia-boluwatife)
