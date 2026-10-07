# 20 — Residual Alpha After Factor Hedge

## Overview
Long a stock with positive residual momentum after hedging market, sector, size, and value factors.

## Setup & Entry Rules
- Run factor regression on candidate returns.
- Residual return trend is positive and statistically meaningful.
- Hedge with sector/factor basket.
- Enter when residual series breaks a 60-day high.

## Exit Rules
- Exit when residual momentum turns negative.
- Stop if realized residual drawdown exceeds threshold.

## Filters
- Requires clean data and stable factor estimates.
- Avoid periods with major corporate-action distortion.

## Risk Management
Monitor factor exposure drift weekly. This is model-dependent and needs validation.

---
*Category: Factor-Neutral Pair / Quant RV | Timeframe: Weeks | Market: Stocks*
