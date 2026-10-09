# 📱 Phone Usage Analysis (India)

Exploratory data analysis of 17,686 mobile users in India covering demographics, screen time, data usage, calls, app usage, spending and recharge cost, including a data-validation step that tests whether the data is realistic.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Phuvanenthran-P/data-analytics-projects/blob/main/phone-usage-analysis/phone_usage_analysis.ipynb)

## What It Does

- Loads and inspects the dataset (structure, missing values, duplicates, negative values)
- Validates the data logically (brand vs OS, activity time vs total screen time)
- Explores distributions and relationships with Matplotlib, Seaborn and Plotly
- Compares screen time across age groups, cities and primary use
- Tests correlations between all numeric variables

## Dataset

`phone_usage_india.csv`: 17,686 users × 16 columns (age, gender, city, phone brand, OS, screen time, data usage, call duration, apps installed, social/streaming/gaming time, e-commerce spend, recharge cost, primary use). The notebook loads it automatically, so no upload is needed.

## Key Findings

- **Typical user:** ~6.5 hrs screen time/day, 25 GB data/month, 151 min calls/day, 105 apps, ₹1,043 monthly recharge, ₹5,076 monthly e-commerce spend.
- **No meaningful relationships:** every pairwise correlation is near zero (strongest: −0.02).
- **Groups look identical:** average screen time differs by only ~0.1 hrs/day across age groups and ~0.25 hrs/day across cities.
- **Balanced categories:** each gender ≈ 33%, OS 50/50, each primary use ≈ 20%.
- **Data quality issues:** Apple phones appear on Android (879 of 1,775), and 76.5% of users have social + streaming + gaming time greater than their total screen time.

**Conclusion:** the dataset is structurally clean but shows the hallmarks of synthetic, randomly generated data, so it cannot support real-world claims about Indian mobile users. The project demonstrates a full EDA workflow and the habit of validating data before trusting it.

## Tech Stack

Python · Pandas · NumPy · Matplotlib · Seaborn · Plotly · Google Colab

## Run It

Click the Colab badge above (use **File → Save a copy in Drive**, then **Runtime → Run all**), or locally:

```bash
pip install pandas numpy matplotlib seaborn plotly jupyter
jupyter notebook phone_usage_analysis.ipynb
```

## Future Improvements

- Repeat the analysis on real telecom or survey data
- Add statistical tests (e.g. ANOVA) across groups
- Build a Streamlit dashboard with filters
