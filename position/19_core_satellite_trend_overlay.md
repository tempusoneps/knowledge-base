# 19 — Core-Satellite Trend Overlay

## Overview
Use a long-term trend filter to decide whether portfolio core exposure should be fully invested or reduced.

## Setup & Entry Rules
- Core market index above rising 10-month MA: allow full core exposure.
- Index below falling 10-month MA: reduce core exposure.
- Satellite positions are added only when index and sector trends align.
- Rebalance monthly, not daily.

## Exit Rules
- Reduce exposure on monthly close below 10-month MA.
- Restore exposure on monthly reclaim with breadth improvement.

## Filters
- Avoid whipsaw by using monthly close only.
- Confirm with market breadth or credit conditions.

## Risk Management
This is portfolio-level risk control. Keep rules mechanical and precommitted.

---
*Category: Portfolio Overlay / Position | Timeframe: Position | Market: Stocks / ETFs*
