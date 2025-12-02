# Customer Shopping Behavior Analysis

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/MySQL-316192?style=flat&logo=postgresql&logoColor=white)
![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=flat&logo=powerbi&logoColor=black)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)

## 📋 Project Overview

This project analyzes customer shopping behavior using transactional data from **3,900 purchases** across various product categories. The goal is to uncover insights into spending patterns, customer segments, product preferences, and subscription behavior to guide strategic business decisions.

## 📊 Dataset Summary

| Feature | Details |
|---------|---------|
| **Rows** | 3,900 |
| **Columns** | 18 |
| **Missing Data** | 37 values (Review Rating) |

### Key Features

- **Customer Demographics:** Age, Gender, Location, Subscription Status
- **Purchase Details:** Item Purchased, Category, Purchase Amount, Season, Size, Color
- **Shopping Behavior:** Discount Applied, Promo Code Used, Previous Purchases, Frequency of Purchases, Review Rating, Shipping Type

## 🔧 Methodology

### 1. Exploratory Data Analysis (Python)

- **Data Loading & Exploration:** Imported dataset using pandas, checked structure with `df.info()` and summary statistics with `.describe()`
- **Missing Data Handling:** Imputed missing values in Review Rating using median rating per product category
- **Column Standardization:** Renamed columns to `snake_case` for consistency
- **Feature Engineering:**
  - Created `age_group` column by binning customer ages
  - Created `purchase_frequency_days` from purchase data
- **Data Consistency:** Verified redundancy between `discount_applied` and `promo_code_used`; dropped redundant column
- **Database Integration:** Connected to PostgreSQL and loaded cleaned DataFrame

### 2. SQL Analysis (MySQL)

Performed structured queries to answer key business questions:

| # | Analysis | Key Finding |
|---|----------|-------------|
| 1 | Revenue by Gender | Male: $157,890 \| Female: $75,191 |
| 2 | High-Spending Discount Users | Identified customers using discounts but spending above average |
| 3 | Top 5 Products by Rating | Gloves (3.86), Sandals (3.84), Boots (3.82), Hat (3.80), Skirt (3.79) |
| 4 | Shipping Type Comparison | Express: $60.48 avg \| Standard: $58.46 avg |
| 5 | Subscribers vs Non-Subscribers | Subscribers: 1,053 customers, $59.49 avg \| Non-subscribers: 2,847, $59.87 avg |
| 6 | Discount-Dependent Products | Hat (50%), Sneakers (49.66%), Coat (49.07%) |
| 7 | Customer Segmentation | Loyal: 3,116 \| Returning: 701 \| New: 83 |
| 8 | Top 3 Products per Category | Ranked best-sellers within each category |
| 9 | Repeat Buyers & Subscriptions | Analyzed subscription likelihood for 5+ purchases |
| 10 | Revenue by Age Group | Young Adult: $62,143 \| Senior: $59,197 \| Adult: $55,978 |

### 3. Dashboard (Power BI)

Built an interactive dashboard featuring:

- KPI cards (Customers, Avg Purchase, Avg Rating)
- Subscription status distribution
- Revenue & Sales by Category
- Revenue & Sales by Age Group
- Dynamic filters (Gender, Category, Shipping Type)

## 💡 Business Recommendations

1. **Boost Subscriptions** — Promote exclusive benefits for subscribers
2. **Customer Loyalty Programs** — Reward repeat buyers to convert them into "Loyal" segment
3. **Review Discount Policy** — Balance sales boosts with margin control
4. **Product Positioning** — Highlight top-rated and best-selling products in campaigns
5. **Targeted Marketing** — Focus on high-revenue age groups and express-shipping users

## 🛠️ Tech Stack

- **Python** (pandas, numpy) — Data cleaning & feature engineering
- **MySQL** — Structured data analysis
- **Power BI** — Interactive visualization






