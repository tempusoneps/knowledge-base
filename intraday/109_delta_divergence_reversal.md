# 109 — Delta Divergence Reversal

## Overview

Trade reversals when price makes a new high or low but cumulative delta fails to confirm. The idea is that aggressive flow is no longer supporting the price extreme.

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 1-min or 5-min |
| Markets | VN30F or stocks with reliable aggressor data |
| Indicator | Cumulative delta |

### Short Entry
1. Price makes a new intraday high.
2. Cumulative delta makes a lower high.
3. Price closes back below the prior swing high.
4. Enter short on first lower high after the reclaim failure.
5. Stop above the new price high.

### Long Entry
1. Price makes a new intraday low.
2. Cumulative delta makes a higher low.
3. Price reclaims the prior swing low.
4. Enter long on first higher low.
5. Stop below the new price low.

## Exit Rules

- Target VWAP or the previous balance area.
- Exit if delta confirms a new extreme after entry.
- Take partials at 1R.

## Filters

- Requires reliable trade classification.
- Avoid low-volume periods where delta is noisy.
- Stronger near known liquidity levels.

## Risk Management

Divergence is only a warning. Entry requires price confirmation.

---
*Category: Order Flow / Divergence Reversal | Timeframe: Intraday | Market: VN30F / Liquid Stocks*
