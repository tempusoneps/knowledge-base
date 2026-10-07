# 57 — The Moving Average "Rubber Band" (Mean Reversion)

## Overview

Moving averages act like a rubber band attached to price. During strong momentum spikes (caused by panic, euphoria, or sudden news), price can stretch very far away from its moving average. However, it cannot stay disconnected forever; it must eventually snap back to its mean. The **Rubber Band** strategy aims to fade extreme intraday extensions when price is unsustainably far from a key moving average.

---

## Concept

```
The Mechanics:
  1. Calculate a dynamic "envelope" or percentage deviation from a moving average (e.g., the 20-period EMA).
  2. When price extends beyond a statistically rare threshold (e.g., > 1.5% away from the EMA on a 5-min chart).
  3. Wait for price action to stall and show signs of exhaustion.
  4. Fade the move, targeting a reversion back to the EMA.
```

**Trade Logic:** Extreme momentum often represents the capitulation of the final participants. By waiting for the exhaustion print, you are betting against the unsustainable velocity of the move.

---

## Indicators Required

| Indicator      | Setting                      | Purpose                                  |
| -------------- | ---------------------------- | ---------------------------------------- |
| EMA            | 20-period                    | The "Mean" target                        |
| Envelopes/Bands| 1.5% or 2% deviation from EMA| Define the "Extreme" stretch             |
| RSI            | 14-period                    | Confirm overbought/oversold (>80 / <20)  |

---

## Setup & Entry Rules

| Parameter | Value                                          |
| --------- | ---------------------------------------------- |
| Timeframe | 5-min chart                                    |
| Markets   | VN30F, Highly liquid HSX Stocks                |
| Threshold | Price > 1.5% away from 20-EMA (adjust based on stock volatility) |

### Short Entry (Fade Extreme Rally)
1. **The Stretch:** Price rallies vertically, pulling far away from the 20-EMA.
2. **The Extreme:** The closing price of a 5-min candle is > 1.5% (or 2.0%) above the 20-EMA.
3. **Confirmation:** RSI is > 80 (Extreme Overbought).
4. **Trigger:** A bearish reversal candle (Doji, Shooting Star, or Red Engulfing) forms.
5. **Entry:** Go Short on the close of the reversal candle.
6. **Stop Loss:** 1 ATR above the high of the climax candle.

### Long Entry (Fade Extreme Drop)
1. **The Stretch:** Price collapses vertically.
2. **The Extreme:** Closing price > 1.5% below the 20-EMA.
3. **Confirmation:** RSI is < 20 (Extreme Oversold).
4. **Trigger:** Bullish reversal candle forms.
5. **Entry:** Go Long on the close.
6. **Stop Loss:** 1 ATR below the low of the climax candle.

---

## Exit Rules

- **Target 1:** Halfway back to the 20-EMA. Take 50%.
- **Target 2:** The 20-EMA itself. Take remaining 50%.
- **Failure:** If price consolidates sideways at the extreme instead of reverting, the EMA will catch up to the price over time. This ruins the setup -> Exit at break-even or a small loss.
- **Time Stop:** The rubber band should snap back relatively quickly (within 30-45 minutes). If it doesn't, exit.

---

## Filters

- [ ] **Crucial:** NEVER fade a move just because it "looks high" or "looks low." You must wait for the mathematical stretch (e.g., >1.5%) AND the reversal candlestick.
- [ ] Do not trade this during the first 15 minutes of the open (ATO), as gaps naturally stretch the bands before true trading begins.
- [ ] If a major macro news event just dropped, avoid this strategy. The "mean" is being fundamentally repriced.

---

## Risk Management

| Rule             | Guideline                          |
| ---------------- | ---------------------------------- |
| Max Risk/Trade   | 0.5% - 0.75% of account equity (Counter-trend is risky) |
| Stop Placement   | Strict stop beyond climax extreme  |
| Min R:R          | 1:1.5                              |

---

## Edge & Statistics

- **Win rate:** 50-60%.
- **Edge:** Parabolic moves are inherently unsustainable. By using strict mathematical deviation thresholds, you filter out normal trend behavior and only trade genuine capitulation.

---

## Example Trade Log

```
Date:      2026-06-11
Symbol:    HPG (HSX)
Context:   HPG drops aggressively from 28,000.
The Stretch: At 10:45, HPG hits 27,200. The 20-EMA is currently at 27,700. Price is 1.8% away from the EMA.
Confirmation: RSI hits 18.
Trigger:   10:50 candle forms a massive hammer with high volume.
Entry:     27,250 (Long)
Stop:      27,150 (Below the hammer wick)
Target:    27,650 (Near the 20-EMA)
Result:    Violent short-covering bounce. Hits target at 11:20. +WIN (+400 pts).
```

---

## Notes & Improvements
- This works very well on VN30F during panic sell-offs. Calculate the average 20-EMA deviation for the last 30 days of VN30F to find the perfect statistical threshold (e.g., maybe VN30F rarely extends > 12 points away from its 5-min 20-EMA).

---
*Category: Mean Reversion / Counter-Trend | Timeframe: Intraday (5-min) | Market: VN30F / HSX Stocks*
