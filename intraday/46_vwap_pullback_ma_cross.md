# 46 — VWAP Pullback + Moving Average Cross

## Overview

The **VWAP Pullback + MA Cross** is a robust trend-continuation strategy that combines the institutional relevance of the Volume Weighted Average Price (VWAP) with the short-term momentum signal of a fast moving average crossover. It aims to enter an established trend during a pullback, precisely when short-term momentum realigns with the broader intraday trend.

---

## Concept

```
VWAP: Acts as the intraday baseline (the "fair value" for institutions).
Fast MA (e.g., 9 EMA): Tracks short-term price momentum.
Slow MA (e.g., 20 EMA): Tracks intermediate momentum.

The Logic:
  1. Price is trending strongly (above VWAP for longs).
  2. Price pulls back toward VWAP. During this pullback, the 9 EMA crosses BELOW the 20 EMA.
  3. Price holds at or slightly above VWAP (Support).
  4. The 9 EMA crosses back ABOVE the 20 EMA -> This is the trigger that the pullback is over and the primary trend is resuming.
```

**Trade Logic:** You are buying a dip, but waiting for mathematical confirmation (the MA cross) that the dip has ended, rather than trying to catch a falling knife at VWAP.

---

## Indicators Required

| Indicator      | Setting                      | Purpose                                  |
| -------------- | ---------------------------- | ---------------------------------------- |
| VWAP           | Daily                        | Primary support/resistance and trend filter|
| Fast EMA       | 9-period                     | Short-term momentum trigger              |
| Slow EMA       | 20-period                    | Intermediate trend reference             |
| Volume         | 20-bar MA                    | Confirm the cross with volume            |

---

## Setup & Entry Rules

| Parameter | Value                                          |
| --------- | ---------------------------------------------- |
| Timeframe | 5-min chart                                    |
| Markets   | VN30F, High-liquidity VN30 Stocks              |
| Context   | Best on clear trend days                       |

### Long Entry (Bullish Pullback)
1. **Trend Filter:** Price must be above the daily VWAP.
2. **The Pullback:** Price pulls back towards VWAP. During this move, the 9 EMA crosses below the 20 EMA.
3. **The Support:** Price must hold at or above VWAP (it can wick slightly below, but must close above).
4. **The Trigger:** The 9 EMA crosses back **ABOVE** the 20 EMA.
5. **Entry:** Go Long on the close of the candle that completes the bullish MA cross.
6. **Stop Loss:** Below the lowest point of the pullback (usually just below VWAP).

### Short Entry (Bearish Pullback)
1. **Trend Filter:** Price is below daily VWAP.
2. **The Pullback:** Price rallies toward VWAP. 9 EMA crosses above 20 EMA.
3. **The Resistance:** Price rejects at or below VWAP.
4. **The Trigger:** 9 EMA crosses back **BELOW** the 20 EMA.
5. **Entry:** Go Short on the crossover candle close.
6. **Stop Loss:** Above the highest point of the rally (usually just above VWAP).

---

## Exit Rules

- **Target 1:** The previous High of Day (HOD) or Low of Day (LOD). Take 50%.
- **Target 2:** Ride the trend. Trail the stop loss behind the 20 EMA.
- **Failure:** If price breaks and closes below VWAP (for a Long) after entry, the intraday trend has likely changed -> Exit.

---

## Filters

- [ ] Ensure the pullback is orderly. If the pullback to VWAP consists of massive, high-volume red candles, it might be a trend reversal, not a pullback.
- [ ] Skip the trade if the MA crossover happens too far away from VWAP (e.g., halfway back to the HOD). The edge comes from entering near VWAP.
- [ ] Avoid taking this setup in the first 45 minutes of trading (VWAP and MAs need time to establish).

---

## Risk Management

| Rule             | Guideline                          |
| ---------------- | ---------------------------------- |
| Max Risk/Trade   | 1% of account equity               |
| Stop Placement   | Below the pullback swing low       |
| Min R:R          | 1:2                                |

---

## Edge & Statistics

- **Win rate:** 55-65% on trend days.
- **Edge:** Extremely mechanical. It removes the emotion of "guessing" when a pullback is over by requiring a strict indicator crossover.

---

## Example Trade Log

```
Date:      2026-06-09
Symbol:    VPB (HSX)
Context:   Strong morning trend. Price hits 22,000, VWAP is at 21,500.
Pullback:  10:30 to 11:15, price drifts down to 21,550. 9 EMA crosses below 20 EMA.
Support:   Price holds 21,550 (just above VWAP).
Trigger:   At 11:30, strong green candle pushes price up. 9 EMA crosses ABOVE 20 EMA.
Entry:     21,650 (Long)
Stop:      21,500 (Below the pullback low and VWAP)
Target:    22,000 (Previous HOD)
Result:    Trend resumes. Hits target at 13:45. +WIN (+350 pts).
```

---

## Notes & Improvements
- This is a classic "bread and butter" day trading setup.
- You can optimize the moving average lengths (e.g., 8/21 or 10/20) depending on the specific volatility of the asset you trade.

---
*Category: Trend Continuation | Timeframe: Intraday (5-min) | Market: VN30F / HSX Stocks*
