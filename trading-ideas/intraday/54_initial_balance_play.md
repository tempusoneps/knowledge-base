# 54 — Initial Balance (IB) Breakout / Fade

## Overview

In Market Profile terminology, the **Initial Balance (IB)** is defined as the price range established during the first hour of trading (09:00 - 10:00 on HOSE). This hour represents the market's initial attempt to find fair value. How price reacts to the boundaries of the IB (IB High and IB Low) dictates the strategy for the rest of the day. A breakout suggests a trend day, while a fade suggests a range-bound day.

---

## Concept

```
Initial Balance (IB):
  IB High = Highest price from 09:00 to 10:00.
  IB Low = Lowest price from 09:00 to 10:00.

Scenarios:
  1. IB Breakout: Price breaks IB High/Low and holds -> Signals a Trend Day. Go with the breakout.
  2. IB Fade: Price pokes outside IB High/Low, rejects, and falls back inside -> Signals a Range Day. Fade the edges.
```

**Trade Logic:** The first hour establishes the playing field. Trading the edges of the IB aligns you with the daily structural bias.

---

## Indicators Required

| Indicator      | Setting                      | Purpose                                  |
| -------------- | ---------------------------- | ---------------------------------------- |
| Price Lines    | Manual (09:00-10:00 H/L)     | Define the IB boundaries                 |
| Volume         | 20-bar MA                    | Differentiate between Breakout and Fade  |
| VWAP           | Daily                        | Reference for Range Day targets          |

---

## Setup & Entry Rules

| Parameter | Value                                          |
| --------- | ---------------------------------------------- |
| Timeframe | 5-min or 15-min chart                          |
| Markets   | VN30F, VN30 Constituents                       |
| Context   | Wait until exactly 10:00 to draw the lines     |

### Setup 1: IB Breakout (Trend Day Play)
1. **Define IB:** Draw lines at IB High and IB Low at 10:00.
2. **The Break:** Price pushes outside the IB High (for Long) or IB Low (for Short) after 10:00.
3. **Volume:** The breakout candle has high volume.
4. **Trigger:** A 5-min candle closes completely outside the IB boundary.
5. **Entry:** Enter in the direction of the breakout on the close, or on the first micro-pullback.
6. **Stop Loss:** Just inside the IB boundary (if it falls back in, the breakout failed).

### Setup 2: IB Fade (Range Day Play)
1. **Define IB:** Draw IB High and Low.
2. **The Test:** Price pushes outside the IB High (e.g., at 10:30).
3. **The Rejection:** Volume is light on the push, and a reversal candle forms immediately. Price closes back *inside* the IB.
4. **Trigger:** The close back inside the IB confirms the false breakout.
5. **Entry:** Go Short (fading the IB High) or Go Long (fading the IB Low).
6. **Stop Loss:** Just outside the extreme of the fake breakout wick.

---

## Exit Rules

- **Target (Breakout):** 1x the width of the IB projected outward. Trail with 9-EMA for the rest.
- **Target (Fade):** VWAP (Take 50%), then the opposite side of the IB (Take remaining 50%).
- **Time Stop:** Close by 14:15.

---

## Filters

- [ ] **Width of IB:** If the IB is extremely wide (e.g., > 1.5% of the index), expect a Range Day. Fades work better.
- [ ] If the IB is very narrow, expect a Trend Day. Breakouts work better.
- [ ] Do not trade *inside* the middle of the IB. Only trade at the edges (High/Low).

---

## Risk Management

| Rule             | Guideline                          |
| ---------------- | ---------------------------------- |
| Max Risk/Trade   | 1% of account equity               |
| Stop Placement   | Dependent on setup (Tight on Fades, looser on Breakouts) |
| Min R:R          | 1:2                                |

---

## Edge & Statistics

- **Win rate:** 55-60%.
- **Edge:** By waiting a full hour, you let the market reveal its daily character (Trend vs. Range) before committing capital, heavily reducing the chance of getting chopped up in morning volatility.

---

## Example Trade Log

```
Date:      2026-06-05
Symbol:    VN30F2607
IB Definition: At 10:00, IB High is 1,280, IB Low is 1,270. (Width = 10 pts, average).
Context:   At 10:45, price rallies to 1,282 (breaking IB High).
Rejection: Volume is low. 10:50 candle is a massive red engulfing, closing at 1,278 (back inside IB).
Entry:     1,278 (Short, IB Fade setup)
Stop:      1,283 (Above the fake breakout peak)
Target:    1,274 (VWAP) -> 1,270 (IB Low)
Result:    Price drifts back through the range. Hits VWAP at 11:30 (+4 pts), hits IB Low at 13:45 (+8 pts). +WIN.
```

---

## Notes & Improvements
- This concept is derived from Market Profile theory (J. Peter Steidlmayer). Understanding the statistical probability of the IB breaking based on its initial width is the key to mastering this setup.

---
*Category: Market Profile / Structure | Timeframe: Intraday (First Hour Context) | Market: VN30F*
