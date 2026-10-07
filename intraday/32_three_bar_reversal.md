# 32 — 3-Bar Reversal Pattern

## Overview

The **3-Bar Reversal** (also called 3-Candle Reversal) is a simple but powerful price action signal. After an extended trend, three specific candles appear: the trend continuation candle, a key reversal candle (the pivot), and a confirmation candle closing against the prior trend. This pattern captures the precise moment momentum shifts, offering tight stops and clear entry rules.

---

## Concept

```
BEARISH 3-BAR REVERSAL (at top):
  Bar 1: Strong up candle (trend continuation)
  Bar 2: Reversal candle — HIGHER HIGH but closes near low (shooting star / engulfing bear)
  Bar 3: Down candle closing BELOW Bar 2 low → Confirmation → Enter Short

  Example:
  Bar1:  Open 1,270  Close 1,278  (bullish)
  Bar2:  Open 1,278  High 1,283  Close 1,275  (upper wick rejection)
  Bar3:  Open 1,275  Close 1,270  ← Enter Short on this close
  Stop:  Above Bar2 High (1,283)

BULLISH 3-BAR REVERSAL (at bottom):
  Bar 1: Strong down candle
  Bar 2: Lower low but closes near high (hammer)
  Bar 3: Up candle closing above Bar 2 high → Long entry
  Stop:  Below Bar 2 Low
```

---

## Setup & Entry Rules

| Parameter    | Value                                          |
|--------------|------------------------------------------------|
| Timeframe    | 5-min chart                                    |
| Markets      | VN30F, any liquid HSX stock                    |
| Session      | 09:30 – 13:30                                  |
| Context      | Must occur after sustained trend of 5+ bars    |

### Long Entry (Bullish 3-Bar)
1. Price has been in a downtrend for 5+ consecutive 5-min bars.
2. Bar 1: Continuation down candle.
3. Bar 2: Makes new low, but closes in upper half of its range (hammer-like).
4. Bar 3: Closes **above Bar 2's high** — confirmation complete.
5. Enter Long on Bar 3 close.
6. Stop Loss: Below Bar 2's low.
7. Target: Beginning of the downtrend or VWAP.

### Short Entry (Bearish 3-Bar)
1. Uptrend for 5+ bars.
2. Bar 1: Continuation up candle.
3. Bar 2: New high but closes in lower half of its range.
4. Bar 3: Closes **below Bar 2's low**.
5. Enter Short on Bar 3 close.
6. Stop: Above Bar 2's high.

---

## Quality Enhancement Checklist

| Criterion                                          | Adds Conviction |
|----------------------------------------------------|-----------------|
| Bar 2 has a prominent wick (>50% of bar range)     | +High           |
| Bar 3 closes with above-average volume             | +High           |
| Pattern at a key S/R level or VWAP                 | +Very High      |
| RSI divergence on Bar 1 vs prior bar               | +High           |
| Bar 3 closes strongly (near its own extreme)       | +Medium         |

---

## Exit Rules

- **Target 1:** 1× the height of Bar 2 from Bar 3's close → close 60%.
- **Target 2:** Prior swing high/low or VWAP → close 40%.
- **Trail:** Trail stop below/above each new candle's low/high.
- **Failure:** If price closes back above Bar 2's high (for Short) → exit immediately.
- **Time Stop:** Close before 14:00.

---

## Filters

- [ ] Do not trade 3-bar reversals in the middle of a range (need clear trend first).
- [ ] Skip if Bar 2 range is very small (< 0.2% — not a meaningful reversal candle).
- [ ] Skip if the broader market is strongly trending against the trade direction.
- [ ] Avoid late-session patterns (13:30 onwards) — insufficient time for move to develop.
- [ ] Skip if the prior trend was less than 5 candles (too short for reliable reversal).

---

## Risk Management

| Rule              | Guideline                       |
|-------------------|---------------------------------|
| Max Risk/Trade    | 0.75% of account equity         |
| Stop Placement    | Beyond Bar 2 extreme            |
| Min R:R           | 1:1.5 at entry                  |
| Max Trades/Day    | 4 patterns                      |
| Daily Loss Limit  | −2%                             |

---

## Edge & Statistics

- Win rate: **55–65%** with S/R confluence.
- Tight stop (just beyond Bar 2) allows good R:R even with ~50% win rate.
- Best on: All market conditions — the pattern is universal and condition-agnostic.
- Worst on: Very choppy, low-ATR sessions where bars are too small to signal meaningfully.

---

## Example Trade Log

```
Date:       2026-06-08
Symbol:     HPG (HSX)
Trend:      7-bar downtrend on 5-min (09:20–09:55)
Bar 1:      09:50 → Open 27,200 Close 27,050 (continuation down)
Bar 2:      09:55 → Low 26,950 Close 27,150 (hammer wick ✓)
Bar 3:      10:00 → Closes at 27,250 (above Bar 2 high ✓), volume 1.8× ✓
Entry:      27,250 (Long on Bar 3 close)
Stop:       26,940 (below Bar 2 low)
T1:         27,550 (1× Bar 2 height) ← 60% at 10:15
T2:         27,800 (VWAP) ← 40% at 10:35
Result:     +WIN
```

---

## Notes & Improvements

- Combine with **MACD**: if MACD histogram shows bullish/bearish divergence when Bar 2 forms → stronger signal.
- **Morning Star** and **Evening Star** (3-bar candlestick patterns from Japanese charting) are essentially the same concept with Japanese names — same rules apply.
- Backtest: measure which "prior trend length" (5 bars? 8 bars? 10 bars?) produces the highest reversal success rate.
- This pattern is programmable: scan for it across all VN30 stocks in real-time using candle classification logic.

---

*Category: Price Action Reversal | Timeframe: Intraday (5-min) | Market: VN30F / HSX Stocks*
