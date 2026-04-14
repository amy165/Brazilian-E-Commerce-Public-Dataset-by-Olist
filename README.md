# 📊 E-commerce Analytics – Power BI Project

## Overview

This project started as a simple question: *What can we learn from real e-commerce data beyond the obvious KPIs?*

I took the Brazilian Olist dataset and built an end-to-end BI workflow in Power BI. The goal wasn't just to create dashboards, it was to simulate a real-world analytics scenario where **data quality issues are real**, and **business logic matters as much as visuals**.

Along the way, I found inconsistencies (payments with no orders, canceled orders with delivery dates, among others), validated assumptions, and applied advanced DAX to detect anomalies.

---

## 📂 Dataset

**Brazilian E-Commerce Public Dataset by Olist**  
🔗 [Kaggle link](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

Includes orders, payments, reviews, sellers, customers, and product data. A solid playground for realistic analysis.

---

## 🚀 What I Did

- Built **5 interactive dashboards** covering sales, sellers, customers, delivery experience, and financial validation  
- Found **$162K in payments without linked orders** — a data integrity red flag  
- Detected inconsistencies in order status and payment records  
- Used advanced DAX (`CALCULATE`, `FILTER`, `TREATAS`, `RANKX`) for validation and anomaly detection  
- Identified strong **Pareto patterns**: ~15% of sellers generate ~80% of revenue; ~94% of customers are one-time buyers

---

## 🧠 Business Questions I Wanted to Answer

- How is the platform performing over time?  
- Which sellers drive most revenue? Is it concentrated?  
- Do customers come back, or are they one-time buyers?  
- Does delivery speed affect review scores?  
- Are payments consistent with orders — or are there hidden gaps?

---

## 📊 Dashboards at a Glance

| Dashboard | Focus |
|-----------|-------|
| **Overview** | Revenue trends, order volume, geographic distribution, delivered vs total orders |
| **Seller Performance** | Revenue concentration (Pareto), seller contribution, delivery vs reviews |
| **Customer Performance** | One-time vs returning, revenue distribution across customers |
| **Customer Experience** | Delivery delays vs review scores, outliers |
| **Financial Validation** | Payment vs order reconciliation, anomaly detection |

---

## 🧩 Data Model Design

I used a **star schema** with separation between core data and analytical layers:

**Fact tables**  
- `Fact_Order_Items`  
- `Fact_Payment`  
- `Fact_Order_Review`

**Dimension tables**  
- `Dim_Orders`, `Dim_Customer`, `Dim_Sellers`, `Dim_Products`, `Dim_Date`

**Aggregated tables** (for performance)  
- `Agg_Customer`, `Agg_Seller`

---

## ⚠️ Data Challenges I Faced (and Solved)

| Issue | How I Handled It |
|-------|------------------|
| Canceled orders with payment & delivery data | Used *delivered date* as true completion indicator. Order status alone is not reliable — some canceled orders have delivery timestamps. |
| Payments without matching orders | 775 cases, ~$162K. Extreme discrepancies are driven by orders lacking item records, not true financial anomalies. |
| Canceled orders with payments | 455 orders, ~$105K impacted. Analyzed separately as edge cases, not included in core financial validation. |
| Multiple payments per order | Aggregated at order level before reconciliation. |

---

## 📈 Key Insights

- **~97%** of orders delivered  
- Revenue growth is steady  
- **~15% of sellers → ~80% of revenue**  
- **~94%** of customers are one-time buyers (repeat rate ~3%)  
- Delays correlate with lower review scores: average review drops from **4.2 (0–4 days)** to **3.0 (30+ days)**. In remote regions such as Amazonas (AM) and Amapá (AP), longer delivery times do not significantly impact customer satisfaction, indicating that expectations are influenced by geographic and logistical constraints. 
- Most payments are consistent, but anomalies exist and were documented. Payment discrepancies vary by method — voucher transactions show the highest variability.

---

## 🛠 Tools & Tech

- Power BI  
- DAX (`CALCULATE`, `FILTER`, `TREATAS`, `EXCEPT`, `RANKX`)  
- Star schema modeling  
- Data validation techniques  

---

## 📎 Notes on the Process

*I used AI assistance for refining complex DAX logic and structuring documentation. All analytical decisions, validation steps, and business interpretations are my own.*

---

## 📸 Dashboard Previews

| Overview | Seller Performance |
|----------|--------------------|
| ![Overview](https://raw.githubusercontent.com/amy165/Brazilian-E-Commerce-Public-Dataset-by-Olist/main/images/Overview.jpg) | ![Seller](https://raw.githubusercontent.com/amy165/Brazilian-E-Commerce-Public-Dataset-by-Olist/main/images/Seller.jpg) |

| Customer | Experience | Financial |
|----------|------------|----------|
| ![Customer](https://raw.githubusercontent.com/amy165/Brazilian-E-Commerce-Public-Dataset-by-Olist/main/images/Customer.jpg) | ![Experience](https://raw.githubusercontent.com/amy165/Brazilian-E-Commerce-Public-Dataset-by-Olist/main/images/Experience.jpg) | ![Financial](https://raw.githubusercontent.com/amy165/Brazilian-E-Commerce-Public-Dataset-by-Olist/main/images/Financial.jpg) |

---

## 📥 Access the Report

Due to file size limits, the `.pbix` file is hosted externally:

👉 [Download the full Power BI file (Google Drive)](https://drive.google.com/file/d/1TgmR5HlYsVgVYD5WUuVzNmza6x8wfeqe/view?usp=drive_link)

---

## 📊 Data Science – Customer Segmentation

This project includes a data science approach to customer segmentation using:

- KMeans clustering (baseline)
- Autoencoder + KMeans (improved approach)

👉 See full analysis here:
📁 /DS

[Go to Data Science analysis](./DS)


*This project reflects how I approach BI work: curiosity-driven, detail-oriented, and focused on real business value.*
