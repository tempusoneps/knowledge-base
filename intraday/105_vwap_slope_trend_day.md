# 105 — VWAP Slope Trend Day

## Overview

Use VWAP slope as the main trend-day filter. When VWAP is rising or falling steadily, pullbacks to dynamic support/resistance have higher odds than mean-reversion fades.

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 5-min chart |
| Markets | VN30F, liquid stocks |
| Indicator | Daily VWAP slope |

### Long Entry
1. VWAP has a clear positive slope for at least 45 minutes.
2. Price remains above VWAP and makes higher lows.
3. Pullback touches VWAP or 9-EMA without closing below both.
4. Enter long on bullish reversal candle or break of pullback high.
5. Stop below VWAP and pullback low.

### Short Entry
1. VWAP has a clear negative slope.
2. Price remains below VWAP and makes lower highs.
3. Bounce touches VWAP or 9-EMA without reclaiming both.
4. Enter short on bearish reversal or break of bounce low.
5. Stop above VWAP and bounce high.

## Exit Rules

- Target HOD/LOD retest, then measured extension.
- Exit if VWAP flattens and price crosses it repeatedly.
- Trail behind 5-min structure.

## Filters

- Avoid flat VWAP days.
- Stronger with breadth confirmation.
- Do not take late entries after three successful VWAP touches.

## Risk Management

Risk 0.75% maximum. Trend-day pullbacks fail when VWAP slope changes, so respect the exit.

---
*Category: VWAP Trend / Continuation | Timeframe: Intraday | Market: VN30F / HSX Stocks*
