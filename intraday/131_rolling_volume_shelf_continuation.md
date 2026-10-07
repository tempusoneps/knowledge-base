# 131 — Rolling Volume Shelf Continuation

## Overview

Instead of breakout of daily session boundaries, this strategy trades late-session continuation relative to a local rolling **Volume-Weighted Price Shelf (Volume Shelf)**. By comparing the price to the volume shelf and its standard deviation (shelf_z), it identifies high-conviction momentum shifts.

---

## Concept

```
Volume Shelf:
  volume_shelf = Sum(Close * Volume, 12) / Sum(Volume, 12)
  shelf_z      = (Close - volume_shelf) / rolling_shelf_std
```

This acts as a dynamic volume-weighted support/resistance line.

---

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 5-min chart |
| Lookback (Shelf) | 12 bars |
| Entry Times | 13:00, 13:20, 13:40, 14:00, 14:20 |

### Long Entry
- Time matches entry window.
- `shelf_z >= 0.0`.
- RSI(8) $\ge 56$.
- Day body change `body_pct >= 0.15%`.
- Day range `range_pct >= 0.10%`.
- Bar close position `bar_close_pos >= 0.45`.
- Slope (5 bars) $\ge 0$.
- Enter Long.

---

## Exit Rules

- **Stop Loss:** Placed using trade levels from `utils.py`.
- **Force Close:** At 14:25.

---
*Category: Volumetric / Momentum | Timeframe: Intraday (5-min) | Market: VN30F1M*
