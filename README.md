# 📉 Telco Customer Churn Analysis

An exploratory data analysis (EDA) project in **Python** that finds out *why customers leave* a telecom company and which customer groups are most at risk, so the business can plan better retention strategies.

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-EDA-150458?logo=pandas&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-4c72b0)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)

---

## 📌 Table of Contents
- [Problem Statement](#-problem-statement)
- [Dataset](#-dataset)
- [Tools & Libraries](#-tools--libraries)
- [Project Workflow](#-project-workflow)
- [Key Insights](#-key-insights)
- [Recommendations](#-recommendations)
- [Repository Structure](#-repository-structure)
- [How to Run](#-how-to-run)
- [Author](#-author)

---

## 🎯 Problem Statement
Acquiring a new customer costs far more than keeping an existing one. This project analyses customer data to:
- Measure the overall **churn rate**
- Identify the **factors linked to churn** (contract type, payment method, tenure, services, demographics)
- Suggest **data-backed retention strategies**

---

## 📂 Dataset
The analysis uses the **Telco Customer Churn** dataset (`Customer Churn.csv`), where each row is a customer.

| Category | Columns |
|---|---|
| Customer info | `customerID`, `gender`, `SeniorCitizen`, `Partner`, `Dependents` |
| Account info | `tenure`, `Contract`, `PaperlessBilling`, `PaymentMethod`, `MonthlyCharges`, `TotalCharges` |
| Services | `PhoneService`, `MultipleLines`, `InternetService`, `OnlineSecurity`, `OnlineBackup`, `DeviceProtection`, `TechSupport`, `StreamingTV`, `StreamingMovies` |
| Target | `Churn` (Yes / No) |

---

## 🛠 Tools & Libraries
- **Python**
- **Pandas** and **NumPy** for data cleaning and manipulation
- **Matplotlib** and **Seaborn** for visualisation
- **Jupyter Notebook**

---

## 🔄 Project Workflow
1. **Data loading:** read the CSV and inspect it with `info()`, `describe()` and `head()`.
2. **Data cleaning**
   - Blank `TotalCharges` values (customers with tenure = 0) replaced with `0` and converted to `float`
   - Checked for null values and duplicate `customerID`s
   - Converted `SeniorCitizen` from 0/1 to No/Yes for readability
3. **Exploratory data analysis**
   - Churn distribution (count plot and pie chart)
   - Churn by senior citizen status (stacked percentage bar chart)
   - Tenure distribution by churn (histogram)
   - Churn by contract type
   - Churn across phone, internet and add-on services (grid of count plots)
   - Churn by payment method
4. **Insights and recommendations:** summarised in the report PDF.

---

## 🔍 Key Insights

| Factor | Finding |
|---|---|
| **Overall churn** | **26.54%** of customers have churned |
| **Contract type** | Month-to-month customers churn far more than 1-year or 2-year contract customers |
| **Payment method** | Customers paying by **electronic check** are the most likely to churn |
| **Tenure** | Most churn happens in the **first few months**; long-tenure customers tend to stay |
| **Senior citizens** | A larger share of senior citizens churn than non-seniors |
| **Services** | Customers without Online Security, Online Backup or Tech Support churn more; customers with Phone and DSL internet service are more likely to stay |

> 📄 Detailed numbers and discussion are in [`Telco_Customer_Churn_Analysys.pdf`](Telco_Customer_Churn_Analysys.pdf).

---

## 💡 Recommendations
- **Promote long-term contracts** with discounts or loyalty benefits to move customers away from month-to-month plans.
- **Encourage safer, automatic payment methods** (credit card, bank transfer) instead of electronic checks.
- **Strengthen early-tenure engagement** with onboarding calls, welcome offers and follow-ups in the first year.
- **Create senior-citizen retention programs** such as dedicated support and simple plans.
- **Bundle protection and support services** (Online Security, Tech Support, Backup) to increase stickiness.

---

## 📁 Repository Structure
```
├── Customer Churn.csv                  # Dataset
├── TCA.ipynb                           # Jupyter notebook with full analysis
├── Telco_Customer_Churn_Analysys.pdf   # Summary report and recommendations
└── README.md
```

---

## ▶️ How to Run
1. Clone the repository
   ```bash
   git clone https://github.com/<your-username>/<your-repo-name>.git
   cd <your-repo-name>
   ```
2. Install the dependencies
   ```bash
   pip install pandas numpy matplotlib seaborn jupyter
   ```
3. Launch the notebook
   ```bash
   jupyter notebook TCA.ipynb
   ```
4. Make sure `Customer Churn.csv` is in the same folder as the notebook, then run all cells.

---

## 👩‍💻 Author
**Gayatri Marathe**
Data Analyst (Fresher) | SQL · Python · Power BI · Excel

- 🔗 LinkedIn: `<add your LinkedIn link>`
- 📧 Email: `<add your email>`
- 💻 GitHub: `<add your GitHub link>`

⭐ If you found this project useful, consider giving it a star!
