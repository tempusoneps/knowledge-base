# 02 — XGBoost Cross-Sectional Alpha

## Overview
Employ an XGBoost regressor to rank a stock universe based on multi-factor features, buying the top decile and shorting/avoiding the bottom decile.

## Setup & Entry Rules
- Features: Value (P/E, P/B), Momentum (12-1 month), Quality (ROE), and Volatility metrics.
- Train XGBoost model monthly using a rolling 3-year window.
- Enter long positions in the top 10% ranked stocks at the start of each month.

## Exit Rules
- Rebalance monthly: exit positions that fall out of the top 15% rank.
- Exit underperforming assets immediately if they hit a trailing stop of 8%.

## Filters
- Exclude stocks outside the top 100 most liquid equities.
- Skip buying if the model's feature importance for momentum drops below a threshold.

## Risk Management
- Equal-weight the long portfolio. Implement a portfolio-wide drawdown limit of 5% per month.

---
*Category: Machine Learning / Regressor | Timeframe: Monthly | Market: Stocks*
