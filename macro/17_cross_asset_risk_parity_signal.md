# 17 — Cross-Asset Risk Parity Signal

## Overview
Adjust equity exposure based on joint signals from equities, bonds, commodities, and FX volatility.

## Setup & Entry Rules
- Risk-on: equities up, credit spreads down, volatility down, growth-sensitive commodities firm.
- Risk-off: equities below 50-day, credit spreads up, vol up, safe assets bid.
- Enter risk-on basket or defensive hedge after 2-3 confirmations.

## Exit Rules
- Exit when at least two cross-asset confirmations reverse.
- Rebalance weekly.

## Filters
- Avoid relying on one asset class.
- Use liquid proxies only.

## Risk Management
Volatility-target total exposure. This is an allocation model, not a single trade.

---
*Category: Cross-Asset Regime | Timeframe: Weeks | Market: Multi-Asset*
