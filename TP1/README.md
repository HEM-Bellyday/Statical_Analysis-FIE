# TP1 — Returns and Random Walks

**Course:** Statistics and Data Analysis for Financial Engineering  
**Software:** R / Quarto  
**Status:** 8 of 8 exercises completed

## Overview

This repository contains my work for TP1, focusing on financial returns, statistical distributions, risk measurement, geometric random walks, and Monte Carlo simulation.

The assignment explores how mathematical and statistical methods can be applied to financial market data to understand asset returns, market risk, and price dynamics.

## Repository Structure

```text
TP1/
├── README.md
├── TP1.pdf
└── TP1.qmd
```

| File | Description |
|---|---|
| `README.md` | Project overview, progress, and key findings |
| `TP1.pdf` | Original assignment instructions |
| `TP1.qmd` | Quarto source containing R code, analysis, visualizations, and interpretations |

## Exercise Progress

| Exercise | Topic | Status |
|---|---|---|
| 1 | Looking at Financial Data | Completed |
| 2 | Normal Distribution Is Not Normal | Completed |
| 3 | Variances Are Not Constant: Risk | Completed |
| 4 | Net, Gross, Log and Multi-period Returns | Completed |
| 5 | Adjustment for Dividends | Completed |
| 6 | Geometric Random Walk | Completed |
| 7 | Leverage and Monte Carlo Simulation | Completed |
| 8 | Testing the Random Walk Model | Completed |

**Progress: 8/8 exercises completed (100%).**

## Key Topics and Methods

### 1. Financial Returns
- Net and gross returns
- Logarithmic returns
- Multi-period returns
- Dividend adjustments

### 2. Statistical Analysis
- Descriptive statistics
- Normal distribution assumptions
- Return distributions
- Variance and volatility analysis
- Autocorrelation analysis

### 3. Stochastic Modeling
- Geometric random walk
- Lognormal price simulation
- Monte Carlo simulation
- Random walk assumptions

### 4. Financial Risk
- Leverage and equity exposure
- Margin and liquidation thresholds
- First-passage and stopping-time analysis
- Historical bootstrap simulation
- Risk probability estimation

## Selected Findings

### Exercise 6 — Geometric Random Walk

Using DAX market data from `EuStockMarkets`:

- Estimated daily mean log return: **0.0006520**
- Estimated daily volatility: **0.0103008**
- Simulated 1,000 geometric random walk paths.
- Approximately **47.7%** of simulated paths ended above the actual final DAX price.

The analysis also compared squared-return autocorrelation between actual market data and simulated paths. The basic geometric random walk model did not reproduce the volatility clustering observed in the actual data.

### Exercise 7 — Leverage and Monte Carlo Simulation

Using daily CRSP market returns:

- Estimated daily mean log return: **0.0006481**
- Estimated daily volatility: **0.0077762**
- Simulated 10,000 investment paths over 45 trading days.

Estimated probability of breaching the $950,000 liquidation threshold:

| Simulation Method | Probability |
|---|---:|
| Normal distribution | 13.96% |
| Historical bootstrap | 13.71% |

For the 100-day stopping strategy:

| Metric | Normal | Bootstrap |
|---|---:|---:|
| Probability of profit ≥ $100,000 | 57.11% | 57.85% |
| Probability of loss | 22.55% | 22.17% |
| Expected profit | $96,670.41 | $97,076.01 |
| Expected holding period | 67.88 days | 68.13 days |

The comparison illustrates how different return-generation assumptions can influence simulated investment outcomes. The ordinary historical bootstrap preserves the empirical return distribution but does not preserve the original time ordering or volatility clustering.

## Datasets and R Packages

**Datasets**
- `EuStockMarkets`
- `SP500`
- `CRSPday`
- Coca-Cola (`KO`) market data

**R packages used across the assignment**
- `Ecdat`
- `quantmod`
- `tseries`
- `PerformanceAnalytics`

## Learning Objectives

Through this assignment, I aim to:

- Understand different ways to calculate and interpret financial returns.
- Investigate the statistical properties of financial time series.
- Apply stochastic processes to model asset-price movements.
- Use Monte Carlo simulation to estimate financial risks.
- Compare theoretical assumptions with empirical market behavior.
- Interpret quantitative results in a financial context.

## How to Run

1. Clone or download this repository.
2. Open `TP1.qmd` in RStudio.
3. Install the required R packages if they are not already installed.
4. Run the code chunks sequentially or render the Quarto document.

## References

Original assignment: `TP1.pdf`.

---

*This project is part of my learning journey in Financial Engineering, Statistics, and Quantitative Finance.*
