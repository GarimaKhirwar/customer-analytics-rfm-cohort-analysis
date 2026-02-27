# 📊 Customer Analytics: RFM Segmentation & Cohort Retention Analysis

## 🚀 Project Overview

This project analyzes customer purchasing behavior using the Brazilian Olist e-commerce dataset. The goal is to identify high-value customers, understand retention patterns, and generate actionable business insights using RFM segmentation and cohort analysis.

This project simulates how data analysts and growth teams evaluate customer health and revenue drivers in real-world e-commerce businesses.

---

## 🎯 Business Problem

E-commerce companies often struggle to answer:

* Which customers generate the most revenue?
* How many customers actually return after their first purchase?
* Where is customer retention leaking?
* Which user segments should marketing focus on?

This project answers these questions using customer behavioral analytics.

---

## 🗂 Dataset

**Source:** Olist Brazilian E-Commerce Public Dataset

**Key tables used:**

* Customers
* Orders
* Payments

After cleaning and merging, the final dataset contains transaction-level customer purchase history.

---

## ⚙️ Methodology

### 1️⃣ Data Cleaning & Preparation

* Converted timestamp columns to datetime
* Filtered only delivered orders
* Handled missing values in critical fields
* Merged customers, orders, and payments tables

---

### 2️⃣ RFM Feature Engineering

For each customer:

* **Recency** → Days since last purchase
* **Frequency** → Number of unique orders
* **Monetary** → Total amount spent

Customers were scored using quantile-based binning and custom frequency handling due to heavy skew.

---

### 3️⃣ Customer Segmentation

Customers were grouped into business-friendly segments:

* 🏆 Champions
* 💎 Big Spenders
* 🤝 Loyal Customers
* ⚠️ At Risk
* 💤 Hibernating
* 🆕 New Customers

Segmentation was based on combined RFM scores.

---

### 4️⃣ Cohort Retention Analysis

* Created monthly cohorts based on first purchase month
* Calculated cohort index (months since first purchase)
* Built retention matrix
* Visualized retention using heatmap

This reveals how customer engagement decays over time.

---

## 📈 Key Insights

### 🔥 Customer Purchase Behavior

* The vast majority of customers are **one-time buyers**, indicating low natural repeat behavior.
* Average purchase frequency is very close to 1, showing strong acquisition but weak retention.

---

### 💰 Revenue Concentration

* **Big Spenders contribute the largest share of total revenue.**
* A significant portion of revenue also comes from **Hibernating users**, indicating potential win-back opportunities.

---

### 📉 Retention Pattern

* Cohort analysis shows a **sharp drop after the first month**, which is typical for many e-commerce platforms.
* Later-month retention stabilizes at a low level, suggesting limited long-term engagement.

---

### 🎯 Business Recommendations

* 🎁 Provide loyalty rewards to Champions
* 📧 Launch win-back campaigns for At Risk users
* 💎 Offer premium bundles to Big Spenders
* 📢 Improve onboarding and early experience to reduce first-month churn
* 🔄 Invest in retention marketing rather than only acquisition

---

## 🛠 Tech Stack

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook

---

## 📊 Project Structure

```
olist-rfm-cohort-analysis/
│
├── notebooks/
│   └── rfm_cohort_analysis.ipynb
├── images/
├── README.md
└── requirements.txt
```

---

## 🚀 Future Improvements

* Add customer lifetime value (CLV) modeling
* Build churn prediction model
* Create interactive dashboard (Power BI / Streamlit)
* Perform cohort revenue analysis
* Apply machine learning for customer clustering




