# 11 — Volatility Targeted Trend

## Overview
Run a trend-following strategy where position size adjusts inversely with realized volatility.

## Setup & Entry Rules
- Long asset when price is above 200-day MA.
- Flat or short when below 200-day MA.
- Position size targets fixed annualized volatility.
- Rebalance weekly or monthly.

## Exit Rules
- Exit when trend signal flips.
- Reduce exposure automatically when volatility spikes.

## Filters
- Use liquid assets only.
- Cap leverage and turnover.

## Risk Management
Portfolio-level volatility target plus max drawdown kill switch.

---
*Category: Quant Trend / Risk Sizing | Timeframe: Weeks-Months | Market: Multi-Asset*
