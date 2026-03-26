# 📊 E-commerce Analytics – End-to-End Power BI Project

## Project Overview

An end-to-end Business Intelligence project analyzing an e-commerce dataset using Power BI.

The objective was to simulate a real-world BI scenario, focusing on:

- Data consistency and validation
- Customer and seller behavior
- Delivery performance
- Financial integrity

This project goes beyond dashboards — it emphasizes analytical thinking and data reliability.

---

## 📂 Dataset

This project uses the **Brazilian E-Commerce Public Dataset by Olist**, available on Kaggle.

- **Source:** [https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)
- **Provider:** Olist

The dataset includes:
- Orders and order items
- Payments
- Customer reviews
- Sellers and customers
- Products and categories

---

## 🚀 Project Highlights

- 📊 Built **5 fully interactive dashboards** covering key business domains
- 🔍 Identified **$162K in payments without linked orders** (775 orders with payment but no order items)
- ⚠️ Detected **data inconsistencies**: canceled orders with delivery timestamps, delivered orders without delivery dates
- 🧠 Applied **advanced DAX** for anomaly detection and validation
- 📈 Revealed strong **Pareto effects**: ~12–16% of sellers generate ~80% of revenue

---

## 🧭 Business Questions Addressed

### Platform Performance
- How is the platform performing overall?
- How are revenue and orders evolving?

### Seller Dynamics
- Which sellers generate most of the revenue?
- Is revenue concentrated?

### Customer Behavior
- Are customers returning or one-time buyers?
- How is revenue distributed across customers?

### Customer Experience
- Does delivery impact review scores?
- Are delays a key factor?

### Financial Consistency
- Do payments match order values?
- Are there inconsistencies in transactions?

---

## 📊 Dashboard Structure

### 1. Overview
- Orders, revenue, and delivery trends
- Geographic distribution
- Delivered vs total orders

### 2. Seller Performance
- Revenue distribution (Pareto)
- Seller contribution
- Delivery vs reviews

### 3. Customer Performance
- One-time vs returning customers
- Revenue concentration
- Customer behavior

### 4. Customer Experience Drivers
- Delivery delays vs reviews
- On-time vs late deliveries
- Outliers

### 5. Payments & Financial Validation
- Payment vs order reconciliation
- Detection of anomalies
- Payment behavior

---

## 🧩 Data Model

### Fact Tables
- `Fact_Order_Items`
- `Fact_Payment`
- `Fact_Order_Review`

### Dimension Tables
- `Dim_Orders`
- `Dim_Customer`
- `Dim_Sellers`
- `Dim_Products`
- `Dim_Date`

### Aggregated Tables
- `Agg_Customer`
- `Agg_Seller`

---

## ⚙️ Key Modeling Decisions

- Separation of core data and analytical layers
- Aggregated tables for performance
- Delivered vs All Orders logic
- Static ranking for Pareto
- Advanced DAX for validation

---

## ⚠️ Data Challenges

**Inconsistent Order Status**  
Some canceled orders contain payments and delivery data. Order status alone is not a reliable indicator of delivery.  
→ Used delivered date as true completion indicator. Canceled orders defined as those marked canceled AND not delivered.

**Payments Without Orders**  
775 orders have associated payments but no corresponding order items, representing $162.6K in unlinked revenue.  
→ Extreme payment discrepancies are driven by orders lacking item records, not true financial anomalies.

**Canceled Orders with Payments**  
Out of 619 canceled orders with payment, 455 have valid order values.  
→ Financial validation performed only on completed orders; canceled transactions with payments analyzed separately as edge cases.

**Multiple Payments per Order**  
→ Aggregated at order level before reconciliation.

**Delivered Orders Without Delivery Date**  
Some orders with status "delivered" have no delivery timestamp.  
→ Handled via validation logic in DAX.

---

## 📈 Key Insights

**Performance**  
- ~97% orders delivered  
- Revenue growing steadily

**Sellers**  
- ~12–16% of sellers generate ~80% of revenue (Pareto effect)  
- Seller performance evaluated based on completed (delivered) orders for consistency

**Customers**  
- ~94% one-time buyers  
- ~3% repeat rate  
- Customer metrics based on active customers to avoid distortion from inactive accounts

**Experience**  
- Delays reduce review scores. Drivers analysis restricted to delivered orders for valid comparisons.  
- Moderate correlation between delivery time and review score: average review drops from 4.2 (0–4 days) to 3.0 (30+ days)

**Financial**  
- Most transactions show minimal difference between payment and order value  
- Payment discrepancies vary by method; voucher transactions show highest variability  
- Higher-value orders tend to be associated with higher installment counts

---

## 🛠 Tools & Technologies

- Power BI
- DAX (`CALCULATE`, `FILTER`, `TREATAS`, `EXCEPT`, `RANKX`)
- Star schema modeling
- Data validation techniques

---

## 📊 Dashboard Previews

| Overview | Seller Performance |
|----------|--------------------|
| ![Overview](https://github.com/amy165/Brazilian-E-Commerce-Public-Dataset-by-Olist/blob/main/images/Overview.jpg) | ![Seller](https://github.com/amy165/Brazilian-E-Commerce-Public-Dataset-by-Olist/blob/main/images/Seller.jpg) |

| Customer | Experience | Financial |
|----------|------------|----------|
| ![Customer](https://github.com/amy165/Brazilian-E-Commerce-Public-Dataset-by-Olist/blob/main/images/Customer.jpg) | ![Experience](https://github.com/amy165/Brazilian-E-Commerce-Public-Dataset-by-Olist/blob/main/images/Experience.jpg) | ![Financial](https://github.com/amy165/Brazilian-E-Commerce-Public-Dataset-by-Olist/blob/main/images/Financial.jpg) |

---

## 📥 Interactive Report

Due to file size limitations, the Power BI file is hosted externally.

👉 [Download the full .pbix file](https://drive.google.com/file/d/1TgmR5HlYsVgVYD5WUuVzNmza6x8wfeqe/view?usp=drive_link)

---

## 📌 Notes

- The dataset was cleaned and modeled for analytical purposes
- Several data inconsistencies were identified and handled during the analysis
- All business logic decisions are documented within this project
- **AI assistance:** I used AI tools to help refine complex DAX expressions and structure documentation. All analytical decisions, validation logic, and business interpretations are my own.

---

*This project simulates a real-world BI workflow, from data modeling and validation to delivering actionable insights.*
