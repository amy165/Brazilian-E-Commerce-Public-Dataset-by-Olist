# 📊 E-commerce Analytics – End-to-End Power BI Project

## Project Overview

An end-to-end Business Intelligence project analyzing an e-commerce dataset using Power BI.

The objective was to simulate a real-world BI scenario, focusing on:

- Data consistency and validation
- Customer and seller behavior
- Delivery performance
- Financial integrity

This project goes beyond dashboards — it emphasizes analytical thinking and data reliability.

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

## 📌 Notes

- The dataset was cleaned and modeled for analytical purposes
- Several data inconsistencies were identified and handled during the analysis
- All business logic decisions are documented within this project
## 🚀 Project Highlights

- 📊 Built **5 fully interactive dashboards** covering key business domains
- 🔍 Identified **$162K in payments without linked orders**
- ⚠️ Detected **data inconsistencies** in order status and payments
- 🧠 Applied **advanced DAX** for anomaly detection and validation
- 📈 Revealed strong **Pareto effects** in customers and sellers

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
Some canceled orders contain payments and delivery data  
→ Used delivered date as true completion indicator

**Payments Without Orders**  
775 affected orders  
~$162K unlinked revenue

**Canceled Orders with Payments**  
455 affected orders  
~$105K impacted

**Multiple Payments per Order**  
→ Aggregated at order level

---

## 📈 Key Insights

**Performance**  
- ~97% orders delivered  
- Revenue growing steadily

**Sellers**  
- ~15% generate ~80% of revenue

**Customers**  
- ~94% one-time buyers  
- ~3% repeat rate

**Experience**  
- Delays reduce review scores  
- Moderate correlation

**Financial**  
- Payments mostly consistent  
- Key anomalies detected

---

## 🛠 Tools & Technologies

- Power BI
- DAX (`CALCULATE`, `FILTER`, `TREATAS`, `EXCEPT`, `RANKX`)
- Star schema modeling
- Data validation techniques

---

## 📊 Interactive Report

Due to file size limitations, the Power BI file is hosted externally.

👉 [Download the full .pbix file](https://drive.google.com/file/d/1TgmR5HlYsVgVYD5WUuVzNmza6x8wfeqe/view?usp=drive_link)

## 📸 Dashboard Preview

![Overview](https://github.com/amy165/Brazilian-E-Commerce-Public-Dataset-by-Olist/blob/main/images/Overview.jpg)
![Seller](https://github.com/amy165/Brazilian-E-Commerce-Public-Dataset-by-Olist/blob/main/images/Seller.jpg)
![Customer](https://github.com/amy165/Brazilian-E-Commerce-Public-Dataset-by-Olist/blob/main/images/Customer.jpg)
![Experience](https://github.com/amy165/Brazilian-E-Commerce-Public-Dataset-by-Olist/blob/main/images/Experience.jpg)
![Financial](https://github.com/amy165/Brazilian-E-Commerce-Public-Dataset-by-Olist/blob/main/images/Financial.jpg)


---

*This project simulates a real-world BI workflow, from data modeling and validation to delivering actionable insights.*
