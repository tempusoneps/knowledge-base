# 79 — Leader-Laggard Pair Rotation

## Overview

Trade a lagging stock in the same sector when the sector leader breaks out and holds. The idea is not blind catch-up; it requires the laggard to confirm that rotation has started.

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 5-min chart |
| Markets | Same-sector liquid pairs |
| Examples | Bank leaders vs second-tier banks, securities leaders vs laggards |

### Long Entry
1. Sector leader breaks HOD or a major intraday resistance.
2. Sector breadth is positive.
3. Laggard is still below its own HOD but above VWAP.
4. Laggard forms a higher low and breaks a 5-min trigger level.
5. Enter long on the laggard confirmation.

### Short Entry
1. Sector leader breaks LOD or loses VWAP with momentum.
2. Sector breadth turns negative.
3. Laggard is still above its own LOD but below VWAP.
4. Laggard forms a lower high and breaks support.
5. Enter short on confirmation where shorting is available, or use it as an avoid/sell signal.

## Exit Rules

- Target laggard's HOD/LOD or 1.5R.
- Exit if the leader reverses back into its old range.
- Take partials before sector-wide resistance.

## Filters

- Do not trade weak laggards if the leader breakout is already extended.
- Prefer pairs with stable historical correlation.
- Avoid illiquid small caps.

## Risk Management

Risk per trade should be based on laggard volatility, not leader volatility.

---
*Category: Sector Rotation / Relative Strength | Timeframe: Intraday | Market: HSX Stocks*
