📊 Online Retail Sales EDA Project
🛍️ Exploratory Data Analysis of UK-Based E-Commerce Transactions (2010–2011)

📌 Table of Contents
Overview

Dataset

Objectives

Technologies Used

Data Cleaning

Exploratory Data Analysis (EDA)

Key Insights

Visualizations Used

Visual Summary Dashboard

RFM Segmentation

Power BI Dashboard

How to Run

License

📖 Overview
This project presents a comprehensive Exploratory Data Analysis (EDA) of a real-world online retail dataset. The primary goal is to uncover business insights by analyzing customer purchasing behavior, product performance, time-based sales trends, country-level sales, and customer segmentation using RFM analysis.

📁 Dataset
Source: Kaggle – Online Retail Dataset

Scope: UK-based transactions from Dec 2010 to Dec 2011

Size: ~500,000 rows

Key Columns:

InvoiceNo, StockCode, Description

Quantity, UnitPrice, InvoiceDate

CustomerID, Country

🎯 Objectives
Clean and preprocess real-world e-commerce data

Perform EDA (univariate, bivariate, and multivariate analysis)

Identify top products and customer trends

Analyze time-based and country-wise sales

Perform RFM segmentation of customers

Visualize findings using Python and Power BI

🛠️ Technologies Used
Python (Jupyter Notebook):

Pandas, NumPy

Matplotlib, Seaborn

Power BI (for interactive dashboards)

Git & GitHub (for version control)

🧹 Data Cleaning
Performed the following steps:

Dropped rows with missing CustomerID or Description

Removed duplicate records

Excluded canceled invoices (InvoiceNo starting with "C")

Removed or capped outliers in Quantity and UnitPrice using IQR

Converted InvoiceDate to datetime format

Created new features: TotalPrice, InvoiceMonth, DayOfWeek

🔍 Exploratory Data Analysis (EDA)
🔢 General Overview
Unique Products: 3,900+

Unique Customers: 4,300+

Total Transactions: 18,000+

Countries Involved: 37

📈 Key Insights
🛒 Product Analysis
Top 10 products by quantity sold and total revenue

Few products had zero or negative prices, flagged as anomalies

👥 Customer Analysis
Top buyers by volume

Loyal customers identified (30+ transactions)

Clear skew in customer purchase distribution

🗓️ Time Series Trends
Peak Month: November 2011

Slowest Month: February 2011

Sales highest mid-week (Tuesdays to Thursdays)

🌍 Country-Wise Analysis
UK accounted for the majority of orders

Top non-UK countries: Netherlands, Germany, France

📊 Visualizations Used
Visualization Type	Purpose
Bar Chart	Compare quantities, revenue, customer counts, top countries/products
Line Chart	Show monthly sales trend over time
Histogram	Distribution of customer purchases
Box Plot	Identify outliers in purchase frequency
Scatter Plot	Visualize RFM Segments (Recency vs Frequency vs Monetary)
Treemap (Power BI)	Show product/category sales proportions
Map (Power BI)	Display geographical sales distribution
KPI Cards	Display total customers, revenue, transactions
Table Visuals	Display RFM customer attributes and summary

Each visualization was chosen to emphasize insights in an intuitive and visually clear manner.

📊 Visual Summary Dashboard
A combined figure built in Matplotlib that shows:

Total KPIs (Products, Customers, Transactions)

Monthly Revenue Line Chart

Top Selling Products (Bar Chart)

RFM Score Distribution (Bar Chart)

📍 Located in notebooks/eda_dashboard.ipynb

📈 RFM Segmentation
Used Recency, Frequency, and Monetary metrics to score customers from 1 to 4:

VIP Customers: RFM Score ≥ 10

Churn Risk: RFM Score ≤ 5

Segmented visually using scatter plots and histograms

Segment column added to customer data

📍 RFM results saved in rfm_scores.csv

🧠 Power BI Dashboard
Built an interactive .pbix dashboard containing 4 pages:

1. Sales Overview
KPIs: Revenue, Transactions, Unique Customers

Monthly Sales Line Chart

2. Top Products
Bar Charts for Top 10 by Quantity and Revenue

Treemap of product performance

3. Customer Segments
RFM Table

Scatter plot of VIP and Churn-risk customers

4. Geographical Insights
Sales by country using map and bar chart.

📝 License
This project is licensed under the MIT License. Feel free to use and adapt it with attribution.
