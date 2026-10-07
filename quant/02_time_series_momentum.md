# 02 — Time-Series Momentum

## Overview
Trade each asset based on its own trend rather than relative rank.

## Setup & Entry Rules
- Signal: 12-month return above zero for long, below zero for flat/short.
- Confirm with price above/below 200-day MA.
- Apply to stocks, ETFs, futures, or sectors.
- Rebalance monthly.

## Exit Rules
- Exit when 12-month return flips sign or price crosses 200-day MA.
- Use ATR trailing stop for faster risk control.

## Filters
- Skip assets with insufficient history.
- Use diversified instruments.

## Risk Management
Volatility target each asset and cap portfolio drawdown.

---
*Category: Quant Trend Following | Timeframe: Monthly | Market: Multi-Asset*
