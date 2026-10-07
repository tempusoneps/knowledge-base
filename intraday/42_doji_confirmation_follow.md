# 42 — Doji + Confirmation Follow

## Overview

A **Doji** candlestick forms when the open and close are at the exact same (or very close) price level. It represents absolute indecision and a balance between buyers and sellers. While a Doji by itself is not a signal to trade, the **candle immediately following the Doji** provides the breakout confirmation. This strategy trades the break of the Doji's range in the direction of the confirmation candle.

---

## Concept

```
Doji Types:
  Standard Doji: Cross shape (+).
  Long-Legged Doji: Long wicks up and down. High volatility indecision.
  Gravestone Doji: Long upper wick, open/close at low. Bearish bias.
  Dragonfly Doji: Long lower wick, open/close at high. Bullish bias.

The Setup:
  1. Doji forms, setting a High and a Low range.
  2. Next candle breaks the High -> Buyers win the tug-of-war -> Long
  3. Next candle breaks the Low -> Sellers win -> Short
```

**Trade Logic:** The Doji is a coiled spring of indecision. The breakout of its range shows which side has committed capital to break the stalemate.

---

## Indicators Required

| Indicator      | Setting                      | Purpose                                  |
| -------------- | ---------------------------- | ---------------------------------------- |
| Candlesticks   | Standard OHLC                | Identify Doji and range                  |
| EMA            | 20-period                    | Ensure trade is with the short-term trend|
| Volume         | 20-bar MA                    | Confirm the breakout direction           |

---

## Setup & Entry Rules

| Parameter | Value                                          |
| --------- | ---------------------------------------------- |
| Timeframe | 5-min or 15-min chart                          |
| Markets   | VN30F, Liquid HSX Stocks                       |
| Context   | Best during trend pullbacks (continuation)     |

### Long Entry (Doji Breakout Up)
1. **Context:** Price is generally trending up (above EMA20) but has pulled back for 2-3 candles.
2. **The Setup:** A Doji candle forms. Note its High and Low.
3. **Confirmation:** The *very next candle* closes **above** the High of the Doji.
4. **Volume:** Above average on the confirmation candle.
5. **Entry:** Go Long on the close of the confirmation candle.
6. **Stop Loss:** Below the Low of the Doji.

### Short Entry (Doji Breakdown Down)
1. **Context:** Price trending down (below EMA20), rallies for 2-3 candles.
2. **The Setup:** Doji forms.
3. **Confirmation:** Next candle closes **below** the Low of the Doji.
4. **Volume:** Above average.
5. **Entry:** Go Short on confirmation close.
6. **Stop Loss:** Above the High of the Doji.

---

## Exit Rules

- **Target 1:** 1.5x the risk (distance from entry to stop). Take 50%.
- **Target 2:** Next major structure (Swing High/Low). Take 50%.
- **Trailing Stop:** Move to break-even after T1.
- **Time Stop:** Do not hold Doji trades if they stagnate for more than 4 candles. The move should be immediate.

---

## Filters

- [ ] **Crucial:** Do not trade a Doji in a choppy, sideways market. It only works as a pause/continuation pattern in a trending environment, or at a major S/R level.
- [ ] If the confirmation candle is a massive wide-range candle that hits your target immediately, skip the entry (R:R is ruined).
- [ ] The Doji range must not be excessively large (e.g., a massive long-legged doji makes the stop loss too wide).

---

## Risk Management

| Rule             | Guideline                          |
| ---------------- | ---------------------------------- |
| Max Risk/Trade   | 1% of account equity               |
| Stop Placement   | Beyond the Doji extreme            |
| Min R:R          | 1:1.5                              |

---

## Edge & Statistics

- **Win rate:** ~55%.
- **Edge:** The stop loss is usually very tight (just the range of the Doji), allowing for excellent R:R.

---

## Example Trade Log

```
Date:      2026-06-25
Symbol:    TCB (HSX)
Context:   Uptrend. Price pulls back to EMA20 at 10:15.
Doji:      10:20 candle is a perfect Doji (High 42,500, Low 42,350).
Confirm:   10:25 candle closes strongly at 42,600 (above Doji High).
Entry:     42,600 (Long)
Stop:      42,300 (Below Doji Low)
Target:    43,050 (1.5x R:R = +450 pts)
Result:    Trend resumes. Hits target at 11:10. +WIN.
```

---

## Notes & Improvements
- A Doji followed by an Inside Bar (or vice versa) is an even tighter coil of volatility, often leading to explosive moves.

---
*Category: Price Action / Continuation | Timeframe: Intraday | Market: VN30F / HSX Stocks*
