# 44 — 52-Week High Momentum Day

## Overview

Stocks that break out to a new **52-Week High** attract massive attention from algorithms, momentum funds, and retail traders. On the day a stock clears this major level, it often exhibits extraordinary intraday trending behavior with shallow pullbacks. This strategy involves finding stocks breaking 52-week highs and trading their intraday pullbacks for momentum continuation.

---

## Concept

```
Macro Context:
  A stock breaking a 52-week high has no overhead supply (bagholders waiting to sell at breakeven).
  Every holder is in profit. Short sellers are trapped and forced to cover.
  This creates a "blue sky" environment for price discovery.

Intraday Strategy:
  Do not buy the exact breakout (high risk of fake-out).
  Instead, let the stock break the 52-week high in the morning.
  Wait for the first intraday pullback to VWAP or EMA9.
  Buy the pullback for continuation.
```

---

## Indicators Required

| Indicator      | Setting                      | Purpose                                  |
| -------------- | ---------------------------- | ---------------------------------------- |
| Scanner        | 52-Week High Breakout        | Identify candidates pre-market or early  |
| VWAP           | Daily                        | Primary support level                    |
| EMA            | 9-period on 5-min            | Dynamic support for strong trends        |

---

## Setup & Entry Rules

| Parameter | Value                                          |
| --------- | ---------------------------------------------- |
| Timeframe | 5-min chart                                    |
| Markets   | HSX Stocks (Mid-caps and Large-caps)           |
| Context   | Stock must have broken 52-wk high today        |

### Long Entry (Continuation Pullback)
1. **Identify Target:** Stock breaks its 52-week high level in the morning session (09:15 - 10:30) with massive volume.
2. **Wait for Pullback:** Let the initial surge cool off. Wait for price to pull back toward the 9-EMA or Daily VWAP.
3. **Trigger:** A bullish reversal candle (hammer, doji, engulfing) forms at the 9-EMA or VWAP.
4. **Volume Check:** Volume should be light on the pullback and increase on the reversal candle.
5. **Entry:** Go Long on the close of the reversal candle.
6. **Stop Loss:** Below the VWAP or the swing low of the pullback.

---

## Exit Rules

- **Target 1:** The High of Day (HOD) established during the morning surge. Take 50%.
- **Target 2:** Uncharted territory. Trail the remaining 50% using the 9-EMA. If a 5-min candle closes below the 9-EMA, exit.
- **Time Stop:** Can hold into the close (ATC) if it closes strong, but for pure intraday, exit by 14:25.
- **Failure:** If price breaks the 52-week high but then collapses below VWAP and stays there, the breakout has failed. Exit immediately.

---

## Filters

- [ ] **Crucial:** Confirm on the Daily chart that it is a true 52-week high, not just a recent swing high.
- [ ] Skip if the breakout volume is lower than the 20-day average. A true 52-week breakout needs institutional participation.
- [ ] Avoid chasing. Only buy the pullback. Buying extended 52-week highs intraday often results in getting stopped out on standard volatility.

---

## Risk Management

| Rule             | Guideline                          |
| ---------------- | ---------------------------------- |
| Max Risk/Trade   | 1% of account equity               |
| Stop Placement   | Below VWAP or the pullback structure|
| Min R:R          | 1:2                                |
| Sizing           | Standard size                      |

---

## Edge & Statistics

- **Win rate:** ~60% when buying the first VWAP/EMA9 pullback.
- **Edge:** The lack of overhead resistance means that once the pullback is bought, the price can move up rapidly with very little friction.

---

## Example Trade Log

```
Date:      2026-06-25
Symbol:    GMD (HSX)
Context:   GMD breaks 52-week high of 80,000 at 09:30, surging to 82,500.
Pullback:  At 10:45, price drifts down to 81,000, perfectly touching the rising VWAP.
Trigger:   Hammer candle forms at VWAP on low volume. Next candle is strong green.
Entry:     81,200 (Long)
Stop:      80,700 (Below VWAP and hammer low)
Target:    82,500 (HOD test) -> 84,000 (Trail)
Result:    Hits HOD at 13:15, trails out at 83,500 just before close. +WIN (+2,300 pts).
```

---

## Notes & Improvements
- Build a custom scanner to alert you the moment any stock in your watchlist crosses its 250-day high.
- This is one of the best setups for Swing Trading as well. If the stock closes near its high, you can convert the intraday position to an overnight hold.

---
*Category: Momentum Breakout / Pullback | Timeframe: Intraday (5-min) | Market: HSX Stocks*
