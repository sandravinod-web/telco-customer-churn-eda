# Telco Customer Churn Analysis – Exploratory Data Analysis (EDA)

## Project Overview

This project performs Exploratory Data Analysis (EDA) on the IBM Telco Customer Churn dataset to understand customer behaviour and identify the factors associated with customer churn.

The main objective is to explore customer information, service usage, contract types, payment methods and billing details to discover patterns that may help a telecommunications company improve customer retention.

## Objectives

- Understand the distribution of customers who stayed and churned.
- Analyse numerical and categorical features.
- Identify customer groups with higher churn rates.
- Explore relationships between customer tenure, charges and churn.
- Generate meaningful business insights from the data.

## Dataset

**Dataset:** IBM Telco Customer Churn

- Total records: 7,043 customers
- Total original columns: 21
- Target variable: `Churn`

The dataset contains customer demographics, subscribed services, contract information, payment methods and billing details.

## Technologies and Libraries

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

## Key Findings

### 1. Customer Churn Distribution

- 73.5% of customers stayed.
- 26.5% of customers churned.

![Churn Distribution](images/churn_distribution.png)

### 2. Numerical Feature Distributions

Explored the distributions of customer tenure, monthly charges and total charges.

![Numerical Feature Distributions](images/numerical_features_distribution.png)

### 3. Churn by Customer Services

Compared churn rates across contract types, internet services and payment methods.

Key findings:
- Month-to-month contracts have the highest churn rate (42.71%).
- Fiber optic customers have a high churn rate (41.89%).
- Electronic check users have the highest churn rate (45.29%).

![Churn by Customer Services](images/churn_by_customer_services.png)

### 4. Numerical Features vs Churn

Compared tenure, monthly charges and total charges between customers who stayed and customers who churned.

Key findings:
- Customers who churned generally have shorter tenure.
- Customers who churned have higher average monthly charges.
- Customers who stayed have higher average total charges.

![Numerical Features vs Churn](images/numerical_features_vs_churn.png)

### 5. Churn Rate by Tenure Group

Customers with shorter tenure show higher churn rates.

![Churn by Tenure Group](images/churn_by_tenure_group.png)

### 6. Tenure Distribution by Churn

This chart compares customer tenure distributions for customers who stayed and customers who churned.

![Tenure Distribution by Churn](images/tenure_distribution_by_churn.png)

### 7. Correlation Heatmap

The correlation analysis highlights relationships between numerical features.

Key observations:
- Tenure and TotalCharges have a strong positive correlation (0.83).
- MonthlyCharges and TotalCharges have a positive correlation (0.65).
- Tenure and Churn_flag have a negative correlation (-0.35).

![Correlation Heatmap](images/correlation_heatmap.png)

### 8. Tenure vs Monthly Charges

This scatter plot explores the relationship between customer tenure and monthly charges, with customers grouped by churn status.

![Tenure vs Monthly Charges](images/tenure_vs_monthly_charges.png)

### 9. Tenure by Contract Type

The violin plot compares customer tenure across month-to-month, one-year and two-year contracts.

![Tenure by Contract](images/tenure_by_contract.png)

### 10. Numerical Features Pairplot

The pairplot visualises relationships between tenure, monthly charges and total charges, separated by churn status.

![Numerical Features Pairplot](images/numerical_features_pairplot.png)

## Business Insights

Based on the analysis:

- Focus on improving retention among month-to-month contract customers.
- Investigate customer satisfaction and pricing for fiber optic services.
- Review the customer experience for electronic check users.
- Introduce retention strategies for customers during their first 12 months.
- Monitor customers with higher monthly charges who may be at risk of leaving.

## Conclusion

The analysis shows that customer churn is associated with contract type, tenure, internet service, payment method and billing patterns.

Customers with month-to-month contracts, shorter tenure, fiber optic services and electronic check payments show comparatively higher churn rates.

These findings can help the company develop targeted customer retention strategies and improve customer satisfaction.

## Repository Structure

```text
telco-customer-churn-eda/
│
├── images/
│   ├── churn_distribution.png
│   ├── numerical_features_distribution.png
│   ├── churn_by_customer_services.png
│   ├── numerical_features_vs_churn.png
│   ├── churn_by_tenure_group.png
│   ├── tenure_distribution_by_churn.png
│   ├── correlation_heatmap.png
│   ├── tenure_vs_monthly_charges.png
│   ├── tenure_by_contract.png
│   └── numerical_features_pairplot.png
│
├── Telco_Customer_Churn_EDA.ipynb
└── README.md
```

## How to Run the Project

1. Clone this repository:

```bash
git clone https://github.com/sandravinod-web/telco-customer-churn-eda.git
```

2. Open the project folder:

```bash
cd telco-customer-churn-eda
```

3. Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

4. Open Jupyter Notebook:

```bash
jupyter notebook
```

5. Open `Telco_Customer_Churn_EDA.ipynb` and run the cells.

**Note:** Download the IBM Telco Customer Churn CSV dataset separately and place it in the location expected by the notebook.

## Author

**Sandra V**

Data Science Learner | Python | SQL | Exploratory Data Analysis

GitHub: [sandravinod-web](https://github.com/sandravinod-web)
