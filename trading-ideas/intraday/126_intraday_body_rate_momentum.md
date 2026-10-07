# 126 — Intraday Body Rate Momentum

## Overview

Designed for range-bound or low-trend-strength regimes (ADX < 26.5) where the market is mean-reverting on a daily scale but has strong intraday swings. It triggers entries when the intraday price moves relative to yesterday's range (body_rate) align with total daily momentum, confirmed by nến close position.

---

## Concept

```
Body Rate:
  body_rate = (Close - Session_Open) / (Prev_Day_High - Prev_Day_Low)
```

By measuring the intraday range relative to yesterday's total volatility, we identify when the market is expanding intraday without entering an overextended trending regime.

---

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 5-min chart |
| Markets | VN30F1M |
| ADX Filter | ADX(42) < 26.5 |

### Long Entry
- ADX < 26.5.
- `body_rate > 0.50`.
- Daily momentum `mom_y > 0.20%`.
- Bar close position `bcp > 0.65` (closes near its high).
- Enter Long.

### Short Entry
- ADX < 26.5.
- `body_rate < -0.50`.
- Daily momentum `mom_y < -0.20%`.
- Bar close position `bcp < 0.35` (closes near its low).
- Enter Short.

---

## Exit Rules

- **Trailing Stop:** Exit if price falls below the running intraday high by 0.35% (for long) or rises above the running intraday low by 0.35% (for short).
- **Hard Target:** Normal SL/TP levels from `utils.py`.

---
*Category: Intraday Momentum | Timeframe: Intraday (5-min) | Market: VN30F1M*
