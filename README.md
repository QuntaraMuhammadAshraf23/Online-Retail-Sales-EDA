---

# 📊 Online Retail Sales EDA Project

🛍️ **Exploratory Data Analysis (EDA) of UK-Based E-Commerce Transactions (2010–2011)**
**📈 + 📉 + 📍 + 🧠 with Python and Power BI**

---

## 📌 Table of Contents

* [Overview](#overview)
* [Dataset](#dataset)
* [Objectives](#objectives)
* [Technologies Used](#technologies-used)
* [Data Cleaning](#data-cleaning)
* [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
* [Visualizations Used](#visualizations-used)
* [Power BI Dashboard](#power-bi-dashboard)
* [How to Run](#how-to-run)
* [License](#license)

---

## 📖 Overview

This project is a comprehensive **Exploratory Data Analysis (EDA)** of an **e-commerce dataset** using **Python** and **Power BI**. The goal is to uncover insights about **customer behavior**, **product performance**, and **sales trends**, and to build a **dynamic dashboard** for business stakeholders using **interactive visuals and KPIs**.

---

## 📁 Dataset

* **Source:** [Kaggle – Online Retail Dataset](https://www.kaggle.com/datasets/lakshmi25npathi/online-retail-dataset)
* **Scope:** Covers **UK-based** transactions from **Dec 2010 to Dec 2011**
* **Size:** \~500,000 rows
* **Columns:**

  * `InvoiceNo`, `StockCode`, `Description`
  * `Quantity`, `UnitPrice`, `InvoiceDate`
  * `CustomerID`, `Country`

---

## 🎯 Objectives

* Clean and preprocess real-world e-commerce data
* Perform detailed EDA on products, customers, countries, and time
* Apply RFM segmentation to classify customer types
* Visualize key findings using Matplotlib, Seaborn, and Power BI
* Create a professional, interactive business dashboard

---

## 🛠️ Technologies Used

* **Python:** Pandas, NumPy, Matplotlib, Seaborn
* **Power BI Desktop:** Interactive visualizations and dashboards
* **Jupyter Notebook:** Data cleaning and analysis
* **Git & GitHub:** Version control and collaboration

---

## 🧹 Data Cleaning

* Handled missing values in `CustomerID` and `Description`
* Removed duplicate and cancelled orders (`InvoiceNo` starting with "C")
* Filtered out outliers using **IQR method** on `Quantity` and `UnitPrice`
* Converted `InvoiceDate` to datetime
* Engineered new columns:

  * `TotalPrice = Quantity × UnitPrice`
  * `InvoiceMonth`, `DayOfWeek`

---

## 🔍 Exploratory Data Analysis (EDA)

### General Overview

* **Unique Products:** \~3,900
* **Unique Customers:** \~4,300
* **Total Transactions:** \~18,000
* **Countries Involved:** 37

### Product Analysis

* Identified **top 10 products** by quantity and revenue
* Highlighted products with **zero or negative price**
* Detected **skew** in sales volume per item

### Customer Analysis

* Identified **most frequent buyers**
* Analyzed **distribution of purchases** per customer
* Detected **loyal customers** (30+ transactions)

### Time Series Analysis

* **Monthly Revenue Trend**: Peaks in **November 2011**, dips in **February 2011**
* **Weekday Patterns**: Highest sales from **Tuesday to Thursday**

### Country-wise Analysis

* UK contributes the **highest revenue**
* **Top non-UK countries**: Netherlands, Germany, France
* Bottom 10 countries analyzed for improvement opportunities

---

## 📊 Visualizations Used

| Visualization Type | Purpose                                                  |
| ------------------ | -------------------------------------------------------- |
| **Card (KPI)**     | Show totals: Revenue, Customers, Transactions, Countries |
| **Bar Chart**      | Compare top & bottom products and countries              |
| **Line Chart**     | Visualize monthly sales trend                            |
| **Box Plot**       | Outlier detection in purchase quantity                   |
| **Histogram**      | Customer purchase distribution                           |
| **Scatter Plot**   | RFM customer segmentation                                |
| **Treemap / Pie**  | Revenue share by product or country                      |
| **Map**            | Geographical distribution of sales                       |
| **Table**          | Show RFM customer details                                |

---

## 📈 Power BI Dashboard

### 📄 Dashboard Pages & Visuals

---

### 🧾 **Page 1: Sales Overview**

* **KPI Cards:**

  * Total Revenue
  * Unique Customers
  * Total Transactions
* **Line Chart:** Monthly Revenue Trend
* **Clean formatting**, currency (₤), rotated axes, bold titles

---

### 🛒 **Page 2: Top Products**

* **Bar Charts** for:

  * Top 10 Products by Quantity
  * Top 10 Products by Revenue
* **Treemap** or **Pie Chart** for product contribution breakdown

---

### 👥 **Page 3: Customer Segmentation (RFM)**

* **Table:** Displays `Customer ID`, `Recency`, `Frequency`, `Monetary`, `RFM Score`
* **Scatter Plot:**

  * X = Recency
  * Y = Frequency
  * Size = Monetary
  * Color = RFM Segment (e.g., VIPs, Churn Risks)
* **Bar Chart:** Distribution of customers by RFM score

---

### 🌍 **Page 4: Geographical Insights**

* **Map:** Revenue by Country (bubble or filled)
* **Bar Chart:** Top 10 countries by revenue
* **Pie Chart:** Bottom 10 countries by revenue
* **KPI Card:** Number of countries involved

---

## ▶️ How to Run

### Clone the Repo

```bash
git clone https://github.com/your-username/online-retail-eda.git
cd online-retail-eda
```

### Launch Notebook for EDA

```bash
pip install -r requirements.txt
jupyter notebook notebooks/eda_online_retail.ipynb
```

### Open Power BI Dashboard

* Open `powerbi/OnlineRetailDashboard.pbix` using **Power BI Desktop**
* Explore the interactive pages

---

## 📁 Repository Structure

```
online-retail-eda/
├── notebooks/
│   └── eda_online_retail.ipynb               # Python-based EDA
├── csv files/
│   ├── cleaned_online_retail.csv             # Cleaned main dataset
│   └── rfm_scores.csv                        # Customer segmentation data
├── powerbi/
│   └── OnlineRetailDashboard.pbix            # PowerBI Dashboard
├── images/                                   # Contains PowerBI Dashboard SS 
│   ├── sales_overview.png                    # Screenshot of Page 1
│   ├── top_products.png                      # Screenshot of Page 2
│   ├── customer_segmentation.png             # Screenshot of Page 3
│   ├── geographical_insights.png             # Screenshot of Page 4
├── README.md                                 # Project documentation
└── LICENSE                                   # MIT License

```

---

## 📝 License

This project is licensed under the **MIT License**.
You are free to use, share, and modify it — just give proper attribution.
See the `LICENSE` file for full terms.
