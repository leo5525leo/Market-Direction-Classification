# Predicting Daily S&P 500 Direction with Logistic Regression

This repository contains my ECON 590 Machine Learning final project.  
The goal is to investigate whether we can **predict the daily price direction of the S&P 500 index (^GSPC)** using past price and volatility information.

The full analysis and code are in the R Markdown file:

> `ECON590_ML_Final_Project.Rmd`

---

## Research Question

Can we build a model that predicts whether the **next day's S&P 500 return will be positive (up) or negative (down)**, using only historical market data?

This is closely related to the **Random Walk Theory (RWT)** and market efficiency:  
if daily direction is completely unpredictable, a simple logistic regression should not perform much better than random guessing (AUC ≈ 0.5).

---

## Data

- **Asset**: S&P 500 index (^GSPC)
- **Source**: Yahoo Finance  
  - https://finance.yahoo.com/quote/%5EGSPC/history/
- **Sample period**: 2005–2024 (daily frequency)
- **Raw variables**:
  - `open`, `high`, `low`, `close`, `volume`
  - `vix` (daily VIX index)

In the R Markdown file, the data are loaded from a local CSV:

```r
df <- read.csv("df3333.csv")