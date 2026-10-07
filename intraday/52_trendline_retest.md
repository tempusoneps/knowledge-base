# 52 — Trendline Re-test (Kiss of Death / Life)

## Overview

When a major trendline or consolidation boundary is broken, price often experiences a rapid initial move, followed by a pullback to "re-test" the exact line it just broke. This phenomenon occurs because breakout traders take quick profits, and trapped traders use the pullback to exit at break-even. The **Trendline Re-test** strategy enters on this pullback, offering a highly precise, low-risk entry into the new trend.

---

## Concept

```
The Mechanics:
  1. Price breaks a confirmed downward trendline.
  2. Initial breakout creates a higher high.
  3. Price pulls back (often on lower volume) to touch the broken trendline from the TOP side.
  4. The old Resistance has now flipped to New Support (The Kiss of Life).
  
  Conversely for a short:
  Price breaks an upward trendline, drops, then rallies to touch the underside of the broken line.
  Old Support becomes New Resistance (The Kiss of Death).
```

**Trade Logic:** Breakouts can be messy and prone to false starts. The re-test confirms that the market psychology has truly shifted, as buyers step in where sellers used to dominate.

---

## Indicators Required

| Indicator      | Setting                      | Purpose                                  |
| -------------- | ---------------------------- | ---------------------------------------- |
| Trendlines     | Manual (Connecting 3+ touches)| Define the structural boundary           |
| Volume         | 20-bar MA                    | Confirm dry-up on the re-test            |
| Candlesticks   | 5-min or 15-min              | Reversal patterns at the re-test point   |

---

## Setup & Entry Rules

| Parameter | Value                                          |
| --------- | ---------------------------------------------- |
| Timeframe | 5-min or 15-min chart                          |
| Markets   | VN30F, Liquid HSX Stocks                       |
| Context   | Valid trendline must have 3+ prior touches     |

### Long Entry (Kiss of Life)
1. **The Breakout:** Price breaks above a well-defined descending trendline on high volume.
2. **The Wait:** Do not chase the breakout. Let the initial momentum cool off.
3. **The Re-test:** Price drifts back down to touch (or come very close to) the broken trendline. Volume should be *decreasing* on this pullback.
4. **The Trigger:** A bullish reversal candle (hammer, engulfing) forms right at the trendline.
5. **Entry:** Go Long on the close of the reversal candle.
6. **Stop Loss:** Just below the reversal candle's wick (below the trendline).

### Short Entry (Kiss of Death)
1. **The Breakdown:** Price breaks below an ascending trendline on high volume.
2. **The Wait:** Let the price rally back up to the underside of the broken line.
3. **The Re-test:** Volume decreases on the rally.
4. **The Trigger:** Bearish reversal candle (shooting star) at the line.
5. **Entry:** Go Short on the close.
6. **Stop Loss:** Just above the reversal candle's wick.

---

## Exit Rules

- **Target 1:** The swing high/low created by the initial breakout move. Take 50%.
- **Target 2:** Measure the height of the pattern prior to the breakout, project it from the re-test point. Take 50%.
- **Failure:** If price closes back *inside* the old trendline boundary, the breakout was false. Exit immediately.

---

## Filters

- [ ] **Crucial:** The trendline must be objectively clear to everyone. If you have to force the line to fit the candles, it's not a valid structural boundary.
- [ ] The re-test must happen relatively soon after the breakout (within 10-20 candles). If it takes all day to return to the line, it's not a re-test; it's a trend failure.
- [ ] Skip if the re-test happens on massive, expanding volume (indicates the breakout is failing).

---

## Risk Management

| Rule             | Guideline                          |
| ---------------- | ---------------------------------- |
| Max Risk/Trade   | 1% of account equity               |
| Stop Placement   | Extremely tight, just past the trendline |
| Min R:R          | 1:2.5 (Because the stop is so tight) |

---

## Edge & Statistics

- **Win rate:** ~60%.
- **Edge:** The R:R is usually exceptional. Buying the exact re-test allows for stop losses that are a fraction of the size required if you bought the initial breakout.

---

## Example Trade Log

```
Date:      2026-06-25
Symbol:    VN30F2607
Context:   Descending trendline connecting highs at 09:30, 10:15, and 10:45.
Breakout:  At 11:00, price breaks the trendline at 1,265 and pushes to 1,272.
Re-test:   At 11:30, price drifts slowly back to 1,266. Volume is very low.
Trigger:   A perfect hammer candle forms, touching 1,265 and closing at 1,267.
Entry:     1,267 (Long)
Stop:      1,264 (Below the hammer and the trendline)
Target:    1,272 (Target 1) -> Hit at 13:15.
Result:    +WIN (+5 pts).
```

---

## Notes & Improvements
- This works perfectly with horizontal Support/Resistance levels as well. A broken Resistance becomes Support.
- Combine with VWAP: If the broken trendline and the daily VWAP intersect at the exact same point during the re-test, it is an A+ setup.

---
*Category: Price Action / Pullback | Timeframe: Intraday (5-min/15-min) | Market: VN30F / HSX Stocks*
