# TP1 — Returns and Random Walks

**Course:** Statistics and Data Analysis for Financial Engineering  
**Reference:** Statistics and Data Analysis for Financial Engineering, Chapters 1–2  
**Programming Language:** R  
**Field:** Financial Engineering / Quantitative Finance

## Overview

This project explores statistical analysis and mathematical modelling of financial markets using R.

The assignment investigates financial returns, probability distributions, market volatility, random walks, leverage, and Monte Carlo simulation.

Using historical financial datasets, the exercises connect statistical theory with practical financial applications, with particular attention to interpreting quantitative results and evaluating model assumptions.

## Exercise Progress

| Exercise | Topic | Dataset | Status |
|---|---|---|---|
| 01 | Looking at the Data | EuStockMarkets | Completed |
| 02 | The Normal Distribution Is Not Normal | SP500 | Completed |
| 03 | Variances Are Not Constant; Measuring Risk | CRSPday | Completed |
| 04 | Net, Gross, Log and Multi-period Returns | CRSPday, Garch | Completed |
| 05 | Adjustment for Dividends | Coca-Cola (KO) | Completed |
| 06 | Geometric Random Walk | EuStockMarkets | Completed |
| 07 | Leverage and Monte Carlo | CRSPday | Completed |
| 08 | Testing the Random Walk Model | EuStockMarkets | In Progress |

**Overall progress: 7/8 exercises completed (87.5%).**

## Exercise Details

### Exercise 01 — Looking at the Data
- Financial index visualization
- Daily log returns
- Scatterplot matrices
- Correlation analysis
- Historical market performance

### Exercise 02 — The Normal Distribution Is Not Normal
- Extreme daily returns
- Standardized returns
- Normal distribution probabilities
- Student's t-distribution
- Quantile-Quantile (QQ) plots
- Extreme event analysis

### Exercise 03 — Variances Are Not Constant; Measuring Risk
- Annualized volatility
- Time-varying market risk
- Autocorrelation analysis
- Volatility clustering
- Value at Risk (VaR)
- Expected Shortfall (ES)

### Exercise 04 — Net, Gross, Log and Multi-period Returns
- Net and log return conversion
- Wealth accumulation
- Multi-period returns
- Monthly and annual returns
- Exchange rate quotation and inversion

### Exercise 05 — Adjustment for Dividends
- Historical stock prices
- Dividend-adjusted returns
- Total return calculation
- Adjusted closing prices
- Dividend contribution to investment performance

### Exercise 06 — Geometric Random Walk
- Estimation of mean and volatility
- Lognormal geometric random walk
- Monte Carlo simulation (1,000 paths)
- Theoretical versus simulated probabilities
- Autocorrelation of squared returns
- Volatility clustering analysis

### Exercise 07 — Leverage and Monte Carlo
- Financial leverage and liquidation risk
- Estimation of daily return parameters
- Monte Carlo simulation (10,000 paths)
- Normal distribution simulation
- Historical bootstrap simulation
- Stopping times and exit strategies
- Expected profit and holding period
- Comparison of simulation methodologies

### Exercise 08 — Testing the Random Walk Model
- Skewness and excess kurtosis
- Jarque-Bera normality test
- Ljung-Box test
- Autocorrelation of returns and squared returns
- Testing random walk assumptions
- Evaluating model limitations and practical usefulness

## Selected Quantitative Findings

### Exercise 06 — Geometric Random Walk

**DAX parameter estimation**

| Parameter | Result |
|---|---:|
| Mean daily log return | 0.0006520417 |
| Daily volatility | 0.01030084 |

**Monte Carlo simulation**
- Number of simulated paths: 1,000.
- Fraction of paths ending above the actual final DAX value: 47.7%.
- Theoretical one-standard-deviation coverage: 68.27%.
- Simulated coverage was approximately consistent with the theoretical probability.

**Ljung-Box test on squared returns**

| Dataset | p-value | Decision |
|---|---:|---|
| Real DAX | < 2.2 × 10⁻¹⁶ | Reject H₀ |
| Simulated DAX | 0.4903 | Fail to reject H₀ |

The results indicate significant dependence in the squared real DAX returns, which is consistent with volatility clustering. The independent normal simulation does not reproduce this feature.

### Exercise 07 — Leverage and Monte Carlo

**CRSP parameter estimation**

| Parameter | Result |
|---|---:|
| Observations | 2,528 |
| Mean daily log return | 0.0006480784 |
| Daily volatility | 0.007776161 |

**Liquidation probability over 45 trading days**

| Method | Probability |
|---|---:|
| Normal simulation | 13.96% |
| Historical bootstrap | 13.71% |

**Exit strategy over 100 trading days**

| Metric | Normal | Bootstrap |
|---|---:|---:|
| Probability of profit ≥ $100,000 | 57.11% | 57.85% |
| Probability of loss | 22.55% | 22.17% |
| Expected profit | $96,670.41 | $97,076.01 |
| Expected holding time | 67.88 days | 68.13 days |

**Volatility dependence**

The Ljung-Box test on squared CRSP returns produced:

- Test statistic: 519.84
- Degrees of freedom: 20
- p-value: < 2.2 × 10⁻¹⁶

The results provide strong evidence of autocorrelation in squared CRSP returns.

Ordinary bootstrap resampling preserves the empirical distribution of individual returns but destroys their original chronological ordering. Consequently, it does not preserve the historical volatility clustering structure.

## Statistical Methods and Techniques

The assignment applies several statistical and mathematical techniques:

- Descriptive statistics and exploratory data analysis
- Probability distributions and hypothesis testing
- Financial return calculations
- Correlation and autocorrelation analysis
- Volatility estimation
- Risk measurement (VaR and ES)
- Random walk modelling
- Lognormal price simulation
- Monte Carlo methods
- Bootstrap resampling
- Stopping-time analysis
- Model diagnostics and interpretation

## Datasets and R Packages

**Datasets**
- `EuStockMarkets`
- `SP500`
- `CRSPday`
- `Garch`
- Coca-Cola (KO) historical prices and dividends

**R Packages**
- `datasets`
- `Ecdat`
- `quantmod`

## Repository Structure

```text
TP1-Returns-and-Random-Walks/
│
├── README.md
├── TP1.R
│
├── figures/
│   ├── exercise_01/
│   ├── exercise_02/
│   ├── exercise_03/
│   ├── exercise_04/
│   ├── exercise_05/
│   ├── exercise_06/
│   ├── exercise_07/
│   └── exercise_08/
│
└── results/
    ├── exercise_01/
    ├── exercise_02/
    ├── exercise_03/
    ├── exercise_04/
    ├── exercise_05/
    ├── exercise_06/
    ├── exercise_07/
    └── exercise_08/
```

## Learning Objectives

Through this practical assignment, the project develops the ability to:

1. Analyse and interpret historical financial data.
2. Apply probability distributions to financial returns.
3. Measure and interpret financial market volatility.
4. Understand stochastic processes and random walk models.
5. Implement Monte Carlo simulations in R.
6. Evaluate financial risk under leveraged investment strategies.
7. Compare theoretical assumptions with empirical market behaviour.
8. Communicate quantitative findings through statistical interpretation.

## References

*Statistics and Data Analysis for Financial Engineering*, Chapters 1 and 2.

TP1 — Returns and Random Walks, Practical Assignment.

---

**Project Status:** 7 of 8 exercises completed  
**Remaining:** Exercise 08 — Testing the Random Walk Model  
**Programming Language:** R  
**Domain:** Financial Engineering / Quantitative Finance
