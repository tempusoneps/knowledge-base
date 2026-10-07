# 07 — GARCH LSTM Volatility Forecaster

## Overview
Combine statistical GARCH models with LSTM neural networks to accurately forecast future market volatility and dynamically target portfolio risk.

## Setup & Entry Rules
- Estimate conditional volatility using a GARCH(1,1) model.
- Feed GARCH residuals and historical returns into an LSTM to forecast next-week volatility.
- Enter positions when forecasted volatility is below historical realized volatility.

## Exit Rules
- Scale down exposure when forecasted volatility spikes above the 90th percentile.
- Exit if model prediction indicates an impending high-volatility regime.

## Filters
- Do not increase exposure if major economic releases (inflation, interest rates) are scheduled.
- Verify model calibration weekly.

## Risk Management
- Target a constant portfolio volatility of 10%. Adjust position sizes inversely to forecasted volatility.

---
*Category: Hybrid ML / Volatility | Timeframe: Weekly | Market: Index Futures*
