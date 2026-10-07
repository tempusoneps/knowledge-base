# 06 — Dual Listing Premium Reversion

## Overview
Trade the premium/discount between dual-listed securities when it deviates from normal bounds.

## Setup & Entry Rules
- Compute adjusted premium after FX, taxes, and settlement costs.
- Enter when premium is beyond historical 90th/10th percentile.
- Long cheaper listing and short expensive listing where accessible.
- Use equal economic exposure.

## Exit Rules
- Exit when premium returns to historical median.
- Stop if structural restriction changes the fair premium.

## Filters
- Account for capital controls and borrow constraints.
- Avoid corporate-action windows.

## Risk Management
This is operationally sensitive. Include all transaction costs before trading.

---
*Category: Cross-Listing Arbitrage | Timeframe: Days-Weeks | Market: Stocks*
