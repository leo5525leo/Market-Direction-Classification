## 🧠 Project Overview

This project studies whether the **next-day market direction**
can be predicted using **only market-based variables**
(price, volume, and volatility),
without relying on macroeconomic data.

The goal is to evaluate whether simple, interpretable models
can capture any **stable short-term predictive patterns**
in equity markets.

👉 **[View the interactive HTML report](https://leo5525leo.github.io/Market-Direction-Classification/ML_Final_Project.html)**

---

## 🧮 Features & Target (Summary)

- **Target**: next-day direction (up vs. down)
- **Predictors**:
  - Lagged price direction indicators (past 1–4 days)
  - Interaction terms capturing short-term momentum patterns
  - Simple volatility proxies and volume–volatility interactions

Only market-derived variables are used.

---

## 🧪 Methodology (High-level)

- Logistic regression (binomial GLM)
- Time-series–respecting evaluation:
  - Fixed train–test split (2005–2019 / 2020–2024)
  - Rolling-window re-estimation through time
- Performance evaluated using:
  - Accuracy
  - AUC (ROC)

---

## 📊 Outputs

The analysis produces:
- Out-of-sample accuracy and AUC
- Rolling yearly performance comparisons
- Visual diagnostics to distinguish signal from noise

All figures and detailed results are available in the interactive report.
