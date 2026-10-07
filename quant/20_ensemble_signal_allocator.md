# 20 — Ensemble Signal Allocator

## Overview
Combine multiple weak signals into one allocation score to improve robustness.

## Setup & Entry Rules
- Signals: momentum, value, quality, volatility, breadth, macro trend.
- Normalize each signal to comparable score.
- Allocate to assets with highest ensemble score.
- Rebalance monthly with turnover constraint.

## Exit Rules
- Exit when ensemble score falls below threshold.
- Reduce exposure when portfolio volatility exceeds target.

## Filters
- Remove redundant or unstable signals.
- Use out-of-sample testing before deployment.

## Risk Management
Cap factor exposure, sector exposure, and turnover. Ensemble models fail if all inputs are correlated.

---
*Category: Multi-Signal Quant Allocation | Timeframe: Monthly | Market: Multi-Asset / Stocks*
