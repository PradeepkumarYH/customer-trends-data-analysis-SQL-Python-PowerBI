# Customer Shopping Behavior Analysis

## Overview
This project covers a complete end-to-end data analytics workflow analyzing customer behavior for a retail company. The goal is to uncover purchasing patterns across demographics, product categories, and sales channels to improve customer engagement and optimize marketing strategies.

---

## Dataset
Each row represents a customer's latest purchase. Key attributes include:

- **Demographics:** Customer ID, Age, Gender
- **Purchase Details:** Item Purchased, Category, Purchase Amount, Size, Color, Season, Review Rating
- **Behavior & Channels:** Location, Subscription Status, Shipping Type, Discount Applied, Previous Purchases, Payment Method, Frequency of Purchases

---

## Tools Used
- **Python** (Pandas, SQLAlchemy) — Data cleaning, EDA, and database connection
- **PostgreSQL** — Advanced SQL analysis
- **Power BI** — Interactive dashboard
- **Gamma AI** — Presentation deck generation

---

## Project Workflow

### 1. Data Cleaning & Feature Engineering (Python)
- Replaced missing `review_rating` values using median rating per item category
- Converted all column names to `snake_case` for SQL compatibility
- Created an `age_group` column (Young Adult, Adult, Middle-Aged, Senior) using `pd.qcut`
- Mapped `frequency_of_purchases` text values into a numeric `purchase_frequency_days` column
- Dropped `promo_code_used` column (duplicate of `discount_applied`)
- Loaded cleaned data into PostgreSQL using SQLAlchemy

### 2. Advanced SQL Analysis (PostgreSQL)
Used CTEs, CASE statements, and Window Functions (ROW_NUMBER) to answer:
- Total revenue comparison between male and female customers
- Top 5 products by average review rating
- Average purchase amount difference between standard vs express shipping
- Impact of subscription status on average spend and total revenue
- Customer segmentation into New, Returning, and Loyal based on purchase history
- Top 3 most purchased products within each category
- Total revenue across different age groups

### 3. Interactive Dashboard (Power BI)
Connected directly to PostgreSQL to visualize:
- **KPI Cards:** Total Customers, Average Purchase Amount, Average Review Rating
- **Charts:** Revenue by Category, Sales by Category, Revenue & Sales by Age Group
- **Donut Chart:** Subscription Status breakdown
- **Slicers:** Filter by Subscription Status, Gender, Category, Shipping Type

### 4. Reporting & Presentation
- Documented the full technical workflow in a project report
- Used Gamma AI to convert the report into a client-ready presentation deck

---

## Author
**Pradeepkumar Hejjegar**
- GitHub: [PradeepkumarYH](https://github.com/PradeepkumarYH)
- Email: pradeephejjegar@gmail.com
