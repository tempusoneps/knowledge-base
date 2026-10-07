# 110 — Cumulative Delta Trend Confirm

## Overview

Use cumulative delta to confirm trend continuation. Price pullbacks are bought or sold only when aggressive flow remains aligned with the trend.

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 1-min and 5-min |
| Markets | VN30F, liquid stocks with reliable delta |
| Indicator | Cumulative delta |

### Long Entry
1. Price is above VWAP and in a 5-min uptrend.
2. Cumulative delta makes higher highs with price.
3. Pullback in price does not create a meaningful delta breakdown.
4. Enter long when price breaks the pullback high.
5. Stop below the pullback low.

### Short Entry
1. Price is below VWAP and in a 5-min downtrend.
2. Cumulative delta makes lower lows with price.
3. Bounce does not create meaningful delta recovery.
4. Enter short when price breaks the bounce low.
5. Stop above the bounce high.

## Exit Rules

- Target HOD/LOD extension or 2R.
- Exit if delta diverges strongly against the position.
- Trail with 5-min trend structure.

## Filters

- Avoid flat VWAP range days.
- Best during opening drive or broad market trend.
- Require clean, active prints.

## Risk Management

Risk 0.75% maximum. Delta confirms flow but does not replace stop placement.

---
*Category: Order Flow / Trend Continuation | Timeframe: Intraday | Market: VN30F / Liquid Stocks*
