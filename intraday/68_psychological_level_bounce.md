# 68 — The Half-Dollar / Whole-Dollar Psychological Level Bounce

## Overview

Human psychology dictates that traders and institutions naturally gravitate toward round, whole numbers (e.g., 20,000, 50,000, 100,000 VND). These are called "Psychological Levels." Because many traders place their limit orders and stop losses exactly at or just beyond these whole numbers, these levels act as massive magnets for price, and subsequent barriers. The **Psychological Level Bounce** strategy fades price as it touches a major whole number for the first time.

---

## Concept

```
The Magnet Effect:
  If a stock is trading at 49,200 and trending up, it will almost inevitably be drawn to 50,000.
  
The Barrier Effect:
  Once it hits 50,000, massive sell limit orders (take profits) sitting exactly at 50,000 are triggered.
  The price rejects and bounces off the whole number.
```

**Trade Logic:** You are front-running the massive liquidity pools sitting at clean, round numbers.

---

## Indicators Required

| Indicator      | Setting                      | Purpose                                  |
| -------------- | ---------------------------- | ---------------------------------------- |
| Price Action   | Visual                       | Identify major round numbers             |
| Candlesticks   | 1-min or 5-min chart         | Trigger the entry                        |
| Volume         | 20-bar MA                    | Confirm the rejection                    |

---

## Setup & Entry Rules

| Parameter | Value                                          |
| --------- | ---------------------------------------------- |
| Timeframe | 1-min for entry, 5-min for context             |
| Markets   | HSX Stocks (Particularly Mid-caps)             |
| Target    | Major round numbers (e.g., ending in 0,000 or 5,000 VND) |

### Short Entry (Resistance at Whole Number)
1. **The Approach:** Stock rallies aggressively toward a major whole number (e.g., 50,000 VND).
2. **The Touch:** Price touches or slightly pierces the whole number (e.g., hits 50,100).
3. **The Rejection:** Sell orders flood the tape. A 1-min or 5-min candle forms a long upper wick, closing back below the whole number.
4. **Entry:** Go Short on the close of the rejection candle.
5. **Stop Loss:** Just above the high of the rejection wick (e.g., 50,200).

### Long Entry (Support at Whole Number)
1. **The Approach:** Stock drops aggressively toward a major whole number (e.g., 20,000 VND).
2. **The Touch:** Price hits or slightly pierces 20,000.
3. **The Rejection:** Buy orders absorb the selling. A lower wick forms, closing back above the whole number.
4. **Entry:** Go Long on the close of the rejection candle.
5. **Stop Loss:** Just below the low of the rejection wick (e.g., 19,850).

---

## Exit Rules

- **Target 1:** The nearest minor S/R level or moving average (9-EMA). Take 50%.
- **Target 2:** The origin of the aggressive move that led to the touch. Take 50%.
- **Time Stop:** Intraday scalps; do not hold if the bounce doesn't happen immediately.
- **Failure:** If price cleanly breaks the whole number on massive volume and *holds* above it for more than 2 candles, the barrier has broken. Exit immediately.

---

## Filters

- [ ] **Crucial:** Only trade the *FIRST* touch of the psychological level. If a stock hits 50,000, bounces, and comes back 20 minutes later to hit 50,000 again, the sell orders have already been absorbed. The second or third touch will likely break through.
- [ ] Major milestones (like a stock hitting 100,000 VND for the first time) are the strongest barriers.
- [ ] This strategy works best on stocks moving quickly (parabolically) into the level, creating exhaustion.

---

## Risk Management

| Rule             | Guideline                          |
| ---------------- | ---------------------------------- |
| Max Risk/Trade   | 0.5% - 0.75% of account equity (Fast scalp) |
| Stop Placement   | Tightly beyond the wick extreme    |
| Min R:R          | 1:1.5                              |

---

## Edge & Statistics

- **Win rate:** ~60% on first touches of major numbers (ending in 0,000).
- **Edge:** Exploiting the predictable, hard-coded behavior of human psychology and legacy institutional limit order placement.

---

## Example Trade Log

```
Date:      2026-06-16
Symbol:    SSI (HSX)
Context:   SSI rallies from 38,500 in the morning.
The Approach: At 10:45, momentum accelerates as it approaches the major 40,000 level.
The Rejection: Hits 40,050 at 10:50. Instantly, massive sell volume hits. The 5-min candle closes at 39,800, leaving a huge upper wick.
Entry:     39,800 (Short)
Stop:      40,100 (Above the wick)
Target:    39,200 (VWAP)
Result:    Price fades off the psychological resistance. Hits target at 11:25. +WIN (+600 pts).
```

---

## Notes & Improvements
- When a stock breaks *through* a major psychological level (e.g., breaks 50,000 and closes at 50,500), that level immediately flips to massive Support. You can trade the re-test of 50,000 as a Long setup (Idea #52).

---
*Category: Scalping / Market Psychology | Timeframe: 1-min / 5-min | Market: HSX Stocks*
