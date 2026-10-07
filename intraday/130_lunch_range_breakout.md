# 130 — Lunch Range Breakout

## Overview

The midday period (11:00 - 12:55) represents the lunch break and surrounding consolidation in the Vietnamese market. The range established during this period acts as a key balance area. A breakout of this range after the 13:00 PM session open, confirmed by momentum and positive slope, signals a strong late-day trend.

---

## Concept

```
Lunch Range:
  lunch_high = Max(High, 11:00 - 12:55)
  lunch_low  = Min(Low, 11:00 - 12:55)
```

We enter on a clean breakout of this midday range after 13:00.

---

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 5-min chart |
| Midday Period | 11:00 - 12:55 |
| Entry Window | 13:00 - 14:25 |

### Long Entry
- Time matches entry window.
- `Close >= lunch_high`.
- `bar_close_pos >= 0.60` (closes in the upper 40% of its range).
- RSI(8) $\ge 55$.
- Linear regression slope (5 bars) > 0.
- Daily change from open `body_from_open >= 0.0%`.
- Enter Long.

---

## Exit Rules

- **Stop Loss:** Standard levels from `utils.py`.
- **Force Close:** At 14:25.

---
*Category: Range Breakout | Timeframe: Intraday (5-min) | Market: VN30F1M*
