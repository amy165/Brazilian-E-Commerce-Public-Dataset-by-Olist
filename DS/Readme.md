# 📊 Customer Segmentation using KMeans and Autoencoders

## Overview

This analysis builds on the e-commerce dataset and focuses on understanding customer behavior through clustering techniques.

---

## 🧠 Business Questions I Wanted to Answer

Goal: Segment customers based on behavior, experience, and transaction patterns.

---

## 🚀 What I Did

### 1. KMeans (Baseline)

- Feature engineering
- Standard scaling
- Clustering using KMeans
- PCA visualization

![KMeans](https://raw.githubusercontent.com/amy165/images/main/Brazilian-E-Commerce/CustomerSegmentationKMeans.png)

### 2. Autoencoder + KMeans

- Higher-dimensional feature set
- Dimensionality reduction using neural networks
- Clustering on latent space
- PCA visualization

![Autoencoder](https://raw.githubusercontent.com/amy165/images/main/Brazilian-E-Commerce/CustomerSegmentationAutoencoderKMeans.png)

## Comparison

The autoencoder-based approach improved cluster separation and allowed for better identification of customer behavior patterns.


---

## 📈 Key Insights

- Customers are not only segmented by value but also by experience
- Distinct clusters identified:
  - Delivery issues
  - Payment problems
  - High-value dissatisfied customers
  - Healthy customers

---

## 🛠 Tools & Tech

- Python
- Pandas & NumPy
- Scikit-learn (KMeans, PCA)
- TensorFlow / Keras (Autoencoder)
- Matplotlib & Seaborn
- Google Colab

---
## Files
- E-Commerce-Customer-Segmentation-KMeans.ipynb
- E-Commerce-Customer-Segmentation-Autoencoder-KMeans.ipynb
