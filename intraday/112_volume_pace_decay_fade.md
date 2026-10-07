# 112 — Volume Pace Decay Fade

## Overview

Fade an intraday move when price continues marginally in the same direction but volume pace decays sharply. The setup targets exhaustion after the active participants have already acted.

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 5-min chart |
| Markets | VN30F, liquid stocks |
| Metric | Volume pace versus prior 30-60 minutes |

### Short Entry
1. Price pushes to a new high after an extended rally.
2. Volume pace is lower than during the previous impulse.
3. Candle closes back below prior high or forms a rejection wick.
4. Enter short on break of rejection candle low.
5. Stop above exhaustion high.

### Long Entry
1. Price pushes to a new low after an extended selloff.
2. Volume pace is lower than during the prior sell impulse.
3. Candle reclaims prior low or forms a long lower wick.
4. Enter long on break of rejection candle high.
5. Stop below exhaustion low.

## Exit Rules

- Target VWAP, 9-EMA, or prior consolidation.
- Exit if fresh volume returns in the trend direction.
- Take partials at 1R.

## Filters

- Avoid fading strong news trends.
- Best after at least two impulse legs.
- Confirm with RSI or delta divergence if available.

## Risk Management

Risk 0.5%. Exhaustion fades require quick invalidation if trend resumes.

---
*Category: Volume Exhaustion / Reversal | Timeframe: Intraday | Market: VN30F / HSX Stocks*
