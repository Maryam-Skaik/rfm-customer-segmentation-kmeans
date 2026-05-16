# 🧠 Customer Segmentation using RFM Analysis & K-Means Clustering

![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-KMeans-orange.svg)
![Clustering](https://img.shields.io/badge/Unsupervised-Clustering-purple.svg)
![Scikit-Learn](https://img.shields.io/badge/Library-Scikit--Learn-f7931e.svg)
![Status](https://img.shields.io/badge/Project-Completed-success.svg)

---

# 📌 Project Overview

Customer behavior analysis is one of the most important applications of Machine Learning in business intelligence and marketing analytics.

In this project, I applied **Unsupervised Machine Learning using K-Means Clustering** on **RFM customer data** to segment customers into meaningful groups based on their purchasing behavior.

The project transforms raw customer transaction metrics into actionable business insights that can help companies:

* improve customer retention
* personalize marketing strategies
* identify high-value customers
* reduce customer churn
* allocate marketing resources more efficiently

---

# 📊 Understanding RFM Analysis

RFM is a customer segmentation technique commonly used in marketing analytics.

It evaluates customers using three important behavioral metrics:

* ⏱️ **Recency (R)**
  Measures how recently a customer made a purchase

* 🔁 **Frequency (F)**
  Measures how often a customer purchases

* 💰 **Monetary Value (M)**
  Measures how much money the customer spends

Together, these metrics provide a strong understanding of customer engagement, loyalty, and business value.

---

# 🎯 Project Objectives

The main goals of this project were to:

* Apply **K-Means Clustering** to segment customers automatically
* Identify the optimal number of clusters
* Analyze customer behavior patterns
* Discover high-value and at-risk customers
* Build business-oriented marketing strategies based on customer segments

---

# 🧰 Technologies & Libraries

* Python 🐍
* Pandas 📊
* Scikit-Learn 🤖
* Matplotlib 📉
* StandardScaler ⚖️
* K-Means Clustering 🧠

---

# 📂 Dataset Information

### Dataset Features

The dataset contains customer-level RFM metrics:

* `CustomerID`
* `Recency`
* `Frequency`
* `MonetaryValue`

### Dataset Summary

* 👥 Total Customers: **4338**
* ✅ No missing values
* ✅ No duplicate records
* ✅ Clean and structured dataset ready for clustering

---

# ⚙️ Project Workflow

## 1️⃣ Data Exploration & Preprocessing

The first step was understanding and cleaning the dataset.

### Steps performed:

* Loaded the dataset using Pandas
* Explored dataset structure and feature types
* Checked for:

  * missing values
  * duplicate rows
  * incorrect data types
* Removed `CustomerID` because it is only an identifier and does not contribute to clustering

---

## 2️⃣ Feature Scaling

Since K-Means clustering relies heavily on distance calculations, feature scaling is extremely important.

Without scaling:

* features with larger numerical ranges could dominate clustering results
* MonetaryValue could overpower Recency and Frequency

To solve this:

* Applied `StandardScaler`
* Standardized all RFM features

This ensured equal contribution from all variables during clustering.

---

## 3️⃣ Finding the Optimal Number of Clusters

K-Means requires selecting the number of clusters (`K`) before training.

To determine the best value of K, I tested multiple cluster values from **2 to 10** using two evaluation techniques:

### 📉 Elbow Method (Inertia)

Measures cluster compactness.

* Lower inertia means tighter clusters
* The optimal point is where improvement begins slowing down

### 📈 Silhouette Score

Measures cluster separation quality.

* Higher silhouette score indicates better-defined clusters
* Helps evaluate how distinct the customer groups are

By analyzing both metrics together, the optimal number of clusters was identified as:

### ✅ K = 4

---

## 4️⃣ Training the Final Model

Final model configuration:

* Algorithm: **K-Means Clustering**
* Number of Clusters: **4**
* Random State: `42`
* Initialization: `n_init='auto'`

The model successfully assigned each customer to a specific cluster based on behavioral similarity.

---

# 📊 Cluster Profiling & Analysis

After training the model, customer groups were analyzed using average RFM values and customer counts.

## 📌 Cluster Statistics

| Cluster | Recency | Frequency | MonetaryValue | Customer Count |
| ------- | ------- | --------- | ------------- | -------------- |
| 0       | 43.7    | 3.7       | 1359.0        | 3054           |
| 1       | 248.1   | 1.6       | 480.6         | 1067           |
| 2       | 7.4     | 82.5      | 127338.3      | 13             |
| 3       | 15.5    | 22.3      | 12709.1       | 204            |

---

# 🔍 Customer Segment Interpretation

## 🛒 Cluster 0 — Low-Value Customers

* Largest customer segment with **3054 customers**
* Low purchase frequency and relatively low spending
* Individually low-value customers, but collectively important due to segment size

### Business Insight

Even small improvements in this segment could generate significant overall revenue because of the large customer count.

---

## ⛔ Cluster 1 — Inactive / At-Risk Customers

* Customers with extremely high recency values
* Have not purchased for a long period
* Very low engagement and spending behavior

### Business Insight

This segment has a high risk of customer churn and requires re-engagement strategies.

---

## 💎 Cluster 2 — VIP Customers

* Smallest segment with only **13 customers**
* Extremely high frequency and spending behavior
* Generates disproportionately high revenue

### Business Insight

Although this cluster is very small, it represents the most valuable customers in the business. Retaining them is critical for profitability.

---

## 🚀 Cluster 3 — Potential Loyal Customers

* Recently active customers
* Strong spending behavior and good purchase frequency
* High growth potential

### Business Insight

These customers could become future VIP customers with proper engagement and personalized marketing.

---

# 📈 Key Insights

* 💰 Frequency and MonetaryValue were the strongest drivers of customer segmentation
* 📊 Clustering clearly separated:

  * high-value customers
  * inactive customers
  * growth-potential customers
* 🎯 Customer value is not equally distributed across the dataset
* 💎 A very small percentage of customers contributes a disproportionately large amount of revenue
* 🧠 RFM-based clustering provides highly interpretable business insights

---

# 📣 Marketing Strategy Recommendations

## 🛒 Cluster 0 — Low-Value Customers

### Strategy

* Bundle offers
* Seasonal promotions
* Personalized recommendations
* Low-cost retention campaigns

### Goal

Increase purchase frequency and improve customer engagement at scale.

---

## ⛔ Cluster 1 — Inactive Customers

### Strategy

* Win-back campaigns
* Reminder emails
* Re-engagement messages
* Return discounts

### Goal

Reduce customer churn and recover inactive users.

---

## 💎 Cluster 2 — VIP Customers

### Strategy

* Loyalty programs
* Exclusive offers
* Personalized rewards
* Premium support
* Early product access

### Goal

Maximize customer retention and increase customer lifetime value.

---

## 🚀 Cluster 3 — Potential Loyal Customers

### Strategy

* Upselling
* Cross-selling
* Personalized engagement campaigns
* Product recommendations

### Goal

Convert these customers into future VIP segments.

---

# 🧠 Final Conclusion

This project demonstrates how **Machine Learning and RFM analysis** can transform raw customer transaction data into actionable business intelligence.

Using K-Means clustering, customers were successfully segmented into meaningful behavioral groups, allowing businesses to:

* Improve customer retention
* Identify high-value customers
* Detect churn-risk segments
* Personalize marketing campaigns
* Optimize marketing resources
* Increase long-term revenue efficiency

The project highlights the power of **unsupervised learning** in solving real-world business problems and supporting data-driven decision-making.
