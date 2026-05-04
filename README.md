# 🛍️ Consumer Behaviour Analytics

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python) ![MySQL](https://img.shields.io/badge/MySQL-Database-4479A1?logo=mysql) ![PowerBI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?logo=powerbi) ![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

## 📌 Project Overview

An end-to-end data analysis project analyzing **3,900+ customer transactions** across various product categories to uncover spending patterns, customer segments, product preferences, and subscription behavior — supporting data-driven business decisions.

---

## 🎯 Objectives

- Identify purchasing patterns and key revenue drivers
- Segment customers based on purchase history
- Analyze discount dependency and its impact on margins
- Understand generational revenue contribution
- Build an interactive dashboard for business stakeholders

---

## 🗂️ Dataset Summary

| Property | Details |
|---|---|
| Rows | 3,900 |
| Columns | 18 |
| Missing Values | 37 (Review Rating column) |
| Database | MySQL |

**Key Features:** Customer demographics (Age, Gender, Location, Subscription Status), Purchase details (Item Purchased, Category, Purchase Amount, Season, Size, Color), Shopping behavior (Discount Applied, Promo Code Used, Previous Purchases, Frequency, Review Rating, Shipping Type)

---

## 🛠️ Tech Stack

| Tool | Usage |
|---|---|
| Python (Pandas, NumPy) | Data cleaning, EDA, feature engineering |
| MySQL | Structured SQL analysis |
| Power BI | Interactive dashboard |
| Excel | Supporting analysis |

---

## ⚙️ Project Workflow

### 1. Data Cleaning & Preparation (Python)
- Loaded dataset using `pandas`
- Used `df.info()` and `.describe()` for initial structure exploration
- Imputed 37 missing Review Rating values using **category-wise median**
- Renamed columns to snake_case for consistency and documentation
- Engineered `generation` column by binning customer ages
- Engineered `purchase_frequency_days` from purchase data
- Verified redundancy between `discount_applied` and `promo_code_used` — dropped `promo_code_used`
- Connected Python script to MySQL and loaded the cleaned DataFrame for SQL analysis

### 2. SQL Analysis (MySQL)
Wrote **10+ queries** using joins, subqueries, window functions, and aggregations to answer:

| # | Business Question | Key Result |
|---|---|---|
| 1 | Revenue by Gender | Male: $157,890 / Female: $75,191 |
| 2 | High-Spending Discount Users | Customers using discounts but spending above avg |
| 3 | Top 5 Products by Rating | Gloves (3.86), Sandals (3.84), Boots (3.82) |
| 4 | Shipping Type Comparison | Express: $60.48 / Standard: $58.46 avg spend |
| 5 | Subscribers vs Non-Subscribers | 2,847 non-subscribers vs 1,053 subscribers |
| 6 | Discount-Dependent Products | Hat (50%), Sneakers (49.66%), Coat (49.07%) |
| 7 | Customer Segmentation | Loyal: 3,116 / Returning: 701 / New: 83 |
| 8 | Top 3 Products per Category | Jewelry, Blouse, Sandals, Jacket top sellers |
| 9 | Repeat Buyers & Subscriptions | 2,518 repeat buyers are non-subscribers |
| 10 | Revenue by Generation | Gen X: $71,883 / Millennials: $69,301 |

### 3. Dashboard (Power BI)
Built an interactive dashboard with slicers for Gender, Location, Shipping Type, and Subscription Status.

---

## 📊 Key Findings

- **$233K total revenue** | **$59.76 average order value** | **3.75 avg. rating**
- **80% of customers are Loyal** (3,116), 18% Returning (701), only 2% New (83)
- **Gen X** is the highest revenue cohort at **$71,883**, followed by Millennials ($69,301)
- **2,518 repeat buyers hold no subscription** despite ~$59.87 consistent spend — high conversion opportunity
- **5 discount-dependent products** with ~48–50% discount rates impacting margins
- **Express shipping** users spend slightly more ($60.48) vs Standard ($58.46)
- **Fall season** drives the highest average sales ($0.062K per transaction)

---

## 💡 Business Recommendations

1. **Boost Subscriptions** — Target 2,518 loyal non-subscribers with exclusive subscriber benefits
2. **Customer Loyalty Programs** — Reward returning customers to push them into the Loyal segment
3. **Review Discount Policy** — Re-evaluate ~50% discount rates on top 5 products to protect margins
4. **Product Positioning** — Highlight top-rated products (Gloves 3.86, Sandals 3.84) in campaigns
5. **Targeted Marketing** — Focus on Gen X and Millennials; prioritize express-shipping users

---

## 📁 Repository Structure

```
consumer-behaviour-analytics/
│
├── data/
│   └── customer_shopping_data.csv
│
├── notebooks/
│   └── consumer_behaviour_EDA.ipynb
│
├── sql/
│   └── analysis_queries.sql
│
├── dashboard/
│   └── consumer_behaviour_dashboard.pbix
│
└── README.md
```

---

## 🖼️ Dashboard Preview

> *(Add a screenshot of your Power BI dashboard here)*

---

## 👤 Author

**Viren**
- 📧 dagarviren015@gmail.com
- 💼 [LinkedIn](https://linkedin.com/in/viren-dagar66a2463a0)
- 🐙 [GitHub](https://github.com/Viren-Dagar)
