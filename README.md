# 📊 Tech Sales Analysis Dashboard

## Introduction

This project explores technology sales data using Microsoft Power BI to examine revenue, costs, profit, product performance, and customer characteristics. The report brings together sales, product, and customer information in an interactive dashboard. It uses KPI cards, charts, and slicers to help users explore business performance across product brands, colours, customer income levels, regions, and sales dates.

The project demonstrates the use of Power Query for data preparation, data modelling, DAX measures, and Power BI visualisations to transform raw data into a business reporting tool.

## Problem Statement

Businesses need a clear understanding of their sales performance to identify strong-performing products, monitor costs, evaluate profitability, and understand customer purchasing patterns. However, raw sales records alone can make it difficult to compare performance across different product and customer categories.

This project addresses that challenge by developing an interactive Power BI report that consolidates sales, product, and customer data into a single view for business performance analysis.

## Business Questions
The analysis focuses on the following questions:
 1. What is the total revenue generated from technology sales?
 2. What are the total costs and overall profit?
 3. Which product brands contribute the most to sales profit?
 4. How does total cost vary across product colours?
 5. How does profit differ across customer income levels?
 6. How does revenue change across the available sales dates and months?
 7. How do sales and profit vary across customer regions?
 8. How can users explore performance for individual product categories and customer regions?

## Data Source
The project uses an Excel workbook containing the following tables:

**Sales:** 5,200 rows and 7 columns containing sale ID, product ID, customer ID, quantity, sale date, sales amount, and unit cost

**Products:** 250 rows and 6 columns containing product ID, product name, category, brand, colour, and weight

**Customers:** 250 rows and 7 columns containing customer ID, name, region, age, gender, income level, and signup date

The sales, products, and customers tables provide the information required to analyse transactions alongside product attributes and customer characteristics.


## Tools Used
 **• Microsoft Power BI Desktop:** Report development, data modelling, interactive visualisations, and dashboard design.
 
 **• Power Query:** Data import, inspection, cleaning, and preparation.

 **• DAX (Data Analysis Expressions):** Creation of measures used to calculate and display business performance indicators.

 **• Microsoft Excel:** Source data storage and initial inspection.


## Data Cleaning and Preparation
Data preparation is an important part of this project because inconsistencies in the source data can affect calculations, relationships, and visualisations. The data was inspected table by table, with attention to missing values, duplicate records, inconsistent text formatting, data types, and relationships between tables.

### Data Quality Checks
The initial inspection identified the following:
 **• Missing values:** No blank data cells were found in the three main data tables.
 
 **• Duplicate records:** No exact duplicate rows were identified in the initial inspection of the three tables.

 **• Region inconsistencies:** The customer table contains both North and north, indicating inconsistent capitalisation and extra whitespace.

 **• Gender inconsistencies:** The customer table contains both Female and female, which should be standardised for consistent reporting.

 **• Date formatting:** The sales table contains dates represented in both YYYY-MM-DD and YYYY/MM/DD formats. The customer signup dates also use mixed date formats.

 **• Relationship checks:** The product IDs and customer IDs in the sales table were checked against their corresponding lookup tables. No unmatched IDs were identified in the initial inspection.

### Power Query Preparation
Power Query provides the environment for preparing the source data before analysis. The relevant preparation tasks for this dataset include:
 1. Importing the sales, products, and customers tables from the Excel workbook.
 2. Checking column names and assigning appropriate data types.
 3. Standardising text values by removing unnecessary whitespace and correcting inconsistent capitalisation.
 4. Converting sales dates and customer signup dates into consistent date values.
 5. Checking for missing values, duplicate records, and invalid identifiers.
 6. Preparing the tables for relationships and analysis in Power BI.
These checks help ensure that customer regions, gender categories, and dates can be analysed consistently.


## Data Analysis
The Power BI report contains KPI cards, charts, and interactive slicers that support exploration of the available sales data.
### 1. Key Performance Indicators
The dashboard displays four main performance indicators:
 **• Total Revenue:** Measures sales revenue across the selected data.
 **• Total Cost:** Summarises the costs represented by the source data and the report’s measure.
 **• Profit:** Presents the profit measure used in the report.
 **• Total Customers:** Displays the customer count.
These indicators provide a high-level overview of business performance.

### 2. Profit by Brand
A clustered column chart compares profit across product brands.
This visual helps users identify brands contributing more or less profit and compare performance across the six brands represented in the source data: Apple, Samsung, Lenovo, HP, Asus, and Dell.

### 3. Total Cost by Product Colour
A clustered bar chart compares total cost across product colours.
The visual provides a way to examine how costs are distributed among the colour categories in the product data.

### 4. Revenue Across Time
The report includes two revenue-related time visuals:
 • A combination chart using the year level of the sales date hierarchy.
 • A line chart using the month level of the sales date hierarchy.
These visuals are intended to support the exploration of revenue over time. The source sales records contain three distinct dates in January, February, and March 2023.

### 5. Profit by Customer Income Level
A pie chart compares profit across customer income levels: Low, Medium, and High.
This helps users explore how profit is distributed across the income categories recorded in the customer table.

### 6. Interactive Filtering
The dashboard includes two slicers:
 • Region: Filters the report by customer region.
 • Product: Filters the report by product name.
These controls allow users to explore the report from different business perspectives without creating separate reports for each selection.


## Key Insights and Findings
The following findings were calculated from the data’s sales records. They are source-data summaries and should be distinguished from the exact values displayed by the Power BI measures.
**1. Overall Sales:** The data contains 5,200 sales records with a combined SalesAmount of **1,034,150** in the dataset’s recorded monetary units.

 **2. Brand Performance:** Apple has the highest aggregated sales amount of **217,500**, while Dell has the lowest sales amount of **139,500** among the six brands.
These figures represent sales amount, not the profit-by-brand values shown in the dashboard.

**3. Product Performance:** Headphones recorded the highest aggregated sales amount of **182,800**, followed by monitors **(181,200)** and tablets **(171,900)**. Phones recorded the lowest sales of **118,350**.

**4. Customer Income Levels:** Customers in the Medium income category account for the highest aggregated sales amount of **381,950** while Low income category account for the lowest sales amount of **316,600**.

**5. Regional Sales:** North has the highest sales amount of **323,900** among the region labels. West is being recorded as the lowest sales amount of **215,250**. 

**6. Sales Dates:** These are comparisons between three distinct dates; 1 January 2023, 10 March 2023, and 15 February 2023 not a complete month-by-month sales trend. Among these dates, 10 March 2023 has the highest aggregated sales amount of **346,000**, while 15 February 2023 has the lowest sales amount of **343,500**.

## Recommendations 
Based on the source-data findings and the report’s analytical focus, the following actions are recommended:
 **1. Investigate brand performance:** Examine the profit-by-brand visual to identify brands that contribute the most profit, rather than relying on sales amount alone.
 
 **2. Review product performance:** Investigate the sales and cost patterns of headphones, monitors, and tablets to understand their contribution to overall business results.
 
 **3. Standardise customer data:** Correct inconsistent region labels and gender values before producing final customer segment comparisons.
 
 **4. Standardise date fields:** Convert sales and signup dates into proper date data types to support reliable time-based analysis.

 **5. Monitor costs and profitability:** Compare the Total Revenue, Total Cost, and Profit indicators to assess financial performance.

 **6. Explore regional differences:** Use the region slicer to compare performance across customer locations after standardising the region labels.

 **7. Use the dashboard for further investigation:** Apply the product slicer to examine how selecting individual products affects the report’s performance indicators and charts.

## Conclusion
The Tech Sales Analysis project demonstrates how Excel data can be prepared and analysed in Power BI to support business reporting. By combining sales transactions with product and customer information, the report provides a consolidated view of revenue, cost, profit, brand performance, and customer income segments. Its KPI cards, charts, and slicers allow users to explore different aspects of the data interactively.

The project also highlights the importance of data quality. Inconsistent text values and date formats need to be addressed to ensure reliable analysis and reporting. Overall, this project demonstrates practical skills in data inspection, Power Query preparation, data modelling, DAX-based reporting, and Power BI dashboard development.
