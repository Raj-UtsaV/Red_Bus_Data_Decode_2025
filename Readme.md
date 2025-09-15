# Red_Bus_Data_Decode_2025

A machine learning / data science project built for the **redBus Data Decode Hackathon 2025** (Analytics Vidhya), focused on forecasting demand (number of travellers) for bus journeys up to **15 days in advance**.

---

## Table of Contents

- [Problem Statement](#problem-statement)  
- [Dataset](#dataset)  
- [Objective](#objective)  
- [Approach / Methodology](#approach--methodology)  
- [Model Details](#model-details)  
- [Getting Started](#getting-started)  
- [Files Description](#files-description)  
- [Results & Evaluation](#results--evaluation)  
---

## Problem Statement

Forecast the number of travellers for a specific journey date, **15 days ahead of time**, using historical booking and related data. The goal is to accurately predict the demand so that business decisions (pricing, marketing, capacity planning) can be optimized.

This is based on the challenge in the hackathon: [redBus Data Decode Hackathon 2025 - Analytics Vidhya](https://www.analyticsvidhya.com/datahack/contest/redbus-data-decode-hackathon-2025/)

---

## Dataset

The dataset includes (or may include) the following:

- Historical booking data (dates, journey details, number of bookings)  
- Journey metadata (source, destination, route)  
- Temporal features (day of week, holidays, etc.)  
- Target: number of travellers/bookings for a journey date (15 days ahead)

> Note: Data (if present) is placed in `Data.zip` in this repository. Update this section if you use different filenames.

---

## Objective

- Build a model or ensemble to forecast demand **15 days ahead** for each journey.  
- Minimize errors (e.g. RMSE, MAE) and produce a submission in the required hackathon format.

---

## Approach / Methodology

Suggested workflow:

1. **Data Exploration & Cleaning** — inspect missing values, outliers, data quality issues.  
2. **Feature Engineering** — temporal features (weekday, holiday flags), lag features, rolling windows.  
3. **Modeling** — baseline models (linear), tree-based models (LightGBM / XGBoost), and time-series models where appropriate.  
4. **Validation** — time-based splits / expanding window CV.  
5. **Prediction & Submission** — horizon = 15 days; prepare `submission.csv`.

---

## Model Details

- Languages & libs: Python, pandas, numpy, scikit-learn, xgboost/lightgbm, matplotlib.  
- Model types tried: Baseline linear models, tree ensembles (LightGBM/XGBoost).  

---

## Getting Started

### Prerequisites

- Python 3.8+  
- Recommended libraries: `pandas`, `numpy`, `scikit-learn`, `lightgbm`, `xgboost`, `matplotlib`, `jupyter`

### Setup

```bash
    git clone https://github.com/Raj-UtsaV/Red_Bus_Data_Decode_2025
    cd Red_Bus_Data_Decode_2025
    python3 -m venv venv
    source venv/bin/activate   
    pip install -r requirements.txt 
    
```

## File Description
- `Data.zip` : Raw / processed dataset used for modelling
- `Model.ipynb` : Jupyter notebook with EDA, feature engineering, modelling, evaluation
- `predictions.csv` : Model’s predictions (validation/test)
- `submission.csv` : Submission file for hackathon evaluation

## Results & Evaluation
- **Validation metric(s)**: MAE,RMSE 
