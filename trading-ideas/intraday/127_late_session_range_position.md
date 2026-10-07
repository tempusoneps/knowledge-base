# 127 — Late-Session Asymmetric Momentum

## Overview

VN30 futures exhibit a strong bullish bias; upward breakouts at session highs have a significantly higher success rate than downward breakouts at session lows. To capture this structure, this strategy uses an **asymmetric entry design**: Longs are triggered by high running range position, while Shorts require a persistence score showing sustained selling below the session open.

---

## Concept

```
Long Condition:
  Price is in the top 21% of the daily running range (range_pos > 0.79)
  AND ADX > 17 with DI+ > DI-
  AND Linear regression slope is positive

Short Condition:
  Price has spent more than 42% of the last 12 bars below session open (persist_short > 0.42)
  AND ADX > 17 with DI- > DI+
  AND Linear regression slope is negative
```

---

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 5-min chart |
| Markets | VN30F1M |
| Entry Times | 13:10, 13:25, 13:40, 13:55 |

### Long Entry
- Time matches entry window.
- Range position `close_vs_range > 0.79`.
- RSI(5) > 62.
- Day body change `body_pct > 0.12%`.
- ADX(14) > 17 with DI+ > DI-.
- Linear regression slope (8 bars) > 0.
- Enter Long.

### Short Entry
- Time matches entry window.
- Persistence score `persist_short > 0.42`.
- RSI(5) < 38.
- Day body change `body_pct < -0.12%`.
- ADX(14) > 17 with DI- > DI+.
- Linear regression slope (8 bars) < 0.
- Enter Short.

---

## Exit Rules

- **Stop Loss:** Based on levels from `utils.py`.
- **Force Close:** At 14:25.

---
*Category: Asymmetric Momentum | Timeframe: Intraday (5-min) | Market: VN30F1M*
