# 🧠 Customer Segmentation using RFM & K-Means Clustering

![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-KMeans-orange.svg)
![Clustering](https://img.shields.io/badge/Unsupervised-Clustering-purple.svg)
![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-f7931e.svg)
![Status](https://img.shields.io/badge/Project-Completed-success.svg)

---

## 📌 Project Overview

Understanding customer behavior is essential for building effective marketing strategies and improving business profitability.

This project applies **Unsupervised Machine Learning (K-Means Clustering)** on **RFM (Recency, Frequency, Monetary)** customer data to automatically segment customers into meaningful groups.

The goal is to transform raw transactional data into actionable business insights.

---

## 📊 What is RFM?

RFM is a behavioral segmentation technique used in marketing analytics:

- ⏱️ **Recency (R):** How recently a customer made a purchase  
- 🔁 **Frequency (F):** How often a customer makes purchases  
- 💰 **Monetary (M):** How much money a customer spends  

These three metrics help identify valuable vs inactive customers and guide targeted marketing strategies.

---

## 🎯 Project Goal

- Apply **K-Means Clustering** to segment customers
- Determine optimal number of clusters using:
  - 📉 Elbow Method (Inertia)
  - 📈 Silhouette Score
- Analyze cluster behavior
- Convert results into **business-driven marketing strategies**

---

## 🧰 Technologies Used

- Python 🐍  
- Pandas 📊  
- Scikit-Learn 🤖  
- Matplotlib 📉  
- StandardScaler (Feature Scaling) ⚖️  

---

## 📂 Dataset

- Source: RFM customer dataset
- Total Customers: **4338**
- Features:
  - Recency
  - Frequency
  - MonetaryValue

No missing values or duplicates were found.

---

## ⚙️ Workflow

### 1️⃣ Data Preprocessing
- Removed `CustomerID`
- Checked data quality (no missing values)
- Verified data types and structure

### 2️⃣ Feature Scaling
To ensure fair contribution between variables:

- Applied `StandardScaler`
- Standardized Recency, Frequency, MonetaryValue

---

### 3️⃣ Finding Optimal Clusters (K)

We evaluated different values of K using:

- 📉 Inertia (Elbow Method)
- 📈 Silhouette Score

This helped identify the best clustering structure.

---

### 4️⃣ Model Training

Final model:

- Algorithm: **K-Means**
- Optimal clusters: **K = 4**
- Random State: 42

Each customer was assigned a cluster label.

---

## 📊 Cluster Analysis

After training, we grouped customers by cluster and analyzed their behavior.

### 📌 Cluster Profiles

- 💎 **Cluster 2 — VIP Customers**
  - High frequency & high spending
  - Most valuable customers

- 🛒 **Cluster 0 — Low-Value Customers**
  - Low purchase activity
  - Minimal spending behavior

- ⛔ **Cluster 1 — Inactive Customers**
  - Long time since last purchase
  - Low engagement

- 🚀 **Cluster 3 — Potential Loyal Customers**
  - Recently active
  - Moderate spending with growth potential

---

## 📈 Key Insights

- 💰 Frequency and MonetaryValue were the strongest segmentation drivers
- 📊 Clustering successfully separated high-value and inactive users
- 🎯 RFM-based clustering provides strong business interpretability

---

## 📣 Marketing Strategy Recommendations

### 💎 VIP Customers (Cluster 2)
- Loyalty programs
- Exclusive offers
- Early access to products
- Personalized rewards

---

### 🛒 Low-Value Customers (Cluster 0)
- Discounts and bundles
- Seasonal promotions
- Cost-efficient retention campaigns

---

### ⛔ Inactive Customers (Cluster 1)
- Win-back campaigns
- Re-engagement emails/messages
- Special comeback discounts

---

### 🚀 Potential Loyal Customers (Cluster 3)
- Upselling strategies
- Cross-selling recommendations
- Engagement-driven promotions

---

## 🧠 Final Conclusion

This project demonstrates how **Unsupervised Machine Learning + RFM analysis** can transform raw customer data into actionable business intelligence.

By clustering customers, businesses can:
- Improve retention strategies
- Increase customer lifetime value
- Optimize marketing costs
- Personalize customer engagement
