# 🛒 Customer Segmentation & Classification using Machine Learning

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10-blue?style=for-the-badge&logo=python">
  <img src="https://img.shields.io/badge/Scikit--Learn-ML-orange?style=for-the-badge&logo=scikit-learn">
  <img src="https://img.shields.io/badge/Status-Completed-success?style=for-the-badge">
  <img src="https://img.shields.io/badge/Project-Type%20ML-blueviolet?style=for-the-badge">
</p>

---

## Overview
This project builds a **complete end-to-end Machine Learning pipeline** to segment customers based on purchasing behavior using the **Online Retail dataset**.

It combines:
- 📊 Data Analysis  
- 🧠 Unsupervised Learning (K-Means)  
- 🏷️ Labeling  
- 🤖 Supervised Learning (KNN, SVM)  

> 🎯 Goal: Understand customer behavior and predict customer segments for better business decisions.

---

## 📊 Dataset
Transactional dataset containing online retail purchases.

### Features:
- `InvoiceNo` – Transaction ID  
- `StockCode` – Product ID  
- `Description` – Product name  
- `Quantity` – Items purchased  
- `InvoiceDate` – Transaction date  
- `UnitPrice` – Price per item  
- `CustomerID` – Customer identifier  
- `Country` – Customer location  

---

## ⚙️ Project Pipeline

### 1️⃣ Data Preprocessing
✔ Removed duplicates  
✔ Handled missing values  
✔ Converted data types  
✔ Removed negative quantities (returns)  

---

### 2️⃣ Exploratory Data Analysis
- Distribution of quantity & price  
- Top countries & products  
- Sales trends over time  

---

### 3️⃣ Feature Engineering (RFM)

| Metric | Description |
|------|------|
| Recency | Days since last purchase |
| Frequency | Number of transactions |
| Monetary | Total spending |

---

### 4️⃣ Feature Transformation
- Log Transformation (reduce skewness)  
- Standard Scaling (normalize features)  

---

### 5️⃣ Clustering (K-Means)
- Used **Elbow Method**  
- Optimal clusters: **K = 4**

---

## Clustering Results

| Cluster | Recency | Frequency | Monetary |
|--------|--------|--------|--------|
| 0 | 19.13 | 2.07 | 529.47 |
| 1 | 71.13 | 4.05 | 1772.05 |
| 2 | 12.11 | 13.56 | 7942.68 |
| 3 | 185.66 | 1.32 | 337.41 |

---

## Customer Segments

### 🟢 Cluster 2 – VIP Customers
- Very recent purchases  
- Very frequent buyers  
- Highest spending  
 **Most valuable customers**

---

### 🔵 Cluster 1 – Loyal Customers
- Regular purchases  
- High spending  
 **Stable revenue source**

---

### 🟡 Cluster 0 – Occasional Customers
- Recent but infrequent purchases  
 **Growth opportunity**

---

### 🔴 Cluster 3 – Inactive Customers
- Long time since last purchase  
 **Churn risk**

---

## Machine Learning Models

### 🔹 K-Nearest Neighbors (KNN)
- Distance-based classification  
- Tuned using GridSearchCV  

### 🔹 Support Vector Machine (SVM)
- Decision boundary optimization  
- Tuned using GridSearchCV  

---

## Model Optimization
✔ GridSearchCV  
✔ Cross-Validation  

**Tuned Parameters:**
- KNN → `n_neighbors`, `weights`  
- SVM → `C`, `kernel`, `gamma`  

---

## 📈 Results
- KNN Accuracy: **0.98**
- SVM Accuracy: **0.99**

---

## Business Insights

- 💰 VIP customers generate the majority of revenue  
- 🔁 Loyal customers ensure consistent income  
- 📈 Occasional customers can be converted  
- ⚠️ Inactive customers require re-engagement  

---

## Tech Stack

- Python 🐍  
- Pandas, NumPy  
- Scikit-learn  
- Matplotlib, Seaborn  
- Jupyter Notebook  

---

## 🚀 Run Locally

```bash
# Clone repository
git clone https://github.com/passantelsherif/unsupervised-to-supervised-customer-segmentation.git

# Navigate to project
cd unsupervised-to-supervised-customer-segmentation

# Create environment
python -m venv venv

# Activate
venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run notebook
jupyter notebook
