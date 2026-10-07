# 13 — Z-Score Mean Reversion Basket

## Overview
Trade a basket of liquid stocks that deviate significantly from their rolling mean.

## Setup & Entry Rules
- Compute z-score of price versus 20-day moving average.
- Long stocks below -2 z-score if long-term trend is positive.
- Short/avoid stocks above +2 z-score if trend is negative.
- Hold until z-score normalizes.

## Exit Rules
- Exit at z-score near 0.
- Stop if z-score exceeds +/-3 or trend filter breaks.

## Filters
- Exclude earnings/news events.
- Sector-neutral basket preferred.

## Risk Management
Use many small positions; mean reversion can fail during trends.

---
*Category: Quant Mean Reversion | Timeframe: Days-Weeks | Market: Stocks*
