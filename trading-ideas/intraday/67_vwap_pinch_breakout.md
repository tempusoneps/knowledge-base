# 67 — The VWAP "Pinch" Breakout

## Overview

The **VWAP Pinch** is a volatility compression strategy. It occurs when price and a fast moving average (like the 9-EMA or 20-EMA) tightly squeeze against the daily VWAP line, creating a wedge or triangle structure on the intraday chart. As the moving average and VWAP converge (the "pinch"), volatility drops to near zero. When price finally breaks out of this pinch, the resulting momentum is usually explosive.

---

## Concept

```
The Setup:
  1. VWAP is flat or gently sloping (indicating a balanced market).
  2. The 20-EMA approaches VWAP from above or below.
  3. Price gets trapped exactly between the 20-EMA and VWAP.
  4. The distance between the 20-EMA and VWAP shrinks until they are almost touching.
  5. Price breaks out of this extremely tight wedge, initiating a new trend.
```

**Trade Logic:** You are trading pure volatility expansion. The pinch represents extreme indecision. Once a side wins, all the accumulated energy is released in that direction.

---

## Indicators Required

| Indicator      | Setting                      | Purpose                                  |
| -------------- | ---------------------------- | ---------------------------------------- |
| VWAP           | Daily                        | The primary baseline                     |
| EMA            | 20-period                    | The secondary compression boundary       |
| Volume         | 20-bar MA                    | Confirm the breakout direction           |

---

## Setup & Entry Rules

| Parameter | Value                                          |
| --------- | ---------------------------------------------- |
| Timeframe | 5-min chart                                    |
| Markets   | VN30F, Mid-cap / Large-cap HSX Stocks          |
| Context   | Best between 10:30 and 13:30 (Mid-day lull)    |

### Long Entry (Bullish Pinch Breakout)
1. **The Pinch:** The 5-min 20-EMA and the Daily VWAP converge until they are nearly identical in price.
2. **The Squeeze:** Price chops sideways for at least 4-6 candles (20-30 minutes) exactly at this convergence point. Volume dries up completely.
3. **The Trigger:** A 5-min candle breaks strongly **ABOVE** both the VWAP and the 20-EMA.
4. **Volume:** Volume spikes above average on the breakout candle.
5. **Entry:** Go Long on the close of the breakout candle.
6. **Stop Loss:** Just below the VWAP/EMA pinch point.

### Short Entry (Bearish Pinch Breakdown)
1. **The Pinch:** VWAP and 20-EMA converge. Price chops tightly.
2. **The Trigger:** A 5-min candle breaks strongly **BELOW** both the VWAP and 20-EMA.
3. **Volume:** Volume spikes.
4. **Entry:** Go Short on the close.
5. **Stop Loss:** Just above the pinch point.

---

## Exit Rules

- **Target 1:** The previous major intraday swing high/low (often established in the morning). Take 50%.
- **Target 2:** Ride the new trend. Trail the stop loss behind the 20-EMA.
- **Failure:** If price breaks out, but immediately reverses and closes back on the opposite side of the VWAP (a fake-out), exit immediately.

---

## Filters

- [ ] **Crucial:** The longer the pinch lasts, the better the setup. A pinch that lasts for 1 hour is much more explosive than one that lasts for 15 minutes.
- [ ] If the VWAP is steeply angled up or down, this is not a true pinch (that is a trend pullback). A true pinch happens when the VWAP is relatively flat, indicating true market equilibrium.
- [ ] Do not anticipate the breakout. Wait for the candle to close outside the pinch.

---

## Risk Management

| Rule             | Guideline                          |
| ---------------- | ---------------------------------- |
| Max Risk/Trade   | 1% of account equity               |
| Stop Placement   | Very tight (just opposite the breakout) |
| Min R:R          | 1:2.5 or higher                    |

---

## Edge & Statistics

- **Win rate:** 55-60%.
- **Edge:** The stop loss is incredibly small because the volatility is so compressed at the entry point. The resulting move is usually large, creating highly asymmetric trades.

---

## Example Trade Log

```
Date:      2026-06-10
Symbol:    VN30F2607
Context:   Morning was choppy. By 11:00, VWAP is flat at 1,270.
The Pinch: The 20-EMA drops to 1,270.5. Price chops between 1,269 and 1,271 for 45 minutes (11:00 to 11:45). Volume is dead.
Trigger:   At 13:00 (PM Open), price surges and closes at 1,274, breaking out of the pinch on heavy volume.
Entry:     1,274 (Long)
Stop:      1,269 (Below the VWAP pinch)
Target:    1,285 (Next daily resistance level)
Result:    Explosive trend afternoon. Hits target at 14:00. +WIN (+11 pts).
```

---

## Notes & Improvements
- This is a fantastic midday strategy. Markets often establish their range in the morning, pinch during lunch, and break out in the afternoon.

---
*Category: Volatility Expansion / Breakout | Timeframe: Intraday (5-min) | Market: VN30F / HSX Stocks*
