# Customer Retention & Churn Analysis
### Future Interns — Data Science & Analytics | Task 2 | `FUTURE_DS_02`

---

## Objective
Analyze customer data to identify churn patterns, key retention drivers, and customer lifetime trends for a subscription-based telecom business.

---

## Dataset
- **Source:** [Telco Customer Churn — Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- **Size:** 7,043 rows × 21 columns
- **Columns:** customerID, gender, SeniorCitizen, Partner, Dependents, tenure, PhoneService, MultipleLines, InternetService, OnlineSecurity, OnlineBackup, DeviceProtection, TechSupport, StreamingTV, StreamingMovies, Contract, PaperlessBilling, PaymentMethod, MonthlyCharges, TotalCharges, Churn

---

## Tools Used

| Tool | Purpose |
|------|---------|
| Python (Pandas) | Data loading, cleaning, transformation |
| Matplotlib & Seaborn | Data visualizations |
| Jupyter Notebook | Interactive analysis environment |
| Google Looker Studio | Interactive dashboard |

---

## Data Cleaning Steps
- Converted `TotalCharges` from string to numeric
- Filled missing `TotalCharges` with `MonthlyCharges` for new customers
- Created binary `ChurnBinary` column (1 = Churned, 0 = Retained)
- Created `TenureGroup` for cohort analysis (0–12, 13–24, 25–36, 37–48, 49–60, 61–72 months)
- Created `ChargeGroup` for pricing analysis (Low, Medium, High, Very High)

---

## Dashboard KPIs

| Metric | Value |
|--------|-------|
| Total Customers | 7,043 |
| Churned Customers | 1,869 |
| Churn Rate | 26.54% |
| Avg Monthly Charges | $64.76 |

---

## Analysis Performed

| # | Analysis | Key Finding |
|---|----------|------------|
| 1 | Churn Rate by Contract Type | Month-to-month ~43% vs Two-year ~3% |
| 2 | Churn Rate by Tenure Group | 0–12 months has the highest churn (~47%) |
| 3 | Churn Rate by Payment Method | Electronic check leads at ~45% churn |
| 4 | Churn Rate by Internet Service | Fiber optic = 61.4%, DSL = 27.8%, No internet = 10.8% |
| 5 | Churn Rate by Senior Citizen | Non-seniors = 63.8%, Seniors = 36.2% of churned |

---

## Key Insights

1. **Overall churn rate is 26.54%** — significantly above the industry benchmark of 5–7%
2. **Contract type is the #1 churn driver** — month-to-month customers churn at ~43% vs just ~3% for two-year contracts
3. **New customers churn the most** — customers in the 0–12 month group show the highest churn rate (~47%)
4. **Electronic check payment = highest churn** — at ~45%, far above auto-pay methods
5. **Fiber optic customers churn the most** — 61.4% of internet-related churn comes from fiber optic users
6. **Senior citizens are at higher risk** — representing 36.2% of churned customers despite being a smaller segment

---

## Recommendations

- **Incentivize long-term contracts** — offer discounts for customers switching from monthly to annual plans
- **Improve onboarding** — focus retention efforts on the critical first 12 months
- **Promote auto-pay** — offer bill credits for switching to automatic bank transfer or credit card payments
- **Investigate fiber optic quality** — 61.4% fiber churn suggests a service quality or pricing issue
- **Senior citizen program** — create dedicated support and simplified pricing for senior customers
- **Bundle security services** — customers with Online Security and Tech Support churn significantly less

---

## Live Dashboard
[View Interactive Dashboard on Google Looker Studio]([YOUR-LOOKER-STUDIO-LINK-HERE](https://lookerstudio.google.com/s/mxAfwxXUX-M))

---

## Repository Structure

```
FUTURE_DS_02/
├── FUTURE_DS_02_Churn_Analysis.ipynb
├── FUTURE_DS_02_Dashboard.pdf
├── chart_01_churn_overview.png
├── chart_02_churn_by_tenure.png
├── chart_03_churn_by_contract.png
├── chart_04_churn_by_charges.png
├── chart_05_churn_by_services.png
├── chart_06_churn_by_demographics.png
├── chart_07_churn_by_payment.png
├── chart_08_churn_drivers.png
├── requirements.txt
└── README.md
```

---

*Completed as part of the **Future Interns — Data Science & Analytics** Internship Program*
*Track Code: DS | Task: 02*
