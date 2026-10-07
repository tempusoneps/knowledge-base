# 125 — ORB with Body Strength Filter

## Overview

Opening Range Breakouts (ORB) are prone to false breakouts when the breakout candle is a weak doji or has long wicks indicating exhaustion. This strategy filters ORB entries by requiring the breakout bar to have a strong body relative to recent volatility (`body_atr_ratio > 0.20`), ensuring institutional momentum is behind the move.

---

## Concept

```
Body ATR Ratio:
  body_atr_ratio = (Close - Open) / ATR(14)
```

By enforcing that this ratio is high, we avoid entering on "indecisive" bars that cross the range boundary but close poorly.

---

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 5-min chart |
| Opening Range | First 2 bars (09:00 - 09:10 range) |
| Active Window | 09:35 - 13:35 |

### Long Entry
- Price breaks above opening range high.
- `body_atr_ratio > 0.20`.
- Close > EMA(55).
- RSI(14) > 54.
- Enter Long.

### Short Entry
- Price breaks below opening range low.
- `body_atr_ratio < -0.20`.
- Close < EMA(55).
- RSI(14) < 46.
- Enter Short.

---

## Exit Rules

- **Stop Loss / Take Profit:** Placed using trade levels from `utils.py`.
- **Force Close:** At 14:25.

---
*Category: Volatility Breakout | Timeframe: Intraday (5-min) | Market: VN30F1M*
