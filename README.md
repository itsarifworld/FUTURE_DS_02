# Customer Retention & Churn Analysis
### Future Interns — Data Science & Analytics | Task 2 | `FUTURE_DS_02`

---

## Objective
Analyze customer data to identify churn patterns, key retention drivers, and customer lifetime trends for a subscription-based telecom business.

---

## 📂 Dataset
- **Source:** [Telco Customer Churn — Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- **Size:** 7,043 rows × 21 columns
- **Columns:** customerID, gender, SeniorCitizen, Partner, Dependents, tenure, PhoneService, MultipleLines, InternetService, OnlineSecurity, OnlineBackup, DeviceProtection, TechSupport, StreamingTV, StreamingMovies, Contract, PaperlessBilling, PaymentMethod, MonthlyCharges, TotalCharges, Churn

> **Note:** Dataset not included due to GitHub's 25MB limit. Download from [Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn).

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
- Created `TenureGroup` for cohort analysis (0-12, 13-24, ... months)
- Created `ChargeGroup` for pricing analysis

---

## Analysis Performed

| # | Analysis | Chart |
|---|----------|-------|
| 1 | Overall Churn vs Retention | Pie + Bar Chart |
| 2 | Churn by Tenure Group (Cohort) | Bar Chart |
| 3 | Churn by Contract Type | Bar + Grouped Bar |
| 4 | Churn by Monthly Charges | Histogram + Bar |
| 5 | Churn by Service Type | Multi Bar Chart |
| 6 | Churn by Demographics | Multi Bar Chart |
| 7 | Churn by Payment Method | Horizontal Bar |
| 8 | Churn Drivers Heatmap | Horizontal Bar |

---

## Key Insights

1. **Overall churn rate is ~26%** — significantly above the industry benchmark of 5-7%
2. **Contract type is the #1 driver** — month-to-month customers churn at 43% vs 3% for two-year contracts
3. **New customers churn the most** — 0-12 month customers have the highest churn rate
4. **Senior citizens are high risk** — churn rate nearly double that of non-seniors
5. **Fiber optic customers churn more** — possible service quality or pricing issue
6. **Electronic check payment = high churn** — customers on manual payment methods leave more

---

## Recommendations

- **Incentivize long-term contracts** — offer discounts for annual/bi-annual sign-ups
- **Improve onboarding** — focus on first 12 months to reduce early churn
- **Senior citizen program** — dedicated support and simplified pricing
- **Investigate fiber optic quality** — address service complaints proactively
- **Promote auto-pay** — offer bill credits for switching to automatic payments
- **Add value through security services** — customers with Online Security churn significantly less

---

## Live Dashboard
[View Interactive Dashboard on Google Looker Studio]([YOUR-LOOKER-STUDIO-LINK-HERE](https://lookerstudio.google.com/s/qjWqQtGllsY))

---

## Repository Structure

```
FUTURE_DS_02/
├── FUTURE_DS_02_Churn_Analysis.ipynb
├── chart_01_churn_overview.png
├── chart_02_churn_by_tenure.png
├── chart_03_churn_by_contract.png
├── chart_04_churn_by_charges.png
├── chart_05_churn_by_services.png
├── chart_06_churn_by_demographics.png
├── chart_07_churn_by_payment.png
├── chart_08_churn_drivers.png
├── FUTURE_DS_02_Dashboard.pdf
├── requirements.txt
└── README.md
```

---

*Completed as part of the **Future Interns — Data Science & Analytics** Internship Program*  
*Track Code: DS | Task: 02*
