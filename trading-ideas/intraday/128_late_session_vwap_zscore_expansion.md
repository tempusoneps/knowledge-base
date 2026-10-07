# 128 — Late-Session VWAP Z-Score Expansion

## Overview

Quantifies distance from the volume-weighted average price (VWAP) in units of rolling daily standard deviation. During the late session, a Z-score expansion beyond threshold boundaries identifies strong momentum breakouts that are likely to continue into the close.

---

## Concept

```
VWAP Z-Score:
  vwap_z = (Close - VWAP) / VWAP_STD
```

Where standard deviation is calculated using accumulated volume-weighted variance from the start of the day.

---

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 5-min chart |
| Markets | VN30F1M |
| Entry Times | 13:25, 13:40, 13:55 |

### Long Entry
- Time matches entry window.
- `vwap_z >= 0.75`.
- RSI(8) $\ge 54$.
- Intraday return `body_pct >= 0.05%`.
- Session range `range_pct >= 0.12%`.
- Enter Long.

### Short Entry
- Time matches entry window.
- `vwap_z <= -1.00`.
- RSI(8) $\le 41$.
- Intraday return `body_pct <= -0.10%`.
- Session range `range_pct >= 0.18%`.
- Enter Short.

---

## Exit Rules

- **Stop Loss / Take Profit:** Standard levels from `utils.py`.
- **Force Close:** At 14:25.

---
*Category: VWAP / Momentum | Timeframe: Intraday (5-min) | Market: VN30F1M*
