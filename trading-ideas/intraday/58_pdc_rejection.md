# 58 — Previous Day Close (PDC) Rejection

## Overview

The **Previous Day Close (PDC)** is one of the most psychologically important levels on a chart. It dictates whether a stock is "Green" or "Red" on the day. Much of retail and institutional trading logic is tied to whether an asset is positive or negative on the session. When a stock gaps away from the PDC, attempts to fill the gap, but firmly rejects at the PDC line, it provides a high-conviction momentum trade in the direction of the rejection.

---

## Concept

```
The Scenario:
  1. Stock gaps UP at the open.
  2. It pulls back early in the morning, drifting toward yesterday's closing price (the PDC).
  3. The moment it hits the PDC, buyers step in aggressively to keep the stock "Green" on the day.
  4. The rejection at the PDC forms a powerful bounce.

Conversely for a Short:
  Stock gaps DOWN. Rallies to the PDC. Sellers step in to keep the stock "Red". Rejects hard.
```

**Trade Logic:** You are leveraging the psychological barrier of the "Flat Line" (0% change on the day). The market often defends this line vigorously.

---

## Indicators Required

| Indicator      | Setting                      | Purpose                                  |
| -------------- | ---------------------------- | ---------------------------------------- |
| Price Line     | Previous Day Close (PDC)     | The primary support/resistance level     |
| Candlesticks   | 5-min chart                  | Identify the rejection                   |
| Volume         | 20-bar MA                    | Confirm the rejection momentum           |

---

## Setup & Entry Rules

| Parameter | Value                                          |
| --------- | ---------------------------------------------- |
| Timeframe | 5-min chart                                    |
| Markets   | VN30F, High Liquidity HSX Stocks               |
| Context   | Best within the first 2 hours of trading       |

### Long Entry (PDC Support Bounce)
1. **Context:** Stock gaps UP at the open (>0.5%).
2. **The Test:** Price drifts downward toward the PDC line.
3. **The Rejection:** A 5-min candle touches or slightly pierces the PDC line, but reverses sharply and closes green (forming a Hammer or Pin Bar).
4. **Volume:** Volume on the rejection candle should be above average.
5. **Entry:** Go Long on the close of the rejection candle.
6. **Stop Loss:** Just below the low of the rejection wick (below the PDC).

### Short Entry (PDC Resistance Fade)
1. **Context:** Stock gaps DOWN at the open (< -0.5%).
2. **The Test:** Price rallies up to test the PDC line.
3. **The Rejection:** Candle touches the PDC and rejects hard, closing red (Shooting Star).
4. **Entry:** Go Short on the close.
5. **Stop Loss:** Just above the high of the rejection wick (above the PDC).

---

## Exit Rules

- **Target 1:** The High of Day (HOD) or Low of Day (LOD) established before the PDC test. Take 50%.
- **Target 2:** The next major intraday S/R level or Daily VWAP. Take remaining 50%.
- **Failure:** If price breaks and closes convincingly past the PDC (turning the stock from Green to Red, or vice versa), the psychology has flipped. Exit immediately.

---

## Filters

- [ ] **Crucial:** The PDC line must act as a clear barrier. If price chops back and forth across the PDC for 30 minutes, it is no longer being respected as a hard boundary. Do not trade it.
- [ ] This strategy relies on the gap being relatively small-to-moderate (0.5% to 1.5%). If the gap is massive (e.g., 5%), a pullback all the way to the PDC means the trend is already broken; don't buy the bounce.

---

## Risk Management

| Rule             | Guideline                          |
| ---------------- | ---------------------------------- |
| Max Risk/Trade   | 1% of account equity               |
| Stop Placement   | Extremely tight, just past the wick|
| Min R:R          | 1:2                                |

---

## Edge & Statistics

- **Win rate:** ~60%.
- **Edge:** The PDC is a universally watched level. It creates a self-fulfilling prophecy of liquidity, allowing for very tight stops and clear invalidation points.

---

## Example Trade Log

```
Date:      2026-06-18
Symbol:    VHM (HSX)
PDC:       42,500
Context:   VHM gaps up to 42,800 at ATO. Drops slowly over the next 45 minutes.
The Test:  At 10:00, VHM hits 42,500.
Rejection: A massive buying wick forms instantly. 5-min candle closes at 42,600 (Hammer).
Entry:     42,600 (Long)
Stop:      42,450 (Below the wick and the PDC)
Target:    43,000 (New HOD target based on morning momentum)
Result:    Price never looks back, pushing to 43,200 by 11:30. +WIN (+400 pts).
```

---

## Notes & Improvements
- Most charting platforms can automatically plot a line for "Yesterday's Close". Have this on your chart permanently.
- If the PDC aligns perfectly with today's VWAP during the re-test, it is an exceptionally high-probability trade.

---
*Category: Gap Fill / Mean Reversion | Timeframe: Intraday (5-min) | Market: VN30F / HSX Stocks*
