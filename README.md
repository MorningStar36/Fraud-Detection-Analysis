# E-commerce Fraud Detection: Exploratory Data Analysis

This project is an exploratory data analysis (EDA) of over 299,000 e-commerce transactions to identify key patterns and indicators of fraudulent activity. The primary goal was to understand *how* fraudulent behavior differs from legitimate transactions and to visualize these findings.

## 📊 View the Interactive Dashboard

**[>> View the Live Dashboard on Tableau Public](https://your-tableau-public-link-here)**
*(This is the main deliverable of this project. Be sure to create this link and update it here.)*

---

### Tech Stack
* **Data Analysis:** Python, Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn, Tableau

### Project Overview

The dataset contains 299,695 transactions with 17 features, including user account age, transaction amount, AVS match status, and merchant category. The data is highly imbalanced, with a baseline fraud rate of only 2.2%.

The goal of this EDA was to look past the overall numbers and pinpoint the specific features that strongly correlate with fraud, in order to provide actionable insights for risk management.

### Key Insights & Findings

This analysis uncovered several critical, high-impact indicators:

1.  **New Accounts are Extremely High-Risk:** While the baseline fraud rate was 2.2%, accounts less than 5 days old had a fraud rate of 47.8%. This means new accounts are **21.6 times more likely** to be fraudulent.
2.  **Verification Failures are a Major Red Flag:** Transactions that failed the Address Verification System (AVS match = 0) had a fraud rate of 9.7%, making them **4.4 times more likely** to be fraudulent than the average transaction.
3.  **Country Mismatches:** Transactions where the user's `country` did not match the credit card's `bin_country` showed a significantly higher correlation with fraudulent activity.
4.  **Transaction Velocity:** Fraudulent users often had a higher `total_transactions_user` in a short period, indicating rapid, automated attempts.

These findings formed the basis for the interactive Tableau dashboard and provided the key features for the follow-up machine learning model.
