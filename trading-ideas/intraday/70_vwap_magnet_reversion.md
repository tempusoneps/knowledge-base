# 70 — The VWAP "Magnet" Trade (Late Day Reversion)

## Overview

The Volume Weighted Average Price (VWAP) is the ultimate intraday mean. Institutions use it to benchmark their execution quality. If a stock is trading far away from the VWAP late in the day (after 13:30), but the momentum driving it there has clearly exhausted, institutions often use the remaining time in the session to push the price back toward the VWAP to "flatten" the day's average. The **VWAP Magnet** trade is a late-day mean reversion strategy.

---

## Concept

```
The Logic:
  By 13:30, most of the day's volume has been traded, and the VWAP line is highly stable.
  If price is severely overextended (very far from VWAP) and begins to chop or reverse, it acts like a rubber band that has lost its tension.
  The VWAP acts as a magnetic pull. Because there is no new news or momentum to keep pushing the price away, it naturally drifts back to fair value (VWAP) before the close.
```

**Trade Logic:** Fade late-day exhaustion when price is far from VWAP, targeting the VWAP line as the inevitable close.

---

## Indicators Required

| Indicator      | Setting                      | Purpose                                  |
| -------------- | ---------------------------- | ---------------------------------------- |
| VWAP           | Daily                        | The primary target                       |
| RSI            | 14-period on 5-min           | Confirm late-day exhaustion              |
| Candlesticks   | 5-min chart                  | Reversal triggers                        |

---

## Setup & Entry Rules

| Parameter | Value                                          |
| --------- | ---------------------------------------------- |
| Timeframe | 5-min chart                                    |
| Markets   | VN30F, High Liquidity HSX Stocks               |
| Context   | Must be after 13:30 (Afternoon session)        |

### Short Entry (Fade the Late-Day High)
1. **The Context:** It is 13:30 or later. Price is significantly *above* the daily VWAP (e.g., > 1% away on a stock, or > 10 points on VN30F).
2. **The Exhaustion:** Price stops making higher highs. RSI diverges (lower high) or drops below 70 from an overbought state.
3. **Trigger:** A bearish reversal pattern forms (Double Top on 5-min, or a massive Shooting Star) and price breaks below a local intraday support level (e.g., the 9-EMA).
4. **Entry:** Go Short on the breakdown.
5. **Stop Loss:** Just above the High of Day.

### Long Entry (Fade the Late-Day Low)
1. **Context:** After 13:30. Price is significantly *below* VWAP.
2. **The Exhaustion:** Price stops making lower lows. RSI shows bullish divergence.
3. **Trigger:** Bullish reversal pattern (Double Bottom, Hammer) and price breaks above local intraday resistance (e.g., 9-EMA).
4. **Entry:** Go Long on the breakout.
5. **Stop Loss:** Just below the Low of Day.

---

## Exit Rules

- **Target:** The Daily VWAP line. (Since it's late in the day, the VWAP line will be almost flat, making it a very static target). Take 80% to 100% here.
- **Time Stop:** Close the trade at 14:28, regardless of whether it hit VWAP. Do not carry late-day mean reversion trades into the ATC auction, as ATC flow can be highly unpredictable.
- **Failure:** If price reverses and breaks the High of Day (for a short) or Low of Day (for a long), the trend is actually resuming -> Exit immediately.

---

## Filters

- [ ] **Crucial:** Ensure the distance to the VWAP is large enough to justify the trade. If VWAP is only 3 points away on VN30F, the R:R is too poor to risk a trade. You want price to be "stranded" far away from VWAP.
- [ ] If the late-day move is driven by *brand new* breaking news that just dropped at 13:45, do NOT fade it. This strategy relies on the absence of new catalysts.

---

## Risk Management

| Rule             | Guideline                          |
| ---------------- | ---------------------------------- |
| Max Risk/Trade   | 0.75% of account equity            |
| Stop Placement   | Hard stop beyond the extreme of the day |
| Min R:R          | 1:2                                |

---

## Edge & Statistics

- **Win rate:** ~60% in range-bound or exhausting markets.
- **Edge:** Institutional algorithms are designed to execute near VWAP. When the market is quiet late in the day, these algos slowly guide the price back to the mean.

---

## Example Trade Log

```
Date:      2026-06-15
Symbol:    VN30F2607
Context:   VN30F rallied all morning, peaking at 1,290 at 13:15. VWAP is flat at 1,278 (12 points away).
The Exhaustion: From 13:15 to 13:40, price chops between 1,288 and 1,290. Fails to break 1,290. RSI drops from 75 to 60.
Trigger:   At 13:45, a 5-min candle breaks below the 9-EMA and the local support at 1,287.
Entry:     1,286.5 (Short)
Stop:      1,291 (Above HOD)
Target:    1,278 (VWAP)
Result:    Slow, steady bleed into the close. Hits VWAP at 14:20. +WIN (+8.5 pts).
```

---

## Notes & Improvements
- This is one of the most consistent ways to trade the last hour of the day. Retail traders often chase late-day breakouts, while professionals fade them back to VWAP.

---
*Category: Mean Reversion / Late-Day | Timeframe: Intraday (5-min), After 13:30 | Market: VN30F / HSX Stocks*
