# 🚗 Tech Layoffs Analysis & Survival Modeling

[![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)](https://www.python.org/)  
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.5.2-yellow.svg)](https://scikit-learn.org/stable/)  
[![Plotly & Dash](https://img.shields.io/badge/Plotly-Dash-orange.svg)](https://plotly.com/dash/)  
[![Lifelines](https://img.shields.io/badge/Lifelines-0.27.8-green.svg)](https://lifelines.readthedocs.io/)  
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)  

---

## 🔍 Description
This repository contains machine learning pipelines and interactive dashboards for analyzing **tech layoffs**:

- Cluster companies based on **layoff risk** and **funding**.
- Detect **anomalously high layoffs** relative to industry peers.
- Conduct **survival analysis** using **Kaplan–Meier curves** and **Cox Proportional Hazards models** to understand layoff risk over time.

---

## 📊 Tech Layoffs Analysis Dashboard

This project explores global tech layoffs using interactive dashboards and statistical models.
It provides insights into patterns of workforce reductions by industry, stage, country, and funding levels.

Built with Python, Dash, and Plotly, the app integrates:
- Clustering & PCA to group companies by layoff risk.
- Anomaly detection to flag companies with unusually high layoffs relative to industry peers.
- Survival analysis (Kaplan–Meier & Cox Proportional Hazards) to estimate layoff risk over time.

## 🚀 Features
1. Dataset from **Kaggle**: [Tech Layoffs](https://www.kaggle.com/datasets/pranshujayswal/tech-layoffs-and-stock-market-analysis-predicting/data)

2. Exploratory Data Analysis  

3. **Clustering & PCA**  
   - Groups companies based on total layoffs, % workforce reduction, funding, industry, stage, and location.
   - Visualized in 2D PCA space.
   - Filters by industry, stage, and location.
   - Displays cluster summaries: average layoffs, % workforce reduction, and funds raised.

4. **Anomaly Detection**  
   - Uses **Isolation Forest** to identify unusual layoffs relative to peers.
   - Standardizes layoffs within each industry.
   - PCA visualization highlights normal vs anomalous companies.
   - Clusters anomalies for further analysis.
   - Textual summary describes normal and anomalous groups.

5. **Survival Analysis**  
   - **Kaplan–Meier curves**: survival probability over time since first layoff, stratified by funding category (Low/Medium/High).  
   - **Cox Proportional Hazards**: hazard ratios for factors like funding, post-2022 crash indicator, country, or stage.  
   - Textual summaries provide median survival times and highlight significant risk factors.


- Fits a Cox Proportional Hazards model:
i.   Estimates hazard ratios for covariates like Funds raised, Post-2022 crash indicator, Country or Stage (when filtered)
ii.  Displays HRs with 95% confidence intervals.
iii. Textual summary flags statistically significant risk factors.

---

## ⚙️ Installation

1. Clone the repo:
- git clone https://github.com/HRNBEnninful/Tech-Layoffs-Analysis.git
- cd Tech-Layoffs-Analysis
- jupyternotebook Tech_Layoffs.ipynb

2. Create virtual environment and install dependencies:
python -m venv venv
source venv/bin/activate   # On Mac/Linux
venv\Scripts\activate      # On Windows
pip install -r requirements.txt

3. Make sure your dataset (layoffs.csv) is in the data/ folder.
Required columns:
- company
- date
- total_laid_off
- percentage_laid_off
- funds_raised
- stage
- industry
- location
- country

---

### 📊 Example Insights

- Clusters reveal groups of companies with similar layoff patterns (e.g., early-stage startups vs. late-stage).
- Anomaly detection highlights companies whose layoffs are unusually severe relative to peers.
- Survival curves show how long companies survive without layoffs depending on funding.
- Cox PH models identify risk factors significantly associated with higher layoff hazard.

---

## 📌 Requirements

Main dependencies:

- pandas
- numpy
- scikit-learn
- lifelines
- plotly
- dash

Install all requirements:
pip install -r requirements.txt

---

## 🤝 Contributing
Contributions are welcome! 
Please:
- Fork the repository
- Create a feature branch (git checkout -b feature-newmodel)
- Commit changes and push
- Open a Pull Request

---

## 📜 License
MIT License – feel free to use and modify.

---

## 📬 Contact
Henry Reynolds Nana Benyin Enninful
📧 Email: hrnbenninful@gmail.com
🐙 GitHub: @HRNBEnninful
💼 LinkedIn: https://www.linkedin.com/in/henryrnbenninful/

---