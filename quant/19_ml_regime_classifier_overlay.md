# 19 — Machine Learning Regime Classifier Overlay

## Overview
Use a simple ML classifier to switch exposure based on market regime probabilities.

## Setup & Entry Rules
- Features: trend, volatility, breadth, credit, rates, FX, sector dispersion.
- Target: forward index return or drawdown regime.
- Increase exposure only when risk-on probability exceeds threshold.
- Reduce exposure when risk-off probability rises.

## Exit Rules
- Rebalance weekly/monthly as probabilities update.
- Disable model if live performance deviates from validation.

## Filters
- Use walk-forward validation and no lookahead data.
- Prefer interpretable features.

## Risk Management
Model output should scale exposure, not override hard stops.

---
*Category: ML / Regime Overlay | Timeframe: Weeks-Months | Market: Multi-Asset*
