# 134 — Adaptive Historical Edge

## Overview

A statistical pattern-matching strategy that records outcomes of trades matching the current time-of-day and session range position (split into 5 bins). Today's entry is permitted only if the historical win rate of trades in that specific bin/time bucket combination is $> 75\%$ based on at least 30 observations, adapting to structural intraday probabilities.

---

## Concept

We define a group key: `(side, time_bucket, range_pos_bin)`.
For each historical bar:
1. Determine if a trade entered at this bar would have hit target ($+0.2\%$) before stop loss (daily stop rate).
2. Calculate the rolling historical win rate of this key prior to the current day.
3. If `Win Rate >= 75%` and `Count >= 30` and `Average PnL > 0`, today's entry is triggered.

---

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 5-min chart |
| Range Position Bins | 5 equal bins between 0 and 1 |
| Max Entries/Day | 6 trades |

### Long/Short Entry
- Historical win rate for the current `(side, time_code, pos_bin)` $\ge 75\%$ with $\ge 30$ observations.
- Enter Long or Short.
- **Scalp vs Run:**
  - If `range_pos <= 0.125` (near the day's low for longs), enter in **Run Mode** (uses both SL and TP from `utils.py`).
  - Otherwise, enter in **Scalp Mode** (uses SL but exits immediately when price reaches $+0.20\%$ profit target).

---

## Exit Rules

- **Stop Loss:** Based on standard levels from `utils.py`.
- **Take Profit (Run Mode):** Standard take profit from `utils.py`.
- **Take Profit (Scalp Mode):** Exit on next bar if price hits $+0.20\%$ return since entry.
- **Force Close:** At 14:25.

---
*Category: Statistical Edge | Timeframe: Intraday (5-min) | Market: VN30F1M*
