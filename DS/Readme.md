# 📊 Customer Segmentation in E-Commerce using KMeans and Autoencoders

## Overview

This analysis builds on a Brazilian e-commerce dataset and extends the initial BI exploration into a data science approach.

It focuses on understanding customer behavior through clustering techniques.

---

## 🧠 Objective

Segment customers based on behavior, experience, and transaction patterns.

---

## 🔍 Approach

### 1. KMeans (Baseline)

Baseline clustering using engineered customer features.

- Feature engineering
- Standard scaling
- Clustering using KMeans
- PCA visualization

![KMeans](https://raw.githubusercontent.com/amy165/images/main/Brazilian-E-Commerce/CustomerSegmentationKMeans.png)

### 2. Autoencoder + KMeans

Improved approach using neural networks to capture non-linear relationships in the data.

- Higher-dimensional feature set
- Dimensionality reduction using neural networks
- Clustering on latent space
- PCA visualization

![Autoencoder](https://raw.githubusercontent.com/amy165/images/main/Brazilian-E-Commerce/CustomerSegmentationAutoencoderKMeans.png)

## Comparison

The autoencoder-based approach improved cluster separation and revealed more meaningful behavioral patterns.

It allowed better differentiation between types of customer issues (logistics, payments, satisfaction).


---

## 📈 Key Insights

The segmentation revealed that customer behavior is driven not only by value but also by operational and experience-related factors.

- Customers are not only segmented by value but also by experience
- Distinct clusters identified:
  - Delivery issues
  - Payment problems
  - High-value dissatisfied customers
  - Healthy customers

---

## 👥 Customer Segments

The improved clustering approach identified five distinct customer profiles, showing that behavior is driven not only by spending, but also by experience and operational issues:

- **Cluster 0 – Logistics-critical customers**  
  High delivery delays and very high negative reviews. These customers consistently experience poor delivery performance.

- **Cluster 1 – Healthy customers**  
  Low delays, low negative reviews, and stable behavior. This is the baseline segment with a good overall experience.

- **Cluster 2 – Customers frequently affected by delivery delays**  
  High probability of delays and moderate dissatisfaction. Delivery issues are present but less extreme than the critical group.

- **Cluster 3 – High-value but dissatisfied customers**  
  High spending customers with low delays but high negative reviews, suggesting issues with product quality or unmet expectations.

- **Cluster 4 – Customers with high payment friction**  
  Customers with a high rate of payment-related issues, but otherwise normal experience in terms of delivery and reviews.

---

## 🛠 Tools & Tech

- Python
- Pandas & NumPy
- Scikit-learn (KMeans, PCA)
- TensorFlow / Keras (Autoencoder)
- Matplotlib & Seaborn
- Google Colab

---

## 📁 Files

- E-Commerce-Customer-Segmentation-KMeans.ipynb → baseline clustering
- E-Commerce-Customer-Segmentation-Autoencoder-KMeans.ipynb → improved approach
