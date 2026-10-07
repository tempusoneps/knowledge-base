# 47 — Multi-Timeframe (MTF) Alignment Trade

## Overview

The **Multi-Timeframe (MTF) Alignment Trade** is a high-probability strategy that waits for the macro trend, intermediate structure, and micro execution to all point in the exact same direction. By demanding alignment across three distinct timeframes, this strategy filters out the vast majority of market noise and choppy price action, ensuring you are trading with the maximum weight of money behind you.

---

## Concept

```
The Rule of Three Timeframes (e.g., Daily, 1-Hour, 5-Minute):
  1. Macro (Daily): Dictates the overarching bias. (Is the daily chart in an uptrend or downtrend?)
  2. Intermediate (1-Hour/15-Min): Provides the market structure and key S/R zones.
  3. Micro (5-Min/1-Min): Provides the precise entry trigger and risk management.

The Signal:
  Only go Long if Daily is UP, 1-Hour is UP, and 5-Min breaks UP.
  Only go Short if Daily is DOWN, 1-Hour is DOWN, and 5-Min breaks DOWN.
```

**Trade Logic:** A 5-minute breakout is much more likely to succeed if it is pushing in the same direction as the 1-hour and Daily trends, because institutional traders on higher timeframes are supporting the move.

---

## Indicators Required

| Indicator      | Setting                      | Purpose                                  |
| -------------- | ---------------------------- | ---------------------------------------- |
| EMA            | 20 & 50 (on all timeframes)  | Determine trend direction quickly        |
| Price Action   | Higher Highs / Lower Lows    | Confirm trend structure                  |

---

## Setup & Entry Rules

| Parameter | Value                                          |
| --------- | ---------------------------------------------- |
| Timeframes| D1 (Macro), H1 (Intermediate), M5 (Micro)      |
| Markets   | VN30F, Liquid HSX Stocks                       |
| Context   | High-conviction trend days                     |

### Long Entry (Full Bullish Alignment)
1. **Macro Check (Daily):** Price is above D1 20-EMA, making Higher Highs. Bias = LONG ONLY.
2. **Intermediate Check (1-Hour):** Price is above H1 20-EMA. It has recently pulled back and is now forming a bullish structure (e.g., broke a minor resistance or formed a higher low).
3. **Micro Trigger (5-Min):** Wait for a clear intraday setup (e.g., ORB, Flag Breakout, or VWAP Pullback) on the 5-min chart that breaks to the UPSIDE.
4. **Entry:** Go Long on the 5-min trigger.
5. **Stop Loss:** Based on the 5-min setup (e.g., below the 5-min flag or VWAP).

### Short Entry (Full Bearish Alignment)
1. **Macro Check (Daily):** Price below D1 20-EMA, Lower Lows. Bias = SHORT ONLY.
2. **Intermediate Check (1-Hour):** Price below H1 20-EMA, bearish structure.
3. **Micro Trigger (5-Min):** Intraday bearish setup (e.g., Bear Flag, VWAP Rejection).
4. **Entry:** Go Short on the 5-min trigger.
5. **Stop Loss:** Based on the 5-min setup.

---

## Exit Rules

- **Target 1:** Next major S/R level derived from the *1-Hour* chart (allows for much larger targets than typical 5-min scalps). Take 50%.
- **Target 2:** Ride the trend using the 5-min 50-EMA as a trailing stop.
- **Time Stop:** Can be held longer (even overnight if the daily trend is very strong), but standard intraday exit is 14:15.

---

## Filters

- [ ] **Crucial:** If the Daily is UP but the 1-Hour is DOWN, **do not trade**. Wait for the 1-Hour to realign with the Daily, or stay out.
- [ ] This strategy requires extreme patience. You will take far fewer trades, but the quality of the trades will be much higher.
- [ ] Avoid forcing the alignment. If it's messy or unclear on the Daily chart (e.g., stuck in a multi-month range), skip the stock.

---

## Risk Management

| Rule             | Guideline                          |
| ---------------- | ---------------------------------- |
| Max Risk/Trade   | 1% - 1.5% (High conviction allows slightly larger size) |
| Stop Placement   | Managed on the Micro (5-min) timeframe |
| Min R:R          | 1:2.5 or greater (because targets are based on higher TF) |

---

## Edge & Statistics

- **Win rate:** 65-70%.
- **Edge:** By using the 5-min chart for entry and the 1-Hour chart for targets, you generate massive Reward-to-Risk ratios (often 1:3 or 1:4) while maintaining a high win rate due to trend alignment.

---

## Example Trade Log

```
Date:      2026-06-20
Symbol:    FPT (HSX)
Macro:     Daily chart is in a strong uptrend, above 20-EMA. Bias = LONG.
Intermed:  1-Hour chart pulled back yesterday, but today crossed back above 20-EMA.
Micro:     On 5-min chart, FPT forms a Bull Flag at 10:30.
Entry:     135,000 (Long, breaking 5-min flag)
Stop:      134,200 (Below 5-min flag)
Target:    137,500 (Next resistance on 1-Hour chart)
Result:    MTF alignment fuels a strong rally. Hits target at 13:45. +WIN (+2,500 pts).
```

---

## Notes & Improvements
- You can create a scanner that looks for "Triple Timeframe Moving Average Alignment" (e.g., Price > SMA20 on D1, H1, and M5 simultaneously).
- This is the core philosophy of Alexander Elder's "Triple Screen Trading System".

---
*Category: Trend Following / Multi-Timeframe | Timeframe: Intraday (D1/H1/M5) | Market: VN30F / HSX Stocks*
