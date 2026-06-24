# Understanding the Macroeconomic Signals Behind the US Dollar Index (DXY)

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Machine Learning](https://img.shields.io/badge/Machine-Learning-green)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-orange)
![Random Forest](https://img.shields.io/badge/Model-RandomForest-success)

![DXY Project Cover](images/dxy_cover.png)

A machine learning study investigating the relationship between macroeconomic indicators and the US Dollar Index (DXY).

Developed during the M.Sc. in Artificial Intelligence and Big Data at Queen's University.

**Team:** Esraa Mohammed Elsayed · Aya Said Abdallah Noah

---

## Overview

Which macroeconomic indicators move the US Dollar Index (DXY), and how long does it take for their effect to appear?

This project investigates that question using 27 years of Federal Reserve economic data. We collected, integrated, and analyzed multiple macroeconomic indicators, engineered lag-based features, and compared classical linear models against non-linear machine learning approaches.

Our goal was to identify the most influential economic indicators affecting DXY and determine whether their effects are immediate or delayed.

---

## Business Impact

Understanding delayed macroeconomic effects on the US Dollar Index can support:

- Currency forecasting
- Portfolio allocation
- Financial risk management
- Economic policy analysis
- Quantitative research

---

## Key Results

| Model | Exchange Rates R² | Labor Market R² | Housing R² | Inflation R² |
|---|---|---|---|---|
| Linear Regression | < 0 (fails) | < 0 (fails) | < 0 (fails) | < 0 (fails) |
| Ridge | < 0 (fails) | < 0 (fails) | < 0 (fails) | < 0 (fails) |
| ElasticNet | < 0 (fails) | < 0 (fails) | < 0 (fails) | < 0 (fails) |
| **Random Forest** | **High (+)** | **High (+)** | **High (+)** | **High (+)** |

### Main Findings

- Linear models consistently failed to explain DXY variance.
- Random Forest successfully captured non-linear relationships.
- Exchange rates exert the strongest immediate influence.
- Housing, labor market, inflation, and credit indicators show delayed effects.
- Most macroeconomic signals reach their strongest impact after approximately 1–3 months.

---

## Visual Summary

| Model Performance | Feature Importance |
|---|---|
| ![Model Performance](images/model_performance.png) | ![Feature Importance](images/feature_importance.png) |

| Correlation Matrix | Lag Analysis |
|---|---|
| ![Correlation Matrix](images/correlation_matrix.png) | ![Lag Analysis](images/lag_analysis.png) |

---

## Repository Structure

```text
Understanding-DXY-Macroeconomic-Signals/
│
├── notebooks/
│   ├── 01_data_preparation.ipynb
│   └── 02_modeling_and_analysis.ipynb
│
├── data/
│   ├── raw/
│   └── processed/
│
├── reports/
│   ├── Final_Report.pdf
│   ├── Proposal.pdf
│   └── Presentation.pdf
│
├── video/
│   └── demo.mp4
│
├── images/
│   ├── dxy_cover.png
│   ├── model_performance.png
│   ├── feature_importance.png
│   ├── correlation_matrix.png
│   └── lag_analysis.png
│
├── requirements.txt
│
└── README.md
```

---

## Dataset

### Source

Federal Reserve Economic Data (FRED)

### Time Range

1994 – 2021

### Frequency

Daily observations aggregated to monthly frequency.

### Target Variable

DXY Close Price

### Feature Categories

- Exchange Rates
- Interest Rates
- Labor Market
- Inflation
- Credit Conditions
- Housing & Real Estate
- Money Supply and Economic Output

### Feature Engineering

All macroeconomic indicators were transformed into:

- Lag-1
- Lag-2
- Lag-3

features to capture delayed macroeconomic effects.

---

## Methodology

### Data Preparation

- Data collection from Federal Reserve sources
- Dataset integration and cleaning
- Missing value handling
- Monthly aggregation
- Lag feature engineering

### Models

#### Linear Baselines

- Linear Regression
- Ridge Regression
- ElasticNet

#### Non-Linear Model

- Random Forest Regressor

### Evaluation Metrics

- R² Score
- RMSE
- MAE

---

## Contributions

### Esraa Mohammed Elsayed

- Data preprocessing and feature engineering
- Lag feature generation
- Machine Learning modeling
- Feature importance analysis
- Presentation preparation

### Aya Said Abdallah Noah

- Data collection and integration
- Data analysis
- Model evaluation
- Visualization
- Documentation
- Video production

---

## Setup

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Run

```bash
jupyter notebook notebooks/01_data_preparation.ipynb
```

Then:

```bash
jupyter notebook notebooks/02_modeling_and_analysis.ipynb
```

---

## Academic Context

This project was completed during the M.Sc. in Artificial Intelligence and Big Data as part of advanced coursework in Machine Learning and Data Analytics.

---

## Future Work

- Apply stationarity transformations and differencing techniques
- Explore LSTM-based forecasting architectures
- Incorporate news and sentiment indicators
- Extend evaluation to post-2021 economic conditions
- Compare additional ensemble and deep learning models

---

## References

- Meese & Rogoff (1983)
- Breiman (2001)
- Gu, Kelly & Xiu (2020)
- Plakandaras et al. (2015)
- Medeiros et al. (2021)

For the complete bibliography, see:

`reports/Report.pdf`