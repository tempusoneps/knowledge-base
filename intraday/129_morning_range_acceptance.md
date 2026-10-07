# 129 — Morning Range Acceptance

## Overview

Avoids false breakouts by checking if price "accepts" the upper half of the morning range before entering a late-session breakout. The morning range (09:00 - 11:00) is used as a baseline, and the afternoon session must show sustained trading above the mid-point of this range.

---

## Concept

```
Acceptance Metric:
  accept_long = rolling mean of (Close > morning_mid) over last 4 bars
```

If price spends significant time above the midpoint of the morning range during the afternoon session, it shows acceptance of higher prices, paving the way for a breakout.

---

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 5-min chart |
| Morning Session | 09:00 - 11:00 |
| Entry Window | 13:00 - 14:25 |

### Long Entry
- Time matches afternoon window.
- `accept_long >= 0.42` (at least 42% of recent bars are above the morning midpoint).
- `breakout_long >= 0.0` (Price is at or above the morning range high).
- `bar_close_pos >= 0.55` (closes in the upper half of its bar).
- RSI(8) $\ge 54$.
- Linear regression slope (5 bars) > 0.
- Enter Long.

---

## Exit Rules

- **Stop Loss:** Based on levels from `utils.py`.
- **Force Close:** At 14:25.

---
*Category: Range Acceptance | Timeframe: Intraday (5-min) | Market: VN30F1M*
