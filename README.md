# Exploratory Data Analysis – Online Payment Fraud Detection

This project performs **Exploratory Data Analysis (EDA)** on an online payment transaction dataset to understand fraud patterns and identify factors that contribute to fraudulent activities.

The analysis focuses on discovering transaction behaviors, detecting unusual patterns, and identifying high-risk transaction types that may indicate fraud.

The insights from this analysis can help improve fraud detection systems and enhance the security of digital payment platforms.

---

# Project Overview

With the rapid growth of online payment systems, the number of digital transactions has increased significantly. This growth has also led to a rise in fraudulent transactions.

Detecting fraud manually is difficult due to the large volume of transactions and complex fraud patterns.

This project analyzes transaction data to answer questions such as:

* Which transaction types are more likely to be fraudulent?
* Do high transaction amounts indicate higher fraud risk?
* How do account balance changes relate to fraud?
* What transaction patterns indicate suspicious activity?

The project uses **data cleaning, visualization, and statistical analysis** to identify important fraud-related patterns.

---

# Project Objectives

* Understand patterns in fraudulent and non-fraudulent transactions
* Identify high-risk transaction types
* Analyze relationships between transaction amount and account balances
* Detect unusual balance changes that may indicate fraud
* Generate insights to support fraud detection systems

---

# Dataset Information

**Dataset Name:** Online Payment Fraud Detection Dataset
**Dataset Type:** Financial Transaction Dataset
**Rows:** Large dataset containing millions of transactions
**Columns:** 11
**Data Types:** Numerical and Categorical

### Important Features

| Column         | Description                                    |
| -------------- | ---------------------------------------------- |
| step           | Time step representing transaction time (hour) |
| type           | Type of transaction (TRANSFER, CASH-OUT, etc.) |
| amount         | Transaction amount                             |
| oldbalanceOrg  | Sender balance before transaction              |
| newbalanceOrig | Sender balance after transaction               |
| oldbalanceDest | Receiver balance before transaction            |
| newbalanceDest | Receiver balance after transaction             |
| isFraud        | Fraud indicator (1 = Fraud, 0 = Normal)        |
| isFlaggedFraud | System flagged fraud indicator                 |

The **target variable is `isFraud`**, which indicates whether the transaction is fraudulent.

---

# Technologies Used

* Python
* Pandas – Data manipulation
* NumPy – Numerical operations
* Matplotlib – Data visualization
* Seaborn – Statistical visualization
* Jupyter Notebook

---

# Data Cleaning & Preparation

The following preprocessing steps were performed:

* Checked dataset structure and dimensions
* Verified data types of each column
* Checked for missing values
* Checked for duplicate records

### Key Observations

* No duplicate rows were detected
* No missing values were found
* Fraud cases are extremely rare compared to normal transactions
* The dataset shows **class imbalance**

---

# Exploratory Data Analysis

## Univariate Analysis

Univariate analysis was performed to understand the distribution of individual variables.

### Visualizations Used

* Histograms
* Box Plots
* Count Plots

### Key Observations

* Most transactions involve smaller amounts
* Transaction amounts show **right-skewed distribution**
* Several large-value outliers are present
* Fraud transactions are very rare compared to normal transactions

---

## Bivariate Analysis

Bivariate analysis explores relationships between two variables.

### Visualizations Used

* Scatter Plots
* Bar Charts
* Box Plots

### Key Insights

* Fraud occurs more frequently in **TRANSFER** and **CASH-OUT** transactions
* Higher transaction amounts show increased fraud risk
* Many transactions reduce the sender balance close to zero
* Some balance mismatches may indicate suspicious activity

---

## Multivariate Analysis

Multivariate analysis examines relationships between multiple variables simultaneously.

### Visualizations Used

* Correlation Heatmap
* Pair Plot

### Findings

* Transaction amount and destination balance show **moderate correlation**
* Fraud has weak correlation with most variables
* Balance-related variables show relationships with transaction amount
* Overall multicollinearity between features is low

---

# Key Insights

* Fraudulent transactions represent a very small percentage of total transactions
* Fraud is more common in **TRANSFER** and **CASH-OUT** transaction types
* High transaction amounts are more likely to be associated with fraud
* Balance inconsistencies may indicate suspicious behavior
* Most features show weak correlation with fraud, indicating complex fraud patterns

---

# Business Recommendations

* Monitor **high-value transactions** more carefully
* Apply stricter checks for **TRANSFER and CASH-OUT transactions**
* Implement automated fraud detection systems using machine learning
* Track unusual balance changes to detect suspicious activity early

---

# Conclusion

Exploratory Data Analysis helped uncover important patterns in online payment transactions and fraud behavior.

The insights generated from this project can help financial institutions:

* Improve fraud detection mechanisms
* Identify high-risk transactions
* Strengthen digital payment security

The dataset can also be used for **future machine learning models to predict fraudulent transactions automatically.**

---
# Author

**R. Pujitha**
