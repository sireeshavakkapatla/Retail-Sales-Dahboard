<img width="1194" height="785" alt="image" src="https://github.com/user-attachments/assets/f1263d42-2727-45aa-b4e9-efa38b8686d0" />
<img width="1175" height="782" alt="image" src="https://github.com/user-attachments/assets/0c975f6b-6616-4995-87bd-19115af93b1b" />
<img width="1187" height="789" alt="image" src="https://github.com/user-attachments/assets/047f35c2-f9bc-451a-8031-6cd7d0219584" />

https://app.powerbi.com/groups/me/reports/8fa9b8a4-5b36-41ff-8883-29d7d7a48734/0a4385dc115516e880b1?ctid=dbec8e00-2ea4-4a47-bd9a-ffcb2046d9d5&experience=power-bi&bookmarkGuid=2b3cba76-58f1-4236-9c1e-a944d71bbdae

# 🛒 Retail Sales Dashboard — Power BI

An end-to-end interactive sales analytics dashboard built in Power BI, analysing **$16M in retail revenue** across 4 product categories and 6 countries — with full Year-on-Year performance tracking, customer segmentation, and drill-through reporting.

---

## 📌 Project Overview

This dashboard was built to give retail business stakeholders a single, self-service view of sales performance — replacing manual Excel reporting with dynamic, filterable insights across revenue, profit, orders, and customer behaviour.

| | |
|---|---|
| **Tool** | Microsoft Power BI Desktop |
| **Data Model** | Star Schema (1 Fact + 3 Dimensions + Date Table) |
| **Pages** | 3 (Sales Overview · Customer Analysis · Order Details) |
| **Time Period** | 2010–2014 (primary focus: 2013) |
| **Key Metrics** | $16M Sales · 53K Orders · $7M Profit · 179% YoY Growth |

---

## 📊 Dashboard Pages

### 1. Sales Overview
KPI cards for Total Sales, Orders, Average Order Value, and Profit — each with a dynamic YoY badge (green/red). Includes a category tab slicer, revenue trend line (monthly), and bar charts for category and subcategory comparisons.

### 2. Customer Data Analysis
Sales by country, customer segmentation (Low/Medium/High), orders and sales by quarter, age group distribution, and breakdowns by gender and marital status.

### 3. Order Details
Drill-through matrix by Category → Country showing Total Sales, YOY Sales (with conditional formatting), Profit, Profit %, and inline sparklines for monthly trend.

---

## 🗂️ Data Model

Star schema with the following tables:

- **`gold fact_sales`** — Transactional fact table (sales_amount, sales_quantity, sales_price, order_date, customer_key, product_key)
- **`gold dim_products`** — Category, subcategory, product name, cost
- **`gold dim_customers`** — Age, age group, country, gender, marital status, segment
- **`dim_date`** — Date, year, month, month_num, mon_year
- **`_measures`** — Isolated DAX measures table (best practice)

All relationships are **Many-to-One**, **single-direction** filters from fact → dimension.

---

## 🧮 Key DAX Measures

| Measure | Purpose |
|---|---|
| `Total sales` | Base revenue aggregation |
| `last year sales` | SAMEPERIODLASTYEAR time intelligence |
| `YOY sales` / `YoY %` | Absolute and % growth vs prior year |
| `profit` / `profit %` | Gross profit and margin rate |
| `profit_contribution` | % share of total profit using ALL() |
| `cf_profit` / `cf_avgordervalue` | Conditional format flags for KPI badges |
| `YOY KPI` | Formatted arrow + % string for card display |

---

## 💡 Key Insights

- 📈 Revenue grew **179.8% YoY** to $16M; profit grew **228.8%** to $7M
- 🚲 **Bikes** dominate revenue, but **Accessories carry 63% profit margins** — a margin mix-shift opportunity
- 🌏 **Australia ($4.3M)** is nearly on par with the US ($5.2M) — an underinvested high-growth market
- 👥 **81.6% of customers are in the Low segment** — significant LTV upside in segment upgrade programmes
- 👴 The **60+ age group** is the largest customer cohort (6.5K) — messaging should reflect this

---

## 🛠️ Skills Demonstrated

`Power BI` · `DAX` · `Star Schema Modelling` · `Time Intelligence` · `Data Visualisation` · `Conditional Formatting` · `Drill-through` · `KPI Design` · `Customer Segmentation`

---

*Built by [https://www.linkedin.com/in/vakkapatla-sireesha14/) — Data & Reporting Analyst, Melbourne AU*
