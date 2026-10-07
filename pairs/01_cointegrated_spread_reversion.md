# 01 — Cointegrated Spread Reversion

## Overview
Trade mean reversion between two stocks whose price series are cointegrated, not merely correlated.

## Setup & Entry Rules
- Select same-sector liquid stocks.
- Confirm cointegration over rolling 1-2 year window.
- Compute hedge ratio and spread z-score.
- Enter long spread below -2 z-score, short spread above +2.
- Use dollar or beta-neutral sizing from hedge ratio.

## Exit Rules
- Exit when spread returns to 0 to 0.5 z-score.
- Stop if z-score moves beyond 3 or cointegration breaks.

## Filters
- Avoid pairs with fresh single-name catalyst.
- Re-estimate hedge ratio periodically.

## Risk Management
Cap pair risk at 0.5%-1% of equity. Watch borrow, liquidity, and corporate actions.

---
*Category: Statistical Pairs / Mean Reversion | Timeframe: Days-Weeks | Market: Stocks*
