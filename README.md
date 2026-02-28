# 📊 Customer Analytics: RFM, Cohort & Churn Analysis

## 🚀 Project Overview

This project analyzes customer purchasing behavior using the Brazilian Olist e-commerce dataset. The objective is to identify high-value customers, understand retention dynamics, quantify churn risk, and generate actionable business insights using RFM segmentation, cohort retention analysis, and behavioral churn analysis.

This end-to-end analysis simulates how data analysts and growth teams evaluate customer health, retention leakage, and revenue risk in real-world e-commerce businesses.

---

## 🎯 Business Problem

E-commerce companies often struggle to answer:

- Which customers generate the most revenue?
- How many customers actually return after their first purchase?
- Where is customer retention leaking?
- Which user segments are most likely to churn?
- Which customers should retention efforts prioritize?

This project addresses these questions through structured customer analytics.

---

## 🗂 Dataset

**Source:** Olist Brazilian E-Commerce Public Dataset

**Key tables used:**

- Customers  
- Orders  
- Payments  

After cleaning and merging, the final dataset contains transaction-level customer purchase history.

---

## ⚙️ Methodology

### 1️⃣ Data Cleaning & Preparation

- Converted timestamp columns to datetime  
- Filtered only delivered orders  
- Handled missing values in critical fields  
- Merged customers, orders, and payments tables  
- Stored processed data in efficient Parquet format  

---

### 2️⃣ RFM Feature Engineering

For each customer:

- **Recency** → Days since last purchase  
- **Frequency** → Number of unique orders  
- **Monetary** → Total amount spent  

Customers were scored using quantile-based binning with custom handling for heavily skewed frequency distribution.

---

### 3️⃣ Customer Segmentation

Customers were grouped into business-friendly segments:

- 🏆 Champions  
- 💎 Big Spenders  
- 🤝 Loyal Customers  
- ⚠️ At Risk  
- 💤 Hibernating  
- 🆕 New Customers  

Segmentation was based on combined RFM scores.

---

### 4️⃣ Cohort Retention Analysis

- Created monthly cohorts based on first purchase month  
- Calculated cohort index (months since first purchase)  
- Built retention matrix  
- Visualized retention using heatmap  

This reveals how customer engagement decays over time.

---

### 5️⃣ Churn Analysis (NEW)

Churn was defined using an inactivity-based approach:

> Customer is considered churned if no purchase in the last **90 days**.

The analysis included:

- Overall churn rate estimation  
- Behavioral churn analysis (Recency, Frequency, Monetary)  
- Segment-level churn comparison  
- Frequency bucket churn analysis  
- Cohort-based churn view  
- High-value customer churn identification  

This step quantifies customer attrition risk and highlights revenue exposure.

---

## 📈 Key Insights

### 🔥 Customer Purchase Behavior

- The vast majority of customers are **one-time buyers**, indicating a structural repeat-purchase challenge.
- Average purchase frequency is very close to 1, showing strong acquisition but weak retention.

---

### 📉 Churn Risk

- Overall churn rate is **~80%**, typical of transactional marketplace models but indicative of limited customer stickiness.
- Customers with frequency = 1 show the highest churn risk.
- Even high-value segments (Big Spenders, Champions) exhibit meaningful churn levels.

---

### 💰 Revenue Concentration

- **Big Spenders contribute the largest share of total revenue.**
- A notable portion of high-value customers have churned, indicating revenue leakage risk.
- Hibernating users represent a major win-back opportunity.

---

### 📊 Retention Pattern

- Cohort analysis shows a **sharp drop after the first month**.
- Later-month retention stabilizes at a low level.
- The second purchase moment emerges as the most critical lifecycle milestone.

---

## 🎯 Business Recommendations

- 🎁 Provide loyalty rewards to Champions  
- 📧 Launch win-back campaigns for At Risk and Hibernating users  
- 💎 Offer premium bundles to Big Spenders  
- 🔁 Focus on converting first-time buyers into repeat customers  
- 📢 Improve onboarding and early customer experience  
- 🎯 Prioritize retention using value-weighted strategy  

---

## 🛠 Tech Stack

- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Jupyter Notebook  

---

## 📊 Project Structure
customer-analytics-rfm-cohort-analysis/
│
├── notebooks/
│ ├── 01_rfm_cohort_analysis.ipynb
│ └── 02_churn_analysis.ipynb
├── data/
├── visuals/
├── README.md
└── requirements.txt


---

## 🚀 Future Improvements

- Add Customer Lifetime Value (CLV) modeling  
- Build churn prediction model (ML)  
- Perform survival analysis (Kaplan–Meier)  
- Create interactive dashboard (Power BI / Streamlit)  
- Implement churn risk scoring system  




