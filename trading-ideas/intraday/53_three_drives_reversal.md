# 53 — The "Three Drives" Reversal

## Overview

The **Three Drives** pattern is a harmonic reversal pattern consisting of three distinct, consecutive pushes (or "drives") in the direction of the trend, separated by two pullbacks. It visually represents the exhaustion of a trend. The third drive is usually the final capitulation or climax, trapping late retail traders before the institutional money aggressively reverses the market. 

---

## Concept

```
Structure (Bullish Reversal / Buying a Bottom):
  Drive 1: Price drops to a new low.
  Pullback 1: Minor bounce.
  Drive 2: Price drops to a lower low.
  Pullback 2: Minor bounce.
  Drive 3: Price drops to a final lower low, often accompanied by RSI divergence.
  Reversal: Aggressive move UP.

Structure (Bearish Reversal / Shorting a Top):
  Drive 1: Push up.
  Pullback 1.
  Drive 2: Higher high.
  Pullback 2.
  Drive 3: Final higher high (often a throw-over or climax).
  Reversal: Aggressive move DOWN.
```

**Trade Logic:** Trends rarely end quietly on the first or second push. The third drive exhausts the last remaining capital of the trend-followers, making it the highest probability point for a major reversal.

---

## Indicators Required

| Indicator      | Setting                      | Purpose                                  |
| -------------- | ---------------------------- | ---------------------------------------- |
| Price Action   | Counting the pushes          | Identify the structure                   |
| RSI            | 14-period                    | Confirm divergence on Drive 3            |
| Volume         | 20-bar MA                    | Look for climax volume on Drive 3        |

---

## Setup & Entry Rules

| Parameter | Value                                          |
| --------- | ---------------------------------------------- |
| Timeframe | 5-min or 15-min chart                          |
| Markets   | VN30F, High Beta HSX Stocks                    |
| Context   | Best after a sustained intraday or multi-day trend |

### Short Entry (Fade the Top)
1. **Identify the Pattern:** Count the drives. You need to see three distinct pushes upward, separated by clear (but shallow) pullbacks.
2. **Drive 3 Characteristics:** The third push makes a new High of Day (HOD).
3. **The Divergence:** RSI makes a *lower high* on Drive 3 compared to Drive 2.
4. **Trigger:** A bearish reversal candle (engulfing, shooting star) forms at the peak of Drive 3.
5. **Confirmation (Optional but safer):** Wait for price to break below the low of Pullback 2.
6. **Entry:** Go Short on the reversal candle close (aggressive) OR on the break of Pullback 2 (conservative).
7. **Stop Loss:** Just above the high of Drive 3.

### Long Entry (Fade the Bottom)
1. **Identify Pattern:** Three distinct pushes downward.
2. **Drive 3:** Makes a new Low of Day (LOD).
3. **Divergence:** RSI makes a *higher low* on Drive 3.
4. **Trigger:** Bullish reversal candle at the LOD.
5. **Entry:** Go Long on reversal close.
6. **Stop Loss:** Below the low of Drive 3.

---

## Exit Rules

- **Target 1:** The extreme of Pullback 1 (the start of the second drive). Take 50%.
- **Target 2:** The origin of the entire pattern (where Drive 1 started) or Daily VWAP. Take 50%.
- **Failure:** If price consolidates at the peak of Drive 3 instead of reversing, or breaks higher, exit immediately. The trend is not exhausted.

---

## Filters

- [ ] **Crucial:** The three drives should ideally be somewhat symmetrical in time and distance. If Drive 3 is a massive 5% vertical spike and the first two drives were tiny 0.5% bumps, it's not a true Three Drives pattern; it's a parabolic climax (use Pattern #40 instead).
- [ ] RSI divergence is practically mandatory for this pattern to be reliable.
- [ ] Do not trade this in the middle of a range. It must occur at the extremes of the day.

---

## Risk Management

| Rule             | Guideline                          |
| ---------------- | ---------------------------------- |
| Max Risk/Trade   | 0.75% of account equity            |
| Stop Placement   | Tightly beyond Drive 3 extreme     |
| Min R:R          | 1:2.5 (Reversals offer large targets) |

---

## Edge & Statistics

- **Win rate:** ~55%.
- **Edge:** It forces you to wait out the dangerous first and second reversal attempts (where most retail traders get chopped up), entering only when the probability of a true reversal is statistically highest.

---

## Example Trade Log

```
Date:      2026-06-19
Symbol:    VN30F2607
Context:   Uptrend all morning.
Drive 1:   Pushes to 1,270. Pulls back to 1,266.
Drive 2:   Pushes to 1,274. Pulls back to 1,271. (RSI at 75)
Drive 3:   Pushes to 1,277 at 11:15. (RSI at 65 -> Bearish Divergence).
Trigger:   Massive red engulfing candle off 1,277.
Entry:     1,275 (Short, aggressive entry on engulfing close)
Stop:      1,278 (Above Drive 3 peak)
Target:    1,266 (Extreme of Pullback 1)
Result:    Trend breaks. Price collapses to 1,265 by 13:30. +WIN (+9 pts).
```

---

## Notes & Improvements
- This is a simplified version of Elliott Wave Theory (where the Three Drives are Waves 1, 3, and 5). You don't need to be an Elliott Wave expert to trade this; just count the visible pushes.

---
*Category: Reversal / Price Action | Timeframe: Intraday (5-min) | Market: VN30F / HSX Stocks*
