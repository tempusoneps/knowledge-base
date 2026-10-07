# 81 — Index Breadth Divergence Fade

## Overview

Fade an index move when the headline index pushes to a new intraday extreme but internal breadth fails to confirm. The setup is useful when a few large components pull the index while most stocks stop participating.

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 5-min chart |
| Markets | VN30F, VN30 basket |
| Breadth Metric | Advancers/decliners or percent above VWAP |

### Short Entry
1. VN30 or VN30F makes a new HOD.
2. Fewer components are above VWAP than on the previous HOD.
3. The index candle closes back below the breakout level.
4. Enter short after a lower high forms on 1-min or 5-min.
5. Stop above the failed HOD.

### Long Entry
1. VN30 or VN30F makes a new LOD.
2. Fewer components are below VWAP than on the previous LOD.
3. The index reclaims the breakdown level.
4. Enter long after a higher low forms.
5. Stop below the failed LOD.

## Exit Rules

- First target: VWAP or morning midpoint.
- Second target: opposite side of the failed breakout range.
- Exit if breadth confirms the new extreme after entry.

## Filters

- Avoid strong trend days where breadth remains above 75% in the trend direction.
- Best after 10:00 when enough breadth data exists.
- Check bank and large-cap leadership separately.

## Risk Management

Risk 0.5%-0.75%. This is a fade setup, so never average against a confirmed trend.

---
*Category: Breadth / Mean Reversion | Timeframe: Intraday | Market: VN30F / VN30 Basket*
