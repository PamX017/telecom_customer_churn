# Activity 1: Dataset Preparation Activity (Telco Customer Churn)

**Course:** Machine Learning [ADPC509]  
**Class:** T.Y. B.Tech (AI & DS)  
**Academic Year:** 2026-27  
**Department:** Artificial Intelligence & Data Science  
**Institution:** Zeal College of Engineering and Research (ZCOER), Pune  

---

## 📌 Project Overview
This repository contains the complete dataset preparation and exploratory data analysis (EDA) workflow performed as part of **Activity 1: Dataset Preparation Activity**. 

The goal of this project is to inspect a tabular dataset, identify data-quality issues, handle missing entries, perform basic exploratory data analysis, encode categorical features, and scale numerical variables to prepare a clean, ML-ready dataset without building predictive models yet.

---

## 📊 Dataset Details
* **Dataset Name:** Telco Customer Churn Dataset
* **Source:** [Kaggle - Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn) / IBM Open Source
* **Domain:** Business & Telecommunications
* **Format:** Tabular CSV
* **Original Dimensions:** 7,043 Rows × 21 Columns
* **Primary Target Feature:** `Churn` (Yes/No)

---

## 🛠️ Tools & Libraries Used
* **Programming Language:** Python 3.x
* **Environment:** Google Colab / Jupyter Notebook
* **Data Manipulation:** `pandas`, `numpy`
* **Data Visualization:** `matplotlib`, `seaborn`
* **Preprocessing:** `scikit-learn` (`StandardScaler`, `OneHotEncoder`)

---

## 🚀 Step-by-Step Implementation Summary

| Step | Task | Description / Decisions Made |
| :--- | :--- | :--- |
| **Step 1** | **Dataset Selection** | Selected the Telco Customer Churn dataset containing numerical and categorical columns with implicit missing data. |
| **Step 2** | **Load & Inspect** | Loaded the raw dataset and recorded data types, total rows, non-null counts, and head/tail samples. |
| **Step 3** | **Data Types & Stats** | Categorized features into numerical (`tenure`, `MonthlyCharges`) and categorical (`Contract`, `PaymentMethod`). Identified non-predictive column (`customerID`). |
| **Step 4** | **Identify Missing Data** | Converted hidden blank spaces `' '` in `TotalCharges` into `NaN`. Found 11 missing values (0.15% of dataset). |
| **Step 5** | **Handle Missing Values** | Imputed missing `TotalCharges` values using the column **median** due to skewness, preserving all rows. |
| **Step 6** | **Consistency & Duplicates** | Dropped non-predictive `customerID`, checked for duplicate rows, and trimmed whitespaces from string labels. |
| **Step 7** | **Exploratory Data Analysis** | Generated a **Histogram** (`MonthlyCharges`) and **Bar Chart** (`Contract`). Observed high month-to-month subscription density. |
| **Step 8** | **Categorical Encoding** | Applied **Binary Mapping** (0/1) for binary columns (`gender`, `Churn`) and **One-Hot Encoding** for nominal multi-class columns (`Contract`, `PaymentMethod`). |
| **Step 9** | **Feature Scaling** | Applied `StandardScaler` to continuous features (`tenure`, `MonthlyCharges`, `TotalCharges`) to standardize feature ranges. |
| **Step 10** | **Save & Export** | Verified zero missing values/duplicates remained and exported the prepared dataset to `prepared_telco_churn.csv`. |

---

## 📁 Repository Structure
```text
├── README.md                   # Project documentation and summary report
├── dataset_preparation.ipynb   # Main Jupyter/Colab notebook with code and outputs
├── Telco-Customer-Churn.csv    # Original raw dataset
└── prepared_telco_churn.csv    # Final cleaned, encoded, and scaled CSV dataset
```

---

## 📈 Key Visualizations & Findings
1. **Monthly Charges Distribution:** Shows a multi-modal distribution with a distinct high frequency near \$20/month.
2. **Contract Type Breakdown:** A major portion of customers opt for short-term *Month-to-month* contracts compared to one-year or two-year commitments.

---

## 🏁 Conclusion
The dataset preparation workflow successfully converted raw, uncleaned telecom records into a high-quality tabular format ready for downstream machine learning workflows. All missing values, unneeded identifier columns, scale variances, and categorical representations were resolved systematically while keeping the raw data intact.

---
**Author:** Student - Department of AI & DS, ZCOER Pune