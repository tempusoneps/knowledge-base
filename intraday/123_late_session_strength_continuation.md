# 123 — Late Session Strength Continuation

## Overview

In the Vietnamese phái sinh (futures) market, the final hour of trading (13:15 – 14:15) often exhibits strong, one-directional trends as institutions and proprietary desks complete their daily positioning. This strategy identifies late-session strong momentum based on RSI(8), VWAP deviation, and session body expansion, and enters a trend-continuation trade targeting the close.

---

## Concept

```
Late-Session Trend Continuation:
  At 13:25, 13:40, or 13:55:
  IF Price is extended from session open (large body_pct)
  AND RSI(8) is at momentum levels (>60 for long, <40 for short)
  AND Price is extended from intraday VWAP
  → Enter trend continuation trade, holding until 14:25.
```

---

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 5-min chart |
| Markets | VN30F1M |
| Entry Times | 13:25, 13:40, 13:55 |

### Long Entry
- Time is exactly 13:25, 13:40, or 13:55.
- RSI(8) $\ge 60$.
- Price is above intraday VWAP.
- Intraday body expansion (price is significantly above the day's first open price).
- Enter Long on nến close.

### Short Entry
- Time is exactly 13:25, 13:40, or 13:55.
- RSI(8) $\le 40$.
- Price is below intraday VWAP.
- Intraday body compression (price is significantly below the day's first open price).
- Enter Short on nến close.

---

## Exit Rules

- **Take Profit / Stop Loss:** Uses standard closing position levels from `utils.py`.
- **Force Close:** Market on close at 14:25.

---
*Category: Closing Flow / Momentum | Timeframe: Intraday (5-min) | Market: VN30F1M*
