# 📊 E-commerce Analytics – End-to-End Power BI Project

## Project Overview

An end-to-end Business Intelligence project analyzing an e-commerce dataset using Power BI.

The objective was to simulate a real-world BI scenario, focusing on:

- Data consistency and validation
- Customer and seller behavior
- Delivery performance
- Financial integrity

This project goes beyond dashboards — it emphasizes analytical thinking and data reliability.

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

## 📁 Repository Structure

/pbix
  ecommerce_analysis.pbix

/images
  overview.png
  seller.png
  customer.png
  experience.png
  financial.png

README.md


---

*This project simulates a real-world BI workflow, from data modeling and validation to delivering actionable insights.*
