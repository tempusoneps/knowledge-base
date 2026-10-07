# 41 — Morning Star / Evening Star Reversal

## Overview

The **Morning Star** and **Evening Star** are classic 3-candle reversal patterns. A Morning Star occurs at the bottom of a downtrend, signaling a bullish reversal. An Evening Star occurs at the top of an uptrend, signaling a bearish reversal. The defining feature is the middle "star" candle—a small body (often a Doji) that gapping away or showing severe hesitation—followed by a strong directional candle confirming the reversal.

---

## Concept

```
MORNING STAR (Bullish Reversal):
  Candle 1: Strong bearish (red) candle.
  Candle 2: Small body (doji or spinning top), ideally gapping down. Shows indecision.
  Candle 3: Strong bullish (green) candle that closes at least 50% into the body of Candle 1.

EVENING STAR (Bearish Reversal):
  Candle 1: Strong bullish (green) candle.
  Candle 2: Small body, ideally gapping up. Shows momentum stall.
  Candle 3: Strong bearish (red) candle closing at least 50% into Candle 1's body.
```

**Trade Logic:** The pattern visualizes a complete shift in market psychology from aggressive trend following, to doubt/hesitation, to aggressive counter-trend action.

---

## Indicators Required

| Indicator      | Setting                      | Purpose                                  |
| -------------- | ---------------------------- | ---------------------------------------- |
| Candlesticks   | Standard OHLC                | Pattern recognition                      |
| Volume         | 20-bar MA                    | Confirm the 3rd candle's conviction      |
| S/R Levels     | Manual / VWAP / Pivots       | Confluence for the pattern               |

---

## Setup & Entry Rules

| Parameter | Value                                          |
| --------- | ---------------------------------------------- |
| Timeframe | 15-min chart (more reliable than 5-min here)   |
| Markets   | VN30F, Liquid HSX Stocks                       |
| Context   | Must occur after a clear trend of at least 4-5 candles |

### Long Entry (Morning Star)
1. **Context:** Price is in a downtrend and approaching a key Support level or VWAP.
2. **Candle 1:** Closes as a strong down candle.
3. **Candle 2:** Forms a small body (Doji, Hammer, or Spinning Top) near support.
4. **Candle 3:** Closes as a strong up candle, pushing at least halfway up Candle 1.
5. **Confirmation:** Volume on Candle 3 is higher than Candle 2.
6. **Entry:** Go Long on the close of Candle 3.
7. **Stop Loss:** Below the lowest point of Candle 2 (the star).

### Short Entry (Evening Star)
1. **Context:** Price is in an uptrend approaching Resistance.
2. **Candle 1:** Strong up candle.
3. **Candle 2:** Small body (Doji, Shooting Star) near resistance.
4. **Candle 3:** Strong down candle pushing at least halfway down Candle 1.
5. **Entry:** Go Short on the close of Candle 3.
6. **Stop Loss:** Above the highest point of Candle 2.

---

## Exit Rules

- **Target 1:** Next intraday minor S/R level or moving average (EMA20). Take 50%.
- **Target 2:** The origin of the prior trend (full reversal). Take 50%.
- **Trailing Stop:** Move stop to break-even after T1. Trail behind successive 15-min candle highs/lows.
- **Failure:** If price reverses and closes past the midpoint of Candle 3, the momentum has failed -> Exit.

---

## Filters

- [ ] **Crucial:** The pattern MUST form at a preexisting Support, Resistance, or VWAP level. Patterns in the middle of nowhere are often noise.
- [ ] Skip if Candle 3's body is very small. It needs to show conviction.
- [ ] Avoid taking trades in the last hour of trading (after 13:45) as there isn't enough time for the reversal to play out.

---

## Risk Management

| Rule             | Guideline                          |
| ---------------- | ---------------------------------- |
| Max Risk/Trade   | 1% of account equity               |
| Stop Placement   | Beyond the extreme of the "Star"   |
| Min R:R          | 1:1.5                              |

---

## Edge & Statistics

- **Win rate:** 60-65% when combined with strict S/R or VWAP confluence on the 15-min timeframe.
- This is one of the most reliable candlestick patterns because it requires 3 periods (45 minutes) to build the narrative, reducing fake-outs.

---

## Example Trade Log

```
Date:      2026-06-11
Symbol:    VN30F2607
Context:   Downtrend from 09:30 to 10:30. Price hits S1 Pivot at 1,260.
Candle 1:  10:30 candle is strong red.
Candle 2:  10:45 candle is a Doji, holding exactly at 1,260 support.
Candle 3:  11:00 candle is strong green, engulfing Candle 1 completely.
Entry:     1,265 (Long, close of Candle 3)
Stop:      1,259 (Below Doji low)
Target:    1,275 (VWAP)
Result:    Price trends up steadily, hits target at 13:15. +WIN (+10 pts).
```

---

## Notes & Improvements
- Can be automated by scanning for the specific OHLC math (e.g., C3 > (O1+C1)/2).
- If Candle 3 entirely engulfs Candle 1, it is a stronger variation and warrants a slightly larger position size.

---
*Category: Price Action / Reversal | Timeframe: Intraday (15-min) | Market: VN30F / HSX Stocks*
