Impact of Clean Air Policy on PM2.5
📖 Project Overview

This project evaluates the effectiveness of a Clean Air Policy in reducing air pollution (PM2.5) levels across multiple regions between 2018 and 2022. The analysis uses statistical methods and visualizations to measure whether the policy had a significant impact on air quality.

Key highlights:
Dataset: 54,900 region–day observations (2018–2022).
Policy intervention: “Policy Active” indicator (0 = before rollout, 1 = after rollout).
Analysis methods: Exploratory trends, T-test, OLS regression, Residuals check, Parallel trends validation, Difference-in-Differences (DiD), Interrupted Time Series (ITS).
Findings: Policy reduced PM2.5 by ~10 units on average, with stronger improvements in urban regions compared to rural.

📂 Project Structure
/ecomm_ab_test
│-- Dataset/
│ └── clean_air_policy_clean.csv
│ └── clean_air_policy_dataset.csv
│-- Notebooks/
│ └── analysis.ipynb
│-- Report
│ └── Visuals
│ └── Report.docx
│ └── Report.pdf
│-- data_dictionary.csv
│-- Impact-of-Clean-Air-Policy-on-PM25-2018-2022_DashBoard.pbix
│-- Impact-of-Clean-Air-Policy-on-PM25-2018-2022.pptx
│-- README.md
│-- requirements.txt

🛠️ Methodology
Data Cleaning
Removed 100 duplicate rows.
Imputed ~200 missing values using median.
Clipped unrealistic values (negative PM2.5, extreme rainfall).

Exploratory Data Analysis
PM2.5 trends over time.
Treated vs control regions comparison.

Statistical Analysis
Mean comparison (T-test).
OLS regression with weather and economic controls.
Residual diagnostics.
Parallel trends check for DiD validity.
DiD estimation.
Interrupted Time Series analysis.
Regional heterogeneity assessment (Urban vs Rural).

Results
Policy reduced PM2.5 by ~10 units (p < 0.05).
Strong effects confirmed by DiD and ITS.
Urban improvements > Rural improvements.

📊 Key Results
| **Analysis Method**           | **Result**                       | **Significance** |
| ----------------------------- | -------------------------------- | ---------------- |
| Mean Comparison (T-test)      | PM2.5 lower after the policy     | ✅ Yes (p < 0.05) |
| OLS Regression                | Policy coefficient negative (-)  | ✅ Yes            |
| Parallel Trends Check         | Pre-policy trends parallel       | ✅ Valid          |
| Difference-in-Differences     | Sharp drop in treated vs control | ✅ Strong         |
| Interrupted Time Series (ITS) | Level shift at policy rollout    | ✅ Strong         |
| Regional Heterogeneity        | Urban regions improved more      | ✅ Clear          |


📌 Conclusion
The Clean Air Policy significantly improved air quality, reducing PM2.5 levels by ~10 units.
Results are consistent across multiple statistical approaches.
Urban areas saw stronger benefits, suggesting enforcement gaps in rural regions.

Policy Recommendations:
Extend interventions to rural areas.
Strengthen enforcement mechanisms.
Add complementary measures (traffic restrictions, clean energy, crop-burning regulation).

🚀 How to Run
Open analysis.ipynb in Jupyter.
Install required libraries:
pip install pandas numpy matplotlib seaborn statsmodels
Run the notebook step by step to reproduce cleaning, analysis, and plots.
