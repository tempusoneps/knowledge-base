# 51 — The 15-Minute Range Breakout (15m ORB)

## Overview

While the standard Opening Range Breakout (ORB) often focuses on the first 5 minutes, the **15-Minute ORB** is a more stable, conservative variation. The first 15 minutes (09:15 - 09:30 on HOSE, following the ATO) typically absorb the overnight news, retail market orders, and initial institutional positioning. Once this 15-minute range is established, a breakout from it usually sets the genuine trend for the morning session.

---

## Concept

```
The 15-Minute Range:
  High = Highest price between 09:15 and 09:30.
  Low = Lowest price between 09:15 and 09:30.

The Logic:
  The first 5 minutes can be pure noise (the "dumb money" open).
  By waiting 15 minutes, you allow the institutional algorithms to establish a fairer value range.
  A breakout of this 15-minute box requires sustained capital commitment, making false breakouts less likely than the 5-min ORB.
```

---

## Indicators Required

| Indicator      | Setting                      | Purpose                                  |
| -------------- | ---------------------------- | ---------------------------------------- |
| Price Range    | 09:15 to 09:30 High/Low      | Define the breakout box                  |
| Volume         | 20-bar MA                    | Confirm breakout momentum                |
| VWAP           | Daily                        | Ensure trade aligns with daily bias      |

---

## Setup & Entry Rules

| Parameter | Value                                          |
| --------- | ---------------------------------------------- |
| Timeframe | 5-min chart (using first 3 candles to set range) |
| Markets   | VN30F, Major VN30 Constituents                 |
| Context   | Best on days following a tight daily consolidation|

### Long Entry
1. **Define the Box:** Identify the High and Low of the first 15 minutes (09:15 - 09:30).
2. **Context:** Price is trading near the top of the box, and VWAP is sloping upward.
3. **Trigger:** A 5-min candle (e.g., the 09:35 or 09:40 candle) closes **above** the 15-minute High.
4. **Volume:** Volume on the breakout candle must be higher than the previous 5-min candle.
5. **Entry:** Go Long on the close of the breakout candle.
6. **Stop Loss:** Below the midpoint of the 15-minute range (or below VWAP if it's closer).

### Short Entry
1. **Define the Box:** High and Low of 09:15 - 09:30.
2. **Context:** Price is near the bottom of the box, VWAP sloping downward.
3. **Trigger:** A 5-min candle closes **below** the 15-minute Low.
4. **Entry:** Go Short on the close.
5. **Stop Loss:** Above the midpoint of the 15-minute range.

---

## Exit Rules

- **Target 1:** Distance equal to the height of the 15-minute range. Take 50%.
- **Target 2:** 2x the height of the range, or next major daily S/R level. Take 50%.
- **Trailing Stop:** Move to break-even after T1. Trail below 9-EMA for the runner.
- **Time Stop:** Close by 11:30 (Lunch break). Morning trends usually pause or reverse here.

---

## Filters

- [ ] **Crucial:** If the 15-minute range is massively wide (e.g., > 1.5% of the stock price), DO NOT trade the breakout. The move for the day has likely already happened, and the R:R will be terrible.
- [ ] If the breakout happens on very low volume, it is likely a trap. Skip.
- [ ] Ideally, take Longs only if the stock is green on the day, and Shorts only if red.

---

## Risk Management

| Rule             | Guideline                          |
| ---------------- | ---------------------------------- |
| Max Risk/Trade   | 1% of account equity               |
| Stop Placement   | Midpoint of the 15-min range       |
| Min R:R          | 1:1.5                              |

---

## Edge & Statistics

- **Win rate:** 55-60%.
- **Edge:** Fewer false signals compared to the 1-min or 5-min ORB. The trade is less stressful and more structured.

---

## Example Trade Log

```
Date:      2026-06-02
Symbol:    HPG (HSX)
Range:     09:15-09:30 High is 28,500. Low is 28,200. (Range = 300 pts).
Context:   Stock consolidates near 28,450.
Breakout:  09:40 candle closes at 28,550 with strong volume.
Entry:     28,550 (Long)
Stop:      28,350 (Midpoint of the range)
Target:    28,850 (1x Range = +300 pts)
Result:    Steady grind up. Hits target at 10:25. +WIN.
```

---

## Notes & Improvements
- Some institutional algorithms specifically use the 30-minute range (09:15 - 09:45). If the 15-min range fails often for a specific stock, widen the observation window to 30 minutes.

---
*Category: Momentum Breakout | Timeframe: Intraday (15-min context, 5-min execution) | Market: VN30F / HSX Stocks*
