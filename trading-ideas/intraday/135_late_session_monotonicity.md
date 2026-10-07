# 135 — Late-Session Monotonicity

## Overview

VN30F1M late-session trends (after 13:45) are highly persistent. This strategy uses a multi-layered momentum filter: session range position (Macro), Pearson correlation with time over 12 bars (Meso Monotonicity), and a 3-bar price burst (Micro) to trigger entries in the direction of the late-session drift.

---

## Concept

```
Meso Monotonicity:
  meso_corr = Pearson correlation coefficient between Close and a linear time sequence [0, 1, ..., 11]
```

A high absolute correlation ($|R| \ge 0.60$) indicates a smooth, monotonic trend rather than choppy price action.

---

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 5-min chart |
| Entry Times | 13:45, 13:50, 13:55, 14:00, 14:05, 14:10 |
| Limit | Maximum 1 trade per day |

### Long Entry
- Time matches late session window.
- Range position `range_pos >= 0.65`.
- Meso monotonicity `meso_corr >= 0.60`.
- Micro burst `micro_ret >= 0.03%` (3-bar return).
- Enter Long.

### Short Entry
- Time matches late session window.
- Range position `range_pos <= 0.35`.
- Meso monotonicity `meso_corr <= -0.60`.
- Micro burst `micro_ret <= -0.03%` (3-bar return).
- Enter Short.

---

## Exit Rules

- **Stop Loss:** standard level from `utils.py`.
- **Force Close:** At 14:25.

---
*Category: Intraday Momentum | Timeframe: Intraday (5-min) | Market: VN30F1M*
