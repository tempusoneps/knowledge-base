# 38 — Accumulation/Distribution Divergence Breakout

## Overview

The **Accumulation/Distribution (A/D) Line** is a volume-based indicator designed to measure the cumulative flow of money into and out of a security. It weighs the close price relative to the high-low range and multiplies it by volume. When price is moving sideways or slightly down, but the A/D line is rising sharply, it indicates **hidden institutional accumulation** (smart money buying quietly). When price breaks out of this consolidation, the resulting move is usually sustained and powerful.

---

## Concept

```
A/D Formula:
  Money Flow Multiplier (MFM) = [(Close - Low) - (High - Close)] / (High - Low)
  Money Flow Volume (MFV) = MFM * Volume
  A/D Line = Previous A/D + MFV

Divergence Signal:
  Price: Flat or slightly descending (Consolidation)
  A/D Line: Steadily rising (Higher highs and higher lows)
  Meaning: Volume is heavy on up-closes and light on down-closes. Institutions are absorbing supply.
```

**Trade Logic:** Wait for the hidden accumulation to build, then buy the moment price breaks out of the consolidation pattern, confirming the institutional intent.

---

## Indicators Required

| Indicator      | Setting                      | Purpose                                  |
| -------------- | ---------------------------- | ---------------------------------------- |
| Accumulation/Distribution (A/D) | Standard | Track cumulative money flow              |
| Moving Average | 20-period on A/D Line (Opt)| Make trend of A/D easier to see          |
| Price Action   | Consolidations (Flags/Boxes)| Define the breakout level                |

---

## Setup & Entry Rules

| Parameter | Value                                          |
| --------- | ---------------------------------------------- |
| Timeframe | 15-min or 5-min chart                          |
| Markets   | Liquid HSX stocks (institutions hide here)     |
| Duration  | Consolidation must last at least 2 hours       |

### Long Entry (Accumulation Divergence Breakout)
1. **Price Context:** Stock is in a multi-hour consolidation (sideways range or slight pullback).
2. **A/D Divergence:** While price is flat/down, the A/D line is making clear **higher highs and higher lows**.
3. **Trigger:** Price breaks above the resistance of the consolidation pattern.
4. **Volume:** Breakout candle should have above-average volume.
5. **Entry:** Go Long on the close of the breakout candle.
6. **Stop Loss:** Below the most recent swing low within the consolidation.

### Short Entry (Distribution Divergence Breakdown)
1. **Price Context:** Stock is consolidating sideways or slightly drifting up.
2. **A/D Divergence:** The A/D line is steadily falling (lower highs, lower lows), indicating hidden distribution.
3. **Trigger:** Price breaks below the support of the consolidation.
4. **Entry:** Go Short on breakdown close.
5. **Stop Loss:** Above the recent swing high in the consolidation.

---

## Exit Rules

- **Target 1:** Next major daily S/R level. Take 50%.
- **Target 2:** Ride the trend. As long as A/D line keeps making new highs alongside price, hold the remaining 50%.
- **Trailing Stop:** Trail below the 20-EMA on the 5-min chart.
- **Failure Exit:** If price breaks out but A/D immediately plummets, exit the trade (false breakout).

---

## Filters

- [ ] Divergence must be visually obvious (clear slope on A/D line vs flat price).
- [ ] This strategy works poorly on illiquid stocks where a single trade skews the A/D line. Focus on top 50 volume stocks.
- [ ] Wait for the price breakout. **Never front-run the divergence**; accumulation can last for hours or days before the breakout happens.

---

## Risk Management

| Rule             | Guideline                          |
| ---------------- | ---------------------------------- |
| Max Risk/Trade   | 1% of account equity               |
| Stop Placement   | Below consolidation structure      |
| Min R:R          | 1:2                                |
| Max Trades/Day   | 1-2 (takes patience to find)       |

---

## Edge & Statistics

- **Win rate:** ~60% when divergence is clear over a 2+ hour period.
- **Strength:** Excellent for catching "stealth" moves before the rest of the retail market notices the volume footprint.

---

## Example Trade Log

```
Date:      2026-06-05
Symbol:    SSI (HSX)
Context:   SSI trades flat between 36,000 and 36,300 from 09:30 to 13:30.
A/D Line:  Rises consistently throughout this 4-hour period (clear accumulation).
Breakout:  At 13:45, price breaks above 36,300, closing at 36,450.
Entry:     36,450 (Long)
Stop:      36,100 (Below recent consolidation low)
Target:    Ride momentum into the close.
Result:    Price closes near HOD at 37,200. +WIN (+750).
```

---

## Notes & Improvements
- This is a fantastic filter for standard chart patterns (Flags, Triangles). A bull flag with a rising A/D line has a much higher win rate than one with a flat A/D line.
- Can be applied on 1H or Daily charts for swing trading.

---
*Category: Volume / Divergence | Timeframe: Intraday (15-min) | Market: HSX Stocks*
