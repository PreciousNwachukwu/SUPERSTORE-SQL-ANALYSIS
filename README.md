# SUPERSTORE-SQL-ANALYSIS
This SQL based project analyzes the Superstore dataset to uncover insights on product profitability, regional performance, and customer segmentation. By using SQL queries to extract key trends, I provide data-backed recommendations for optimizing sales strategies and business growth.

## Table of Contents
1. [Project Overview](#project-overview)
2. [Project Scope & Business Objective](#project-scope--business-objective)
3. [Use Case & Data Source](#use-case--data-source)
4. [Dataset Overview](#dataset-overview)
5. [Data Analysis & Insights](#data-analysis--insights)
6. [Recommendations](#recommendations)
7. [Conclusion](#conclusion)

## Project Overview
In today’s data-driven business environment, organizations rely heavily on insights to improve performance. This project uses SQL to analyze a simulated retail dataset and uncover patterns that influence profitability and customer behavior.

## Project Scope & Business Objective
**Scope of the Analysis**  
This SQL-based project focuses on answering three critical business questions:  
- Which products generate the highest profit?  
- Which regions contribute the most to sales and profit?  
- Which customer segments are the most profitable?

**Business Objectives**
The goal is to transform raw sales data into strategic insights that:  
- Support inventory planning by focusing on profitable products.  
- Guide market expansion by identifying strong-performing regions.  
- Improve customer retention strategies by targeting high-value customer segments.  

These insights help businesses refine sales models, marketing strategies, and overall financial performance.

## Use Case & Data Source

**Use Case:**
- Helps retail analysts and business teams make data-informed decisions
- Demonstrates practical SQL skills: data extraction, transformation, and insight generation

**Data Source:**
- Dataset: Superstore Dataset (publicly available on Kaggle)
- Format: CSV
- Content: Transactional retail data including sales, profit, customer, and regional fields    

The dataset mirrors real world sales performance, making it ideal for practical analysis.

## Dataset Overview

| Column Name       | Description                                |
|-------------------|--------------------------------------------|
| Order ID          | Unique transaction ID                      |
| Order Date        | Date of purchase                           |
| Product Name      | Name of product sold                       |
| Category          | Product category                           |
| Sales             | Revenue generated                          |
| Profit            | Profit from each transaction               |
| Region            | Geographic region                          |
| Segment           | Type of customer (e.g., Consumer, Corporate)|

## Data Analysis & Insights

### 1. Top 10 Top-Performing Products by Profit
**SQL Query Used:**

```sql
SELECT TOP 10 Product_name,
ROUND(SUM(profit), 2) as Total_profit
FROM Superstore_dataset
GROUP BY Product_name
ORDER BY Total_profit DESC
```
**Visual Insight:**  

![](https://github.com/PreciousNwachukwu/SUPERSTORE-SQL-ANALYSIS/blob/main/top_10_profitable_products.jpg?raw=true)


**Result Table:**

| Product Name                                               | Total Profit |
| ---------------------------------------------------------- | ------------ |
| Canon imageCLASS 2200 Advanced Copier                      | $25,199.93    |
| Fellowes PB500 Electric Punch Plastic Comb Binding Machine | $7,753.04     |
| Hewlett Packard LaserJet 3310 Copier                       | $6,983.88     |
| Canon PC1060 Personal Laser Copier                         | $4,570.93     |
| HP Designjet T520 Inkjet Large Format Printer - 24" Color  | $4,094.98     |
| Ativa V4110MDD Micro-Cut Shredder                          | $3,772.95     |
| 3D Systems Cube Printer, 2nd Generation, Magenta           | $3,717.97     |
| Plantronics Savi W720 Multi-Device Wireless Headset System | $3,696.28     |
| Ibico EPK-21 Electric Binding System                       | $3,345.28     |
| Zebra ZM400 Thermal Label Printer                          | $3,343.54     |

**Insight:**  
-	**These products yield the highest profit margins.**
-	**Focusing on them in inventory planning and promotions can significantly boost revenue.**



### 2. Top-Performing Regions by Profit & Sales
**SQL Query Used:**

```sql
SELECT Region,                                  
ROUND(SUM(profit), 2) AS Total_profit,
ROUND(SUM(sales), 2) AS Total_sales
FROM Superstore_dataset
GROUP BY Region
ORDER BY Total_profit DESC, Total_sales DESC
```
**Visual Insight:**    
![](https://github.com/PreciousNwachukwu/SUPERSTORE-SQL-ANALYSIS/blob/main/top_regions_profit_sales.jpg)


**Result Table:**
| Region  | Total Profit | Total Sales |
| ------- | ------------ | ------------ |
| West    | $108,418.45  | $725,457.82  |
| East    | $91,522.78   | $678,781.24  |
| South	  | $47,169.43   | $391,721.91  |
| Central | $39,706.36   | $501,239.89  |

**Insight:**   
-	**The West and East regions lead in both profit and sales, making them highly strategic markets for growth.**
-	**South and Central show moderate performance, which may benefit from improved marketing and distribution efforts.**
- **Focusing marketing campaigns and operational investments on top-performing regions can maximize returns.**


### 3.	Top-Performing Customer Segments
**SQL Query Used:**

```sql
SELECT Segment,
ROUND(SUM(profit), 2) AS Total_profit
FROM Superstore_dataset
GROUP BY Segment
ORDER BY Total_profit DESC
```
**Visual Insight:**  

![](https://github.com/PreciousNwachukwu/SUPERSTORE-SQL-ANALYSIS/blob/main/most_profitable_customer_segments.jpg)


**Result Table:**

| Segment  | Total Profit |
| ------- | ------------ | 
| Consumer  | $134,119.21 | 
| Corporate | $92,399.13  | 
| Home	    | $60,298.68  | 

**Insight:**  
-	**The Consumer segment generates the highest overall profit, indicating strong purchasing activity and engagement.**
-	**Corporate and Home segments also show solid contributions, but with lower margins.**
- **Tailoring offers, loyalty programs, or upselling strategies for top-performing customer groups can boost long term value.**


## Recommendations

Based on the insights gathered, here are strategic recommendations:  
 **1. Invest in High-Profit Products:**  
-	Focus inventory and promotions around the top 10 most profitable products.
   
**2. Expand in Profitable Regions:**  
-	Channel marketing and operational resources to high-performing regions.

**3. Target High-Value Customer Segments:**  
-	Design loyalty programs or upsell offers for the most profitable customer groups.

## Conclusion

This project demonstrates how SQL can uncover valuable insights from retail data. By analyzing product performance, customer segments, and regional trends, businesses can make informed decisions that enhance revenue and operational efficiency.  
Additionally, this project serves as a demonstration of practical SQL skills, highlighting:  
-	Query optimization for extracting business-critical insights
-	Translating raw data into strategic actions
-	Structuring data to support business intelligence efforts  

This analysis demonstrates the value of SQL in business decision-making. As data continues to shape corporate strategies, leveraging SQL-driven insights will remain a competitive advantage.


























