# 124 — Late Session Flow Imbalance

## Overview

Tracks late-session institutional order flow imbalance approximated from 5-minute volume and price direction. It combines this flow imbalance metric with RSI(8) and VWAP deviation to enter late-session continuation trades during the final hour.

---

## Concept

We calculate intraday signed volume flow:
$$FlowImbalance = \frac{\sum (Volume \times \text{sgn}(\Delta Price))}{\sum Volume}$$

Where sum is accumulated from the session start.
During 13:25 – 13:55, a high flow imbalance confirms institutional direction.

---

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 5-min chart |
| Markets | VN30F1M |
| Entry Times | 13:25, 13:40, 13:55 |

### Long Entry
- Time is 13:25, 13:40, or 13:55.
- $FlowImbalance \ge 0$.
- RSI(8) $\ge 61.11$.
- VWAP deviation $\ge 0.14\%$.
- Body percentage from morning open $\ge 0.12\%$.
- Enter Long.

### Short Entry
- Time is 13:25, 13:40, or 13:55.
- $FlowImbalance \le 0$.
- RSI(8) $\le 42.0$.
- VWAP deviation $\le -0.05\%$.
- Body percentage from morning open $\le -0.10\%$.
- Enter Short.

---

## Exit Rules

- **Stop Loss / Take Profit:** Based on levels from `utils.py`.
- **Force Close:** At 14:25.

---
*Category: Volumetric / Momentum | Timeframe: Intraday (5-min) | Market: VN30F1M*
