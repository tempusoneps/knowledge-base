# 77 — Realized Volatility Compression Break

## Overview

This strategy detects a market that has gone temporarily inactive and trades the first directional break once realized volatility wakes up. It is useful for midday sessions where price coils after the morning move.

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 1-min or 5-min |
| Markets | VN30F, liquid stocks |
| Measure | Rolling 20-bar realized volatility |

### Long Entry
1. Rolling realized volatility falls into the lowest 20% of the day.
2. Price holds above VWAP or above the morning midpoint.
3. A candle closes above the compression box high.
4. The next candle holds above the breakout level.
5. Enter long on continuation.

### Short Entry
1. Rolling realized volatility falls into the lowest 20% of the day.
2. Price holds below VWAP or below the morning midpoint.
3. A candle closes below the compression box low.
4. The next candle fails to reclaim the box.
5. Enter short on continuation.

## Exit Rules

- Use the opposite side of the box as the initial stop.
- Target the next intraday swing or 1.5x box height.
- Exit if volatility expands but direction does not follow.

## Filters

- Avoid boxes smaller than the spread plus fees.
- Prefer compression lasting at least 20 bars.
- Skip if price is directly inside a major daily support/resistance zone.

## Risk Management

Trade only one breakout direction per box. A failed long should not automatically become a short unless a new setup forms.

---
*Category: Volatility / Breakout | Timeframe: Intraday | Market: VN30F / HSX Stocks*
