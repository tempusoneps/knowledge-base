# 37 — Low Volume Node (LVN) Breakout

## Overview

In Volume Profile analysis, a **Low Volume Node (LVN)** is a price level where very little trading volume has historically occurred. LVNs act like a vacuum or "slippery ice" — because there are few historical positions defended at these levels, price tends to move through them rapidly with high momentum once it enters the zone. This strategy aims to catch the fast momentum breakout as price crosses an LVN threshold.

---

## Concept

```
Volume Profile:
  HVN = Peak (Sticky, high friction)
  LVN = Valley (Slippery, low friction)

Behavior:
  LVNs often represent rejection zones from the past.
  When price breaks through the boundary into an LVN, there is very little liquidity to stop it.
  Price accelerates rapidly until it reaches the next HVN.
```

**Trade Logic:** Enter the trade just as price breaks into the LVN, expecting a fast, low-resistance move to the other side of the valley.

---

## Indicators Required

| Indicator      | Setting                      | Purpose                                  |
| -------------- | ---------------------------- | ---------------------------------------- |
| Volume Profile | Session or Multi-Day         | Identify clear LVN valleys               |
| Volume         | 20-bar MA                    | Confirm breakout momentum into LVN       |

---

## Setup & Entry Rules

| Parameter | Value                                          |
| --------- | ---------------------------------------------- |
| Timeframe | 5-min chart                                    |
| Markets   | VN30F, High-Beta HSX stocks                    |
| Profile   | Composite profile (last 3-5 days) preferred    |

### Long Entry (Breakout into LVN)
1. **Identify LVN:** Locate a deep valley (LVN) immediately above current price.
2. **Context:** Price is consolidating just below the LVN zone.
3. **Trigger:** A 5-min candle closes firmly inside the LVN zone.
4. **Confirmation:** Volume expands on the breakout candle (showing intent to push through the vacuum).
5. **Entry:** Go Long on the breakout candle close.
6. **Stop Loss:** Below the consolidation just before the LVN entry.

### Short Entry (Breakdown into LVN)
1. **Identify LVN:** Locate a clear LVN immediately below current price.
2. **Context:** Price consolidating just above the LVN.
3. **Trigger:** Candle closes inside the LVN zone downwards.
4. **Confirmation:** Volume expands.
5. **Entry:** Go Short on close.
6. **Stop Loss:** Above the pre-breakdown consolidation.

---

## Exit Rules

- **Target:** The next major HVN (High Volume Node) on the other side of the LVN valley. (Close 80-100% of position).
- **Time Stop:** Because LVN moves should be fast, if the trade stagnates inside the LVN for > 4 candles (20 mins), exit.
- **Failure:** Price reverses immediately and closes back outside the LVN -> Exit.

---

## Filters

- [ ] The LVN must be a distinct, deep valley in the profile. Shallow dips don't provide the "vacuum" effect.
- [ ] Ensure the distance across the LVN to the next HVN is large enough to justify the R:R (minimum 0.5% move).
- [ ] Skip if volume on the breakout candle is weak; entering a vacuum requires initial thrust.

---

## Risk Management

| Rule             | Guideline                          |
| ---------------- | ---------------------------------- |
| Max Risk/Trade   | 1% of account equity               |
| Stop Placement   | Just outside the LVN entry barrier |
| Min R:R          | 1:2                                |
| Max Trades/Day   | 2-3                                |

---

## Edge & Statistics

- **Win rate:** 55-60%.
- **Velocity:** The primary edge here is speed. Winning trades hit their targets very quickly, freeing up capital and reducing exposure time.

---

## Example Trade Log

```
Date:      2026-06-03
Symbol:    VN30F2607
Context:   Large LVN identified between 1,255 and 1,265. Next HVN is at 1,267.
Action:    Price consolidates at 1,253 for 30 minutes.
Breakout:  10:15 candle breaks above 1,255 and closes at 1,256 with strong volume.
Entry:     1,256 (Long)
Stop:      1,252 (Below consolidation)
Target:    1,265 (Edge of next HVN)
Result:    Price slides quickly through the LVN. Hits target at 10:40. +WIN (+9 pts).
```

---

## Notes & Improvements
- This is an excellent setup for Options traders (if trading US markets) or aggressive futures sizing, because the speed of the move works in your favor against time decay.
- If price gaps over the LVN at the open, do NOT fade it. Gaps over LVNs are standard behavior (market skipping areas of low interest).

---
*Category: Volume Profile / Momentum | Timeframe: Intraday | Market: VN30F / HSX Stocks*
