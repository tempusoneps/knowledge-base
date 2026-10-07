# 45 — HOD Second Test Breakout (False Double Top)

## Overview

A common trap for retail traders is shorting the exact High of Day (HOD) when price returns to test it for the second time, anticipating a Double Top. While Double Tops are valid, in a strong trending market, the second test of the HOD is often a consolidation phase that absorbs selling pressure before a massive breakout. This strategy looks for signs of absorption at the HOD to go Long, trapping the early short sellers.

---

## Concept

```
The Setup:
  1. Price sets a strong High of Day (HOD) in the morning.
  2. Price pulls back, but makes a Higher Low (bullish structure).
  3. Price rallies back to test the HOD for the second time.
  4. Retail shorts pile in, expecting a Double Top.
  5. Instead of rejecting sharply, price consolidates TIGHTLY just below the HOD.
  6. Breakout -> Shorts are trapped and forced to cover, fueling a momentum spike.
```

**Trade Logic:** Tight consolidation just under major resistance is bullish. It means buyers are willing to hold their ground at high prices, absorbing all selling pressure.

---

## Indicators Required

| Indicator      | Setting                      | Purpose                                  |
| -------------- | ---------------------------- | ---------------------------------------- |
| Price Action   | HOD line                     | Define the resistance level              |
| Volume         | 20-bar MA                    | Confirm the breakout                     |
| EMA            | 20-period                    | Ensure higher lows are being made        |

---

## Setup & Entry Rules

| Parameter | Value                                          |
| --------- | ---------------------------------------------- |
| Timeframe | 5-min chart, 1-min for entry                   |
| Markets   | VN30F, High Beta HSX Stocks                    |
| Context   | Must occur in an intraday uptrend (Higher Lows)|

### Long Entry (Breakout)
1. **Context:** Stock is in an uptrend and has established a clear HOD earlier in the session.
2. **The Approach:** Price pulls back but forms a clear Higher Low, then returns to the HOD.
3. **The Tell (Consolidation):** Price hits the HOD but *does not reject hard*. It forms 3-5 tight candles (on the 5-min chart) just 0.1% - 0.3% below the HOD.
4. **Trigger:** A 1-min or 5-min candle breaks above the HOD level.
5. **Volume:** Must spike on the breakout candle.
6. **Entry:** Go Long on the breakout.
7. **Stop Loss:** Below the tight consolidation built just under the HOD.

---

## Exit Rules

- **Target 1:** 1x the distance of the prior pullback. Take 50%.
- **Target 2:** Trail the remaining 50% using a 9-EMA on the 5-min chart. This often catches the "trend of the day".
- **Failure:** If price breaks the HOD but immediately reverses and closes below the consolidation (a Fakey), exit immediately.

---

## Filters

- [ ] **Crucial:** Look at the pullback between the first HOD and the second test. It MUST be a higher low. If it's a deep pullback that breaks VWAP, the second test is more likely to be a true Double Top.
- [ ] If price rejects hard off the second test (long upper wick, big red candle), abort the Long idea. We want to see TIGHT, quiet consolidation at the highs.
- [ ] Ensure the broader market (VN-Index) is not tanking.

---

## Risk Management

| Rule             | Guideline                          |
| ---------------- | ---------------------------------- |
| Max Risk/Trade   | 1% of account equity               |
| Stop Placement   | Tightly below the pre-breakout flag|
| Min R:R          | 1:2                                |

---

## Edge & Statistics

- **Win rate:** 55-60%.
- **Edge:** You are trading against retail psychology. By waiting for the tight consolidation, you ensure that sellers are exhausted. The stop loss is extremely tight, offering asymmetric R:R.

---

## Example Trade Log

```
Date:      2026-06-18
Symbol:    VN30F2607
Context:   Sets HOD at 1,280 at 09:45. Pulls back to 1,272 (Higher Low).
Approach:  At 10:30, price returns to 1,280.
Consolidation: Price trades tightly between 1,278 and 1,279.5 for 20 minutes (4 candles). No hard rejection.
Breakout:  At 10:55, price breaks 1,280 with a volume surge.
Entry:     1,280.5 (Long)
Stop:      1,277.5 (Below the tight consolidation)
Target:    1,288 (1x pullback distance) -> Hit at 11:15.
Result:    +WIN (+7.5 pts).
```

---

## Notes & Improvements
- This pattern is essentially an Ascending Triangle or a High Tight Flag. Recognizing the psychology behind it (trapped shorts) gives you the conviction to hold for bigger targets.

---
*Category: Breakout / Market Psychology | Timeframe: Intraday (1-min/5-min) | Market: VN30F / HSX Stocks*
