
***

# [Credit Risk Modelling Dataset](https://credit-risk-modelling-vat.streamlit.app/)

This repository contains a synthetic dataset for **credit risk analysis** and machine learning modeling, suitable for research, education, and prototyping production-ready credit scoring solutions. 

The data is structured into three relational CSV files:

- `customers.csv`
- `loans.csv`
- `bureau_data.csv`

***

## 📦 Dataset Files

### 1. `customers.csv`
Contains customer demographic and basic financial information.

*Example columns:*
- `customer_id`: Unique identifier for each customer
- `age`: Age of the customer
- `gender`: Gender (M/F)
- `income`: Annual income
- `employment_status`: Employment type (salaried, self-employed, etc.)
- `credit_score`: Credit score at account creation

### 2. `loans.csv`
Documents every loan issued to customers.

*Example columns:*
- `loan_id`: Unique identifier for the loan
- `customer_id`: Matches to the loan holder in `customers.csv`
- `disbursal_date`: When the loan was issued
- `loan_amount`: Principal issued
- `tenure_months`: Loan period
- `interest_rate`: Annual rate (%)
- `defaulted`: Default indicator (0/1)

### 3. `bureau_data.csv`
Aggregates credit bureau activity and past loans for each customer.

*Example columns:*
- `customer_id`: Foreign key to `customers.csv`
- `num_loans`: Number of reported loans (all bureaus)
- `avg_dpd`: Average days past due
- `current_balance`: Total bureau-recorded balance
- `credit_active`: Whether the bureau loan is open (yes/no)
- `delinquency_ratio`: Overdue accounts ratio

***

## 🔗 Data Relationships

- `customers.csv` links to `loans.csv` and `bureau_data.csv` via `customer_id`.
- A customer may have multiple loans and multiple bureau records.

***

## 🧠 Algorithms Used

This dataset is designed for benchmarking and developing various **credit risk modeling** solutions using both traditional statistics and modern machine learning algorithms. Commonly applied algorithms include:

- **Logistic Regression:** Fundamental for binary default risk, highly interpretable and a regulatory industry standard.
- **Decision Trees:** Simple rule-based splits, useful for initial modeling and segmenting customers into risk categories.
- **Random Forests:** Ensemble of trees to handle feature interactions and non-linear risk patterns, improve model stability.
- **Gradient Boosting Machines (e.g., XGBoost, LightGBM):** Advanced iterative ensembles that excel in predictive performance and industry competitions.
- **Clustering/Unsupervised Learning:** Segment customers for risk profiling or anomaly detection, e.g., k-means or DBSCAN.

Modern credit risk workflows emphasize robust **feature engineering** (ratios, historical behaviors), regularization, and hyperparameter optimization. Ensemble models and deep learners are frequently benchmarked against interpretable baselines like logistic regression, with explainability (e.g., SHAP, LIME) increasingly important for financial applications.[1][2][3][4][5][6][7][8]
**

## 💡 Usage

This dataset is ideal for:
- Credit scoring, customer risk rating, automated decisioning
- Default probability prediction and portfolio risk management
- Feature engineering, data preprocessing, and analytics demos
- Practical EDA, merging, and machine learning pipelines


***

## 🔗 Project & App

- Data Source: [Credit_Risk_Modelling](https://github.com/ABHI9234/Credit_Risk_Modelling)
- **Deployed App:** [credit-risk-modelling-vat.streamlit.app](https://credit-risk-modelling-vat.streamlit.app/)

