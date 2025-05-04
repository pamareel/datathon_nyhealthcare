# New York Hospital Performance Analysis
This project aims to analyze hospital discharge volumes, financial performance, illness severity impacts, and geographic trends to uncover patterns in patient care costs, hospital efficiency, and patient outcomes across New York State from 2009 to 2017, and 2021.

## 💡 Project Objective

Our primary objective is to uncover actionable insights into hospital performance across New York State by:
1. Analyzing hospital discharge volume trends
2. Examining the relationship between illness severity and healthcare costs
3. Identifying hospitals with exceptional financial performance (both profitable and unprofitable)
4. Mapping geographic differences in patient care and financial metrics
5. Ranking hospitals based on custom metrics such as profitability and complexity handling

## 🗂 Data Source  
[Hospital Inpatient Discharges (SPARCS De-Identified): Cost Transparency: Beginning 2009](https://health.data.ny.gov/Health/Hospital-Inpatient-Discharges-SPARCS-De-Identified/7dtz-qxmr/about_data)

## 🧹 Data Preparation

1. Handled missing value by filling the according to the information from data dictionary
2. Convert columns into correct data type
3. Aggregated duplicate rows by recalculated mean and median costs and charges
4. Generated calculated fields including: 
    - Profitability = (Mean Charge - Mean Cost) / Mean Charge Mean
    - Profit = (Mean Charge - Mean Cost) 
    - Severity Weighted Score = (1 × Minor Discharges + 2 × Moderate Discharges + 3 × Major Discharges + 4 × Extreme Discharges) / Total Discharges
5. Merge with external location data (hospital's latitude and longitude)

## 👩🏻‍🍳 Metric Development:
1. **Profitability** metric, used to rank hospitals' financial efficiency
2. **Severity Weighted Score** metric, used to identify hospitals specialized in handling complex patients
3. **Discharge** metric, to detect volume volatility

## 🛠 Tools Used:
- Python for data preparation
- Tableau for visualization and dashboard building
- HTML for document analysis report

## Other Resources Link
- [Python for Cleaning Data](https://github.com/pamareel/pamareel.github.io/blob/main/Datathon_2025.ipynb)
- [Tableau](https://public.tableau.com/views/NYHospitalEfficiencyAnalysis/DischargesbySeverity?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)


**This project is part of 6th DubsTech Datathon 2025, at University of Washington.*
