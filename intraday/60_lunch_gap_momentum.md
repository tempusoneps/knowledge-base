# 60 — The "Lunch Gap" (Midday News Break)

## Overview

The Vietnamese stock market has a unique structural feature: a 90-minute lunch break (11:30 - 13:00). During this time, the market is closed, but news, rumors, and global macroeconomic events continue to occur. This often results in a "Lunch Gap"—where the market reopens at 13:00 significantly higher or lower than where it closed at 11:30. The **Lunch Gap** strategy is a momentum play that trades the immediate continuation of this gap, assuming it is driven by legitimate new information processed during the break.

---

## Concept

```
The Logic:
  11:30 Close: Market pauses.
  11:30 - 13:00: A major news piece drops (e.g., NHNN announces a rate cut, or a major geopolitical event occurs in Europe/US futures).
  13:00 Open: The market gaps aggressively in response.
  
  Unlike overnight gaps (which often fade), Lunch Gaps happen while traders are already at their desks, fully awake, and reacting in real-time. This creates immediate, sustained directional momentum.
```

**Trade Logic:** Do not fade a Lunch Gap driven by news. Trade the continuation of the gap (the "Gap and Go") as the rest of the market participants scramble to re-position their portfolios.

---

## Indicators Required

| Indicator      | Setting                      | Purpose                                  |
| -------------- | ---------------------------- | ---------------------------------------- |
| Gap Scanner    | PM Open vs AM Close          | Identify the anomaly                     |
| Volume         | 1-min chart                  | Confirm the urgency at 13:00             |
| News Feed      | Real-time (CafeF, Bloomberg) | Confirm the fundamental catalyst         |

---

## Setup & Entry Rules

| Parameter | Value                                          |
| --------- | ---------------------------------------------- |
| Timeframe | 1-min chart (for entry), 5-min (for context)   |
| Markets   | VN30F, Entire VN30 Basket                      |
| Context   | The 13:00 reopening bell                       |

### Long Entry (Lunch Gap Up Continuation)
1. **The Gap:** The market or stock opens at 13:00 gapping UP at least 0.5% from the 11:30 close.
2. **The Catalyst:** Verify there is an actual news catalyst (not just random fluctuation).
3. **The Trigger:** The first 1-min candle (13:00 - 13:01) closes green, showing buyers are stepping in to support the gap.
4. **Entry:** Go Long on the break of the first 1-min candle's high.
5. **Stop Loss:** Below the low of the 13:00 opening candle.

### Short Entry (Lunch Gap Down Continuation)
1. **The Gap:** Market opens at 13:00 gapping DOWN > 0.5% from 11:30 close.
2. **The Catalyst:** Negative news confirmed during the break.
3. **The Trigger:** First 1-min candle closes red.
4. **Entry:** Go Short on the break of the first 1-min candle's low.
5. **Stop Loss:** Above the high of the 13:00 opening candle.

---

## Exit Rules

- **Target 1:** 2x the risk (stop loss distance). Take 50%.
- **Target 2:** The next major daily S/R level. Take remaining 50%.
- **Trailing Stop:** Trail behind the 9-EMA on the 1-min chart. This momentum is fast and can reverse sharply once the initial panic/euphoria subsides.
- **Failure:** If price immediately fills the Lunch Gap (returning to the 11:30 close) within the first 5 minutes, the news was a nothingburger -> Exit.

---

## Filters

- [ ] **Crucial:** If there is NO fundamental news to explain the Lunch Gap, treat it as a random anomaly and consider fading it instead (using Pattern #27 - Lunchtime Reversal).
- [ ] You must act quickly. The best moves on Lunch Gaps happen between 13:00 and 13:15.
- [ ] If the gap is massive (e.g., > 2%), the move might already be overextended. Wait for a pullback to the 13:00 open price to enter safely.

---

## Risk Management

| Rule             | Guideline                          |
| ---------------- | ---------------------------------- |
| Max Risk/Trade   | 0.75% of account equity            |
| Stop Placement   | Extremely tight (1-min candle extreme) |
| Min R:R          | 1:2                                |

---

## Edge & Statistics

- **Win rate:** ~60% when supported by a legitimate, market-wide news catalyst.
- **Edge:** Exploiting the bottleneck of information processing. Retail traders take 10-15 minutes to read and react to the news; algorithms and prop desks react instantly at 13:00. You are riding the algorithm's coattails.

---

## Example Trade Log

```
Date:      2026-06-23
Symbol:    VN30F2607
Context:   11:30 close at 1,270. During lunch, State Bank announces surprise liquidity injection.
The Gap:   13:00 opens at 1,276 (Gap up of 6 points).
Trigger:   13:01 candle is a massive green bar closing at 1,278. 13:02 breaks the high.
Entry:     1,278.5 (Long)
Stop:      1,276 (Below the 13:00 open price)
Target:    1,285 (Next daily resistance level)
Result:    Market surges on the news. Hits target at 13:20. +WIN (+6.5 pts).
```

---

## Notes & Improvements
- Keep a news terminal (or Twitter/X lists of Vietnamese financial news) open during the 11:30 - 13:00 break. Being prepared with the knowledge of *why* the market might gap gives you the conviction to execute instantly at 13:00.

---
*Category: Event Driven / Momentum | Timeframe: 1-min | Market: VN30F / VN30 Stocks*
