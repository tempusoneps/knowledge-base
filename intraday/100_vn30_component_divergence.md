# 100 — VN30 Component Divergence

## Overview

Trade VN30F reversals when the futures contract makes a new extreme but key heavyweight components fail to confirm. The strategy focuses on index construction rather than broad market breadth.

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 5-min chart |
| Markets | VN30F |
| Confirmation | Top-weight VN30 components |

### Short Entry
1. VN30F makes a new HOD.
2. Several top-weight components fail to make new highs.
3. Futures candle closes back below the breakout level.
4. Enter short on first lower high after the failure.
5. Stop above futures HOD.

### Long Entry
1. VN30F makes a new LOD.
2. Several top-weight components fail to make new lows.
3. Futures reclaims the breakdown level.
4. Enter long on first higher low.
5. Stop below futures LOD.

## Exit Rules

- Target futures VWAP or prior balance midpoint.
- Exit if heavyweight components start confirming the futures extreme.
- Take partials at 1R.

## Filters

- Stronger when banks and Vingroup-related names both diverge.
- Avoid if one very large component justifies the index move alone.
- Use real-time component data.

## Risk Management

Risk 0.5%-0.75%. Divergence can persist, so wait for futures trigger before entry.

---
*Category: Index Components / Reversal | Timeframe: Intraday | Market: VN30F*
