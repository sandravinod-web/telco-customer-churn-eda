# Telco Customer Churn Analysis – Exploratory Data Analysis (EDA)

## Project Overview

This project performs Exploratory Data Analysis (EDA) on the IBM Telco Customer Churn dataset to understand customer behaviour and identify factors associated with customer churn.

The objective is to explore customer demographics, subscribed services, contract types, payment methods and billing information to discover patterns that can help a telecommunications company improve customer retention.

## Summary of Key Findings

- **26.5%** of customers churned (1,869 out of 7,043).
- **Contract type:** Month-to-month customers have the highest churn rate (42.71%), compared with 11.27% for one-year contracts and 2.83% for two-year contracts.
- **Customer tenure:** Customers in their first 12 months have the highest churn rate (about 47.4%), compared with about 9.5% for customers with more than 48 months of tenure.
- **Internet service:** Fiber optic customers have a churn rate of 41.89%, compared with 18.96% for DSL customers.
- **Payment method:** Electronic check users have the highest churn rate (45.29%).
- **Technical support:** Customers without Tech Support have a higher churn rate than customers who subscribe to it.
- **Online security:** Customers without Online Security also show a higher churn rate.

## Project Objectives

- Understand the distribution of customers who stayed and churned.
- Analyse numerical and categorical features.
- Identify customer groups with higher churn rates.
- Explore relationships between tenure, monthly charges and churn.
- Identify factors associated with higher churn rates.
- Generate meaningful business insights.

## Dataset Information

**Dataset:** IBM Telco Customer Churn

**Source:** [Kaggle – Telco Customer Churn Dataset](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)

- Total records: 7,043 customers
- Total original columns: 21
- Target variable: `Churn`
- Dataset file: `WA_Fn-UseC_-Telco-Customer-Churn.csv`

The dataset contains customer demographics, subscribed services, contract details, payment methods and billing information.

## Technologies Used

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn

## Project Workflow

1. Importing required libraries
2. Loading the dataset
3. Understanding the dataset
4. Data quality assessment
5. Data cleaning and preprocessing
6. Univariate analysis
7. Outlier detection using the IQR method
8. Bivariate analysis
9. Multivariate analysis and correlation
10. Business insights and conclusion

## Data Cleaning Highlights

- Identified 11 blank values in `TotalCharges`. All 11 belong to customers with `tenure = 0`. These values were converted to missing values (`NaN`) and retained rather than replaced with zero.
- No duplicate rows or duplicate customer IDs were found.
- `SeniorCitizen` was represented as a categorical feature (No/Yes) for categorical analysis.
- "No internet service" and "No phone service" were retained as valid categories.
- A numeric `Churn_flag` column was created (Yes = 1, No = 0) for churn-rate calculations and correlation analysis.
- A numeric `SeniorCitizen_flag` column was used for correlation analysis.
- The IQR (1.5 × IQR) method was used to identify potential outliers in numerical features.

---

# Exploratory Data Analysis and Visualizations

## 1. Customer Churn Distribution

This chart shows the distribution of customers who stayed and customers who churned.

**Key Findings:**
- 73.5% of customers stayed.
- 26.5% of customers churned.

![Churn Distribution](images/churn_distribution.png)

## 2. Numerical Features Distribution

This section explores the distributions of tenure, MonthlyCharges and TotalCharges.

**Key Findings:**
- Tenure shows a concentration of both new and long-term customers.
- MonthlyCharges has multiple distribution patterns.
- TotalCharges is right-skewed, with many customers having relatively low total charges.

![Numerical Features Distribution](images/numerical_features_distribution.png)

## 3. Churn Rate by Customer Services

This comparison explores churn rates across contract types, internet services and payment methods.

**Key Findings:**
- Month-to-month contracts have the highest churn rate (42.71%).
- Fiber optic customers have a high churn rate (41.89%).
- Electronic check users have the highest churn rate (45.29%).

**Business Insight:** The company should focus on retaining month-to-month customers, reviewing fiber optic service satisfaction and improving the payment experience.

![Churn by Customer Services](images/churn_by_customer_services.png)

## 4. Numerical Features vs Customer Churn

This analysis compares tenure, monthly charges and total charges between customers who stayed and customers who churned.

**Key Findings:**
- Customers who churned generally have shorter tenure.
- Customers who churned have higher average monthly charges (approximately 74.44 compared with 61.27).
- Customers who stayed have higher average total charges.

![Numerical Features vs Churn](images/numerical_features_vs_churn.png)

## 5. Tenure Distribution by Churn

This chart compares the tenure distributions of customers who stayed and customers who churned.

**Key Finding:** Customers who churned are more concentrated in the lower tenure range, suggesting that early customer retention is important.

![Tenure Distribution by Churn](images/tenure_distribution_by_churn.png)

## 6. Churn Rate by Tenure Group

Customers are divided into four tenure groups to compare their churn rates.

**Key Finding:** Customers with shorter tenure have higher churn rates. The 0–12 month group shows the highest churn rate (about 47.4%), falling to about 9.5% for customers with more than 48 months of tenure.

![Churn Rate by Tenure Group](images/churn_by_tenure_group.png)

## 7. Tenure by Contract Type

This violin plot compares customer tenure across month-to-month, one-year and two-year contracts.

**Key Finding:** Customers with longer-term contracts generally show longer tenure.

![Tenure by Contract](images/tenure_by_contract.png)

## 8. Tenure vs Monthly Charges

This scatter plot explores the relationship between customer tenure and monthly charges, with customers differentiated by churn status.

**Key Finding:** Churned customers appear more concentrated among customers with shorter tenure and higher monthly charges.

![Tenure vs Monthly Charges](images/tenure_vs_monthly_charges.png)

## 9. Numerical Features Pairplot

The pairplot visualises relationships between tenure, monthly charges and total charges, with customers grouped by churn status.

**Key Findings:**
- TotalCharges increases strongly with tenure.
- Churned customers are more concentrated at lower tenure and lower total charges.

![Numerical Features Pairplot](images/numerical_features_pairplot.png)

## 10. Correlation Heatmap

The correlation heatmap displays relationships between numerical features.

**Key Findings:**
- Tenure and TotalCharges have a strong positive correlation (0.83).
- MonthlyCharges and TotalCharges have a positive correlation (0.65).
- Tenure and Churn_flag have a negative correlation (-0.35).

**Note:** Correlation shows association, not causation.

![Correlation Heatmap](images/correlation_heatmap.png)

---

## Key Business Insights

Based on the analysis:

- Focus on improving retention among month-to-month contract customers by offering benefits for moving to longer contracts.
- Give new customers extra attention during their first 12 months, when churn is highest.
- Investigate customer satisfaction and pricing for fiber optic services.
- Review the customer experience for electronic check users and encourage automatic payment methods.
- Promote Tech Support and Online Security bundles, and evaluate whether they help reduce churn.
- Monitor customers with higher monthly charges who may be at risk of leaving.

## Conclusion

The analysis highlights several patterns associated with customer churn, including contract type, tenure, internet service, payment method and billing patterns.

Customers with month-to-month contracts, shorter tenure, fiber optic services and electronic check payments show comparatively higher churn rates.

These findings can help the company develop targeted customer retention strategies and improve customer satisfaction.

## Limitations and Future Scope

This analysis identifies associations between customer characteristics and churn, not causes. The dataset does not contain detailed time information explaining when or why each customer left.

A possible next step is to build a machine learning model, such as Logistic Regression or Random Forest, to predict customer churn and evaluate model performance.

## Repository Structure

```text
telco-customer-churn-eda/
│
├── images/
│   ├── churn_distribution.png
│   ├── numerical_features_distribution.png
│   ├── churn_by_customer_services.png
│   ├── numerical_features_vs_churn.png
│   ├── tenure_distribution_by_churn.png
│   ├── churn_by_tenure_group.png
│   ├── tenure_by_contract.png
│   ├── tenure_vs_monthly_charges.png
│   ├── numerical_features_pairplot.png
│   └── correlation_heatmap.png
│
├── Telco_Customer_Churn_EDA.ipynb
├── requirements.txt
└── README.md
```

## How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/sandravinod-web/telco-customer-churn-eda.git
```

### 2. Navigate to the project folder

```bash
cd telco-customer-churn-eda
```

### 3. Install the required libraries

```bash
pip install -r requirements.txt
```

### 4. Download the dataset

Download the IBM Telco Customer Churn dataset from [Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn).

Save the file as `WA_Fn-UseC_-Telco-Customer-Churn.csv` in the same folder as the notebook.

### 5. Launch Jupyter Notebook

```bash
jupyter notebook
```

### 6. Open and run

Open `Telco_Customer_Churn_EDA.ipynb` and run all cells.

## Author

**Sandra V**

Data Science Learner | Python | SQL | Exploratory Data Analysis

GitHub: [sandravinod-web](https://github.com/sandravinod-web)
