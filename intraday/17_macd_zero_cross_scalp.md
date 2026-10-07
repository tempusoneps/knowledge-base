# 17 — MACD Zero-Line Cross Scalp

## Overview

The MACD (Moving Average Convergence Divergence) histogram crossing the zero line represents a shift in medium-term momentum — the faster EMA crossing the slower EMA. When this crossover aligns with price structure (above/below VWAP) and occurs with expanding histogram bars, it provides a mechanical, systematic scalping signal with clear entry and exit rules.

---

## Concept

```
MACD Line    = EMA(12) − EMA(26)
Signal Line  = EMA(9) of MACD Line
Histogram    = MACD Line − Signal Line

Zero-Line Cross:
  MACD > 0: Fast EMA above Slow EMA → Bullish momentum → Long bias
  MACD < 0: Fast EMA below Slow EMA → Bearish momentum → Short bias

Key signal: Histogram CROSSING zero (not just moving toward it)
```

**The zero-line cross is more reliable than signal-line crossovers** because it represents an actual EMA crossover, not just a derivative calculation.

---

## Indicators Required

| Indicator    | Setting          | Purpose                              |
|--------------|------------------|--------------------------------------|
| MACD         | 12, 26, 9        | Primary momentum indicator           |
| MACD Histogram| Bars            | Visual strength and direction        |
| VWAP         | Daily            | Trend filter / directional bias      |
| EMA          | 50-period        | Secondary trend filter               |
| Volume       | 20-bar MA        | Confirm momentum on cross            |

---

## Setup & Entry Rules

| Parameter    | Value                                              |
|--------------|----------------------------------------------------|
| Timeframe    | 5-min chart                                        |
| Markets      | VN30F, VCB, HPG, FPT (trending stocks)             |
| Session      | 09:30 – 13:30                                      |
| Signal       | MACD histogram crossing zero from negative to positive (Long) |

### Long Entry (Bullish Zero-Line Cross)
1. MACD histogram crosses from negative to positive (zero cross).
2. MACD Line is below 0 before cross (coming from bearish territory).
3. Price is **above VWAP** or just crossed above (trend alignment).
4. Histogram bars expanding (getting larger positive values).
5. Volume above average on the cross candle.
6. Enter Long on the cross candle close.
7. Stop Loss: Below the recent swing low or VWAP.

### Short Entry (Bearish Zero-Line Cross)
1. MACD histogram crosses from positive to negative.
2. Price is below VWAP.
3. Histogram bars expanding negatively.
4. Volume confirms.
5. Enter Short on cross candle close.
6. Stop Loss: Above recent swing high or VWAP.

---

## Exit Rules

- **Target 1:** When histogram starts declining after peak (momentum slowing) → close 50%.
- **Target 2:** Previous swing high/low or next S/R → close 50%.
- **Signal Exit:** When MACD histogram starts moving back toward zero → exit remaining.
- **Trail:** Trail stop at EMA(26) level.
- **Time Stop:** Close all before 14:00.

---

## Filters

- [ ] Only trade zero-line crosses that come after the histogram has been on one side for at least 6 bars (meaningful momentum shift).
- [ ] Skip if histogram barely crossed zero (< 0.5 in absolute value) — weak signal.
- [ ] Skip if price is far extended from VWAP (entering late in the move).
- [ ] Avoid in choppy sessions where MACD oscillates around zero repeatedly.
- [ ] Do not trade more than 2 zero-line crosses in the same direction per session.

---

## Risk Management

| Rule              | Guideline                    |
|-------------------|------------------------------|
| Max Risk/Trade    | 0.75% of account equity      |
| Stop Placement    | Below/above swing extreme    |
| Min R:R           | 1:1.5                        |
| Max Trades/Day    | 4 scalps                     |
| Daily Loss Limit  | −2%                          |

---

## Edge & Statistics

- Win rate: **48–55%** (mechanical system).
- R:R: ~1:1.8 → positive expectancy.
- Best on: Trending markets with clear momentum phases.
- Worst on: Whipsaw days where MACD crosses zero 5+ times.

---

## Example Trade Log

```
Date:      2026-06-13
Symbol:    VN30F2607
Signal:    MACD histogram crosses zero at 10:10 (negative → positive)
Histogram: -2.1 → -0.8 → +0.4 → +1.2 (expanding) ✓
VWAP:      1,268, price at 1,270 (above VWAP ✓)
Volume:    1.6× average ✓
Entry:     1,271 (Long)
Stop:      1,265 (below VWAP / swing low)
T1:        1,278 (histogram peak, starts declining) ← 50%
T2:        1,283 (prior resistance) ← 50%
Result:    +WIN
```

---

## Notes & Improvements

- **Use MACD on 15-min** as a trend filter: only take 5-min Long signals when 15-min MACD is also above zero.
- Optimize MACD parameters per symbol (VN30F may respond better to 8/17/9).
- Combine with **RSI**: if RSI is between 50–60 when MACD crosses zero (not overbought), higher success rate.
- Automate signal detection: scan for zero-line crosses across all VN30 constituents at the open.

---

*Category: Momentum Scalping | Timeframe: Intraday (5-min) | Market: VN30F / HSX Stocks*
