# 63 — The "Fake Breakout" Fade (Turtle Soup)

## Overview

Popularized by Linda Raschke as the "Turtle Soup" pattern, this strategy is designed to fade false breakouts of 20-period highs or lows. Retail traders and trend-followers (like the famous "Turtles") love to buy breakouts of new highs. Institutions know this, and often push the price just past the high to trigger buy orders (providing liquidity), before instantly reversing the market. The **Fake Breakout Fade** capitalizes on this trap.

---

## Concept

```
The Setup:
  1. Market makes a significant 20-period High (or Low).
  2. Price pulls back for a few periods.
  3. Price rallies again and breaks the previous 20-period High.
  4. Breakout traders buy aggressively.
  5. Instead of trending, the price immediately stalls and reverses back below the previous High line.
  6. Breakout buyers are trapped and must sell to cut losses, accelerating the reversal.
```

**Trade Logic:** False breakouts are often more powerful than real breakouts because they involve the forced liquidation of trapped positions.

---

## Indicators Required

| Indicator      | Setting                      | Purpose                                  |
| -------------- | ---------------------------- | ---------------------------------------- |
| Donchian Channel| 20-period (Optional)        | Easily identify the 20-period High/Low   |
| Horizontal Line| Manual                       | Mark the exact breakout level            |
| Candlesticks   | 5-min or 15-min              | Confirm the rejection back into the range|

---

## Setup & Entry Rules

| Parameter | Value                                          |
| --------- | ---------------------------------------------- |
| Timeframe | 15-min chart (best for filtering noise)        |
| Markets   | VN30F, Major HSX Stocks                        |
| Context   | The previous High/Low must have been made at least 4 periods ago |

### Short Entry (Fade the False High)
1. **Identify the Level:** Mark a clear 20-period High on the 15-min chart.
2. **The Breakout:** Price rallies and breaks above this High.
3. **The Trap:** The breakout must fail quickly (within 1 to 3 candles). Price reverses and closes back *below* the breakout line.
4. **Trigger:** The close of the 15-min candle back below the previous High line.
5. **Entry:** Go Short on the close.
6. **Stop Loss:** Just above the absolute high of the false breakout wick.

### Long Entry (Fade the False Low)
1. **Identify the Level:** Mark a clear 20-period Low.
2. **The Breakdown:** Price breaks below this Low.
3. **The Trap:** Fails quickly, closing back *above* the Low line.
4. **Trigger:** Close of the candle back inside the range.
5. **Entry:** Go Long on the close.
6. **Stop Loss:** Just below the absolute low of the false breakdown wick.

---

## Exit Rules

- **Target 1:** The midpoint of the 20-period range. Take 50%.
- **Target 2:** The opposite side of the 20-period range (e.g., if you faded the High, target the 20-period Low). Take 50%.
- **Time Stop:** Intraday setups should hit their targets within 2-3 hours. If chopping, exit.

---

## Filters

- [ ] **Crucial:** The initial 20-period High/Low must be a distinct, obvious peak/valley. Do not trade this in a tight, sideways chop.
- [ ] The reversal back inside the range must happen *fast*. If price stays above the breakout level for 5+ candles, it has established acceptance. Do not fade it.
- [ ] Works best in range-bound or mildly trending markets. In a roaring bull market, do not fade new highs.

---

## Risk Management

| Rule             | Guideline                          |
| ---------------- | ---------------------------------- |
| Max Risk/Trade   | 1% of account equity               |
| Stop Placement   | Tightly beyond the fake breakout wick |
| Min R:R          | 1:2.5                              |

---

## Edge & Statistics

- **Win rate:** ~60% in range-bound markets.
- **Edge:** "From false moves come fast moves." The stop loss is extremely tight (just the tip of the fake-out), while the target spans the entire recent range.

---

## Example Trade Log

```
Date:      2026-06-09
Symbol:    VN30F2607
Context:   15-min chart. At 09:45, VN30F sets a High at 1,280. Pulls back to 1,270.
The Break: At 13:15, price rallies and breaks 1,280, hitting 1,282.
The Trap:  The very next 15-min candle (13:30) is a massive red bar, closing at 1,278 (back below the 1,280 level).
Entry:     1,278 (Short)
Stop:      1,283 (Above the 1,282 fake peak)
Target:    1,270 (The bottom of the recent range)
Result:    Trapped longs liquidate. Hits target at 14:15. +WIN (+8 pts).
```

---

## Notes & Improvements
- This is the direct opposite of the Donchian Channel Breakout (Idea #33). You can build an automated system that plays the breakout, but if stopped out quickly as price returns to the range, instantly reverses into the Turtle Soup setup.

---
*Category: Mean Reversion / Trap | Timeframe: Intraday (15-min) | Market: VN30F / HSX Stocks*
