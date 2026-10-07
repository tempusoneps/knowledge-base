# 12 — ATR Breakout System

## Overview
Trade breakouts only when price exceeds recent range by an ATR-adjusted threshold.

## Setup & Entry Rules
- Long when close > 20-day high + 0.25 ATR.
- Short/flat when close < 20-day low - 0.25 ATR.
- Size by ATR.
- Rebalance daily or weekly.

## Exit Rules
- Exit on 10-day low for longs or 10-day high for shorts.
- Stop at 2 ATR from entry.

## Filters
- Avoid low-liquidity instruments.
- Trend regime filter improves results.

## Risk Management
Cap correlated positions and total ATR risk.

---
*Category: Systematic Breakout | Timeframe: Days-Weeks | Market: Stocks / Futures*
