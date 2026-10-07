# 69 — The "Inside Bar" Consolidation Breakout (Multi-Timeframe)

## Overview

An **Inside Bar** occurs when a candlestick's High is lower than the previous candle's High, and its Low is higher than the previous candle's Low. It represents a pause, or consolidation, in the market. While a single 5-min Inside Bar can be noisy, when an Inside Bar forms on a higher timeframe (like the 1-Hour chart) during a strong trend, its breakout offers a powerful, high-probability continuation signal for intraday traders.

---

## Concept

```
The Mechanics:
  1. Mother Bar: A large, directional candle (e.g., a strong 1-Hour green candle).
  2. Inside Bar: The next candle is entirely contained within the high/low range of the Mother Bar.
  3. Meaning: The market is resting. Volatility is contracting.
  4. Breakout: Price breaks the High or Low of the Inside Bar, releasing the contracted volatility.
```

**Trade Logic:** You use the 1-Hour Inside Bar to locate the "coiled spring," and you use the 5-min chart to execute the breakout with a very tight stop loss.

---

## Indicators Required

| Indicator      | Setting                      | Purpose                                  |
| -------------- | ---------------------------- | ---------------------------------------- |
| Candlesticks   | 1-Hour chart                 | Identify the Mother Bar / Inside Bar     |
| Candlesticks   | 5-min chart                  | Execute the breakout                     |
| EMA            | 20-period on 1-Hour          | Confirm the macro trend direction        |

---

## Setup & Entry Rules

| Parameter | Value                                          |
| --------- | ---------------------------------------------- |
| Timeframe | 1-Hour for setup, 5-min for execution          |
| Markets   | VN30F, Major HSX Stocks                        |
| Context   | Must be trading in the direction of the 1H Trend|

### Long Entry (Bullish Inside Bar Breakout)
1. **The Setup (1-Hour Chart):** Price is above the 1H 20-EMA. A strong green 1-Hour candle (Mother Bar) is followed by a 1-Hour Inside Bar.
2. **Mark the Levels:** Draw a line at the High and Low of the *Inside Bar*.
3. **Execution (5-min Chart):** Drop down to the 5-min chart. Watch price interact with the High line of the Inside Bar.
4. **Trigger:** A 5-min candle closes **ABOVE** the High line of the Inside Bar.
5. **Entry:** Go Long on the close of the 5-min breakout candle.
6. **Stop Loss:** Below the Low of the Inside Bar (or below the most recent 5-min swing low if the Inside Bar is very large).

### Short Entry (Bearish Inside Bar Breakdown)
1. **The Setup (1H Chart):** Price below 1H 20-EMA. Red Mother Bar followed by Inside Bar.
2. **Mark Levels:** Draw lines at High/Low of Inside Bar.
3. **Trigger (5-min Chart):** 5-min candle closes **BELOW** the Low line.
4. **Entry:** Go Short on the close.
5. **Stop Loss:** Above the High of the Inside Bar.

---

## Exit Rules

- **Target 1:** Distance equal to the height of the Mother Bar, projected from the breakout point. Take 50%.
- **Target 2:** Next major S/R level on the 1-Hour chart. Take remaining 50%.
- **Trailing Stop:** Trail behind the 20-EMA on the 5-min chart.
- **Failure:** If the 5-min breakout candle immediately reverses and closes back inside the range, exit the trade.

---

## Filters

- [ ] **Crucial:** Only trade breakouts in the direction of the macro trend (e.g., if 1H trend is UP, only buy breakouts of the Inside Bar High; ignore breakdowns).
- [ ] If the Inside Bar is extremely small (e.g., a tiny Doji), the breakout is highly reliable. If the Inside Bar is huge (almost the same size as the Mother Bar), the signal is weak and the stop loss will be too wide. Skip it.

---

## Risk Management

| Rule             | Guideline                          |
| ---------------- | ---------------------------------- |
| Max Risk/Trade   | 1% of account equity               |
| Stop Placement   | Dependent on Inside Bar size       |
| Min R:R          | 1:2                                |

---

## Edge & Statistics

- **Win rate:** 60-65% when aligned with the 1-Hour trend.
- **Edge:** Multitimeframe alignment. You are finding macro consolidation (1H) and entering with micro risk (5m).

---

## Example Trade Log

```
Date:      2026-06-22
Symbol:    VN30F2607
Context:   1H trend is strongly UP. 
Setup:     09:00 - 10:00 candle is a massive green Mother Bar. 10:00 - 11:00 candle is an Inside Bar (High = 1,280, Low = 1,275).
Execution: Drop to 5-min chart. At 11:15, a 5-min candle breaks and closes at 1,281 (above the Inside Bar High).
Entry:     1,281 (Long)
Stop:      1,275 (Below the Inside Bar Low, 6 pt risk)
Target:    1,293 (Mother Bar was 12 pts. 1,281 + 12 = 1,293)
Result:    Trend resumes strongly in the afternoon. Hits target at 14:00. +WIN (+12 pts).
```

---

## Notes & Improvements
- Consecutive Inside Bars (e.g., an Inside Bar *inside* another Inside Bar) indicates massive, coiled volatility. Breakouts from these are exceptionally explosive.

---
*Category: Volatility Expansion / MTF | Timeframe: 1-Hour / 5-min | Market: VN30F / HSX Stocks*
