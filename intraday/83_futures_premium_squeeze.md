# 83 — Futures Premium Squeeze

## Overview

Trade continuation when VN30F holds a positive premium while cash pulls back shallowly. Persistent premium can signal futures traders are positioning ahead of another cash-index push.

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 1-min and 5-min |
| Markets | VN30F |
| Metric | Basis and cash-index pullback depth |

### Long Entry
1. VN30 cash index is above VWAP.
2. VN30F trades at a positive basis for at least 15 minutes.
3. Cash index pulls back less than 38%-50% of the prior impulse.
4. VN30F refuses to lose VWAP or the morning midpoint.
5. Enter long when VN30F breaks the pullback high.

### Short Entry
1. VN30 cash index is below VWAP.
2. VN30F trades at a persistent discount.
3. Cash bounce retraces less than 38%-50%.
4. VN30F rejects VWAP or prior support from below.
5. Enter short when VN30F breaks the pullback low.

## Exit Rules

- Target prior HOD/LOD and then measured move.
- Exit if basis flips against the trade for 2 consecutive 5-min candles.
- Trail behind 5-min pullback lows/highs.

## Filters

- Best on broad trend days.
- Avoid if premium is caused by temporary data delay.
- Require cash basket breadth confirmation.

## Risk Management

Risk 0.75% maximum. Stop must be on futures structure, not basis alone.

---
*Category: Futures / Trend Continuation | Timeframe: Intraday | Market: VN30F*
