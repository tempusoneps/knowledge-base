# 107 — Prior Week VWAP Retest

## Overview

Use the previous week's VWAP as a higher-timeframe intraday decision level. When price retests it during the day, institutions may defend or reject it as a fair-value reference.

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 5-min intraday with weekly VWAP reference |
| Markets | VN30F, liquid stocks |
| Reference | Prior week VWAP |

### Long Entry
1. Price approaches prior week VWAP from above.
2. Intraday selling slows near the level.
3. A 5-min candle reclaims the level after a small undercut.
4. Enter long on reclaim or first higher low.
5. Stop below the retest low.

### Short Entry
1. Price approaches prior week VWAP from below.
2. Buying slows near the level.
3. A 5-min candle rejects and closes back below it.
4. Enter short on rejection continuation.
5. Stop above the retest high.

## Exit Rules

- Target daily VWAP, PDC, or nearest weekly level.
- Exit if price accepts through prior week VWAP for 2 candles.
- Take partial at 1R.

## Filters

- Stronger when prior week VWAP aligns with PDC or volume node.
- Avoid if price has chopped through the level all morning.
- Use adjusted data for corporate actions.

## Risk Management

Weekly levels can be wider zones. Size down if the stop must be wider than normal.

---
*Category: Higher-Timeframe VWAP / Level Trade | Timeframe: Intraday | Market: VN30F / HSX Stocks*
