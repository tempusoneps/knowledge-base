# 55 — The Opening Drive (Tick Divergence)

## Overview

The **Opening Drive** strategy focuses on the very first few minutes of the trading session (09:00 - 09:10). Instead of waiting for a range to form (like the ORB), this strategy attempts to catch the immediate institutional imbalance at the open. Because price action can be chaotic, it relies on a market internal indicator—specifically Market Breadth or Tick Data (Advance/Decline ratio)—to confirm the true direction of the opening drive and filter out fake gaps.

---

## Concept

```
The Logic:
  A stock gaps up. Is it retail excitement, or institutional buying?
  If the stock gaps up, but the overall Market Breadth (Advancing issues vs Declining issues on HOSE) is heavily negative, the gap is likely a fake-out (retail trap).
  If the stock gaps up, AND Market Breadth is heavily positive (e.g., 300 stocks up, 50 down), institutions are buying the whole market. The gap will likely "drive" higher.
```

**Trade Logic:** Trade the first 5 minutes of the open ONLY if the individual stock's direction perfectly aligns with extreme readings in broader market internals.

---

## Indicators Required

| Indicator      | Setting                      | Purpose                                  |
| -------------- | ---------------------------- | ---------------------------------------- |
| Market Breadth | Advancing vs Declining Stocks| Measure true market sentiment            |
| Price Action   | 1-min chart                  | Fast execution                           |
| VWAP           | Daily                        | Ensure we stay on the right side of flow |

---

## Setup & Entry Rules

| Parameter | Value                                          |
| --------- | ---------------------------------------------- |
| Timeframe | 1-min chart                                    |
| Markets   | High Beta VN30 Stocks                          |
| Context   | The first 10 minutes of the session (09:00 - 09:10)|

### Long Entry (Bullish Opening Drive)
1. **The Open:** Stock opens higher or pushes up immediately off the ATO.
2. **Internal Confirmation:** Check HOSE Market Breadth. It MUST be extremely positive (e.g., > 2.5x more advancing stocks than declining).
3. **The Trigger:** The first 1-min candle closes green. The second 1-min candle breaks the high of the first candle.
4. **Entry:** Go Long immediately as the high is broken.
5. **Stop Loss:** Below the low of the very first 1-min candle of the day.

### Short Entry (Bearish Opening Drive)
1. **The Open:** Stock opens lower or drops immediately.
2. **Internal Confirmation:** Market Breadth is extremely negative (> 2.5x more declining stocks than advancing).
3. **The Trigger:** First 1-min candle closes red. Second candle breaks the low.
4. **Entry:** Go Short.
5. **Stop Loss:** Above the high of the first 1-min candle.

---

## Exit Rules

- **Target 1:** 2x the risk (distance from entry to stop). Take 50%.
- **Trailing Stop:** This is a momentum play. If the 1-min candles stop making higher highs (for a long) and start printing red, exit the remainder immediately. Do not overstay.
- **Time Stop:** The "Drive" usually exhausts within the first 30 minutes. Be flat or holding a small runner by 09:30.

---

## Filters

- [ ] **Crucial:** If Market Breadth is neutral (e.g., 150 up, 140 down), **DO NOT TRADE THE OPENING DRIVE**. The market lacks a clear institutional consensus.
- [ ] Skip stocks that are heavily news-driven that day (they can move independently of market internals). We want stocks moving *because* the whole market is moving.
- [ ] You must have a fast execution platform. If you hesitate for 30 seconds on a 1-min breakout, you will ruin your R:R.

---

## Risk Management

| Rule             | Guideline                          |
| ---------------- | ---------------------------------- |
| Max Risk/Trade   | 0.5% - 0.75% (Fast, high-stress trade) |
| Stop Placement   | Hard stop at the extreme of the 1st minute |
| Min R:R          | 1:2                                |

---

## Edge & Statistics

- **Win rate:** ~50%.
- **Edge:** The wins are very fast and often very large because you are catching the absolute beginning of an institutional order execution cycle.

---

## Example Trade Log

```
Date:      2026-06-11
Symbol:    SSI (HSX)
Open:      09:00 ATO opens SSI flat at 34,000.
Internals: HOSE Breadth shows 310 Advancers, 45 Decliners (Massive bullish imbalance).
Trigger:   09:01 candle closes green at 34,100. 09:02 candle pushes to 34,150, breaking the high.
Entry:     34,150 (Long)
Stop:      33,950 (Below the 09:01 low)
Target:    Trail stop tightly on 1-min chart.
Result:    SSI drives vertically to 34,800 by 09:15 as the whole market surges. Trailed out at 34,600. +WIN.
```

---

## Notes & Improvements
- Most broker platforms in Vietnam (SSI, VNDirect, TCBS) provide a real-time Market Breadth pie chart. Keep this visible on your screen at the open.
- This strategy pairs well with T+0 trading to clear out overnight inventory on a strong opening drive.

---
*Category: Momentum / Market Internals | Timeframe: 1-min | Market: HSX Stocks*
