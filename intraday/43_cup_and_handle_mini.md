# 43 — Cup and Handle (Mini Intraday)

## Overview

The **Cup and Handle** is traditionally a long-term swing trading pattern, but it forms reliably on intraday charts (5-min, 15-min) as a continuation pattern. It represents a period of consolidation where weak holders are shaken out (the cup), followed by a tight, lower-volume drift (the handle) that shakes out the last remaining sellers before a breakout to the upside.

---

## Concept

```
The Cup:
  U-shaped consolidation.
  Left side: Initial high, then price pulls back.
  Bottom: Rounded bottom, showing accumulation (not a sharp 'V' shape).
  Right side: Price rallies back to test the initial high.

The Handle:
  Price drifts slightly lower from the right lip of the cup.
  Forms a tight channel or flag pattern.
  Volume dries up significantly.

Breakout:
  Price breaks above the Handle resistance (and the Cup lip) on high volume.
```

**Trade Logic:** The handle represents the ultimate volatility compression before the trend resumes. Buying the handle breakout provides a tight stop loss relative to the pattern's potential.

---

## Indicators Required

| Indicator      | Setting                      | Purpose                                  |
| -------------- | ---------------------------- | ---------------------------------------- |
| Trendlines     | Manual                       | Draw the handle resistance               |
| Volume         | 20-bar MA                    | Confirm the dry-up in handle and breakout|
| EMA            | 50-period                    | Ensure broader trend is UP               |

---

## Setup & Entry Rules

| Parameter | Value                                          |
| --------- | ---------------------------------------------- |
| Timeframe | 5-min or 15-min chart                          |
| Markets   | VN30F, Liquid HSX Stocks                       |
| Context   | Best during morning or mid-day consolidation   |

### Long Entry (Bullish Breakout)
1. **Context:** Stock is in an intraday uptrend.
2. **The Cup:** Price forms a U-shape, returning to a recent session high. (Takes 1-3 hours to form).
3. **The Handle:** Price drifts lower in a tight range (should not retrace more than 1/3 of the cup's depth). Volume MUST dry up here.
4. **Trigger:** A 5-min candle closes **above the handle's upper trendline**.
5. **Confirmation:** Volume spikes above average on the breakout.
6. **Entry:** Go Long on the breakout candle close.
7. **Stop Loss:** Below the lowest point of the handle.

*(Note: Inverted Cup and Handle exists for Short setups, but the bullish variant is significantly more reliable intraday).*

---

## Exit Rules

- **Target 1:** The depth of the cup added to the breakout point. Take 70%.
- **Target 2:** Ride remaining 30% with a trailing stop (EMA20).
- **Time Stop:** Close by 14:15.
- **Failure:** If price breaks below the handle's low instead of breaking out, the pattern is invalid -> Do not trade. If in trade and it fake-outs, exit immediately.

---

## Filters

- [ ] **Crucial:** The bottom of the cup must be rounded, not a sharp V. A V-shape indicates extreme volatility, not accumulation.
- [ ] The handle MUST show lower volume than the cup formation.
- [ ] The handle should be in the upper half of the cup. If the handle drifts all the way to the bottom, it's a failed pattern.

---

## Risk Management

| Rule             | Guideline                          |
| ---------------- | ---------------------------------- |
| Max Risk/Trade   | 1% of account equity               |
| Stop Placement   | Below the handle                   |
| Min R:R          | 1:2                                |

---

## Edge & Statistics

- **Win rate:** ~60% when the volume dry-up in the handle is distinct.
- **Edge:** The stop loss (handle depth) is usually very small compared to the cup depth (target), offering great asymmetry.

---

## Example Trade Log

```
Date:      2026-06-08
Symbol:    MWG (HSX)
Cup:       Forms from 09:30 to 11:00. High at 62,000, Low at 61,000. Depth = 1,000.
Handle:    Drifts down to 61,700 between 11:00 and 11:30. Volume is dead.
Breakout:  13:00 (PM open) pushes through 62,000 handle resistance.
Entry:     62,100 (Long, confirmed close)
Stop:      61,650 (Below handle low)
Target:    63,100 (Breakout + 1,000 cup depth)
Result:    Price rallies strongly in PM session. Hits target at 14:00. +WIN (+1,000 pts).
```

---

## Notes & Improvements
- Scanning for this manually is difficult. Look for stocks that hit a high early in the morning, sold off, and are now approaching HOD again around lunchtime.

---
*Category: Pattern Breakout | Timeframe: Intraday (5-min/15-min) | Market: VN30F / HSX Stocks*
