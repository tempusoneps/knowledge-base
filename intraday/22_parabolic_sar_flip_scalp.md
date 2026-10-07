# 22 — Parabolic SAR Flip Scalp

## Overview

The **Parabolic SAR (Stop and Reverse)** is a trend-following indicator that places dots above price (bearish) or below price (bullish). When the SAR "flips" — dots move from above to below price (or vice versa) — it signals a momentum reversal. This strategy uses SAR flips as entry triggers, filtered by trend context, for systematic mechanical scalping.

---

## Concept

```
SAR Formula:
  SAR(n+1) = SAR(n) + AF × (EP − SAR(n))
  AF (Acceleration Factor): starts at 0.02, increases by 0.02 each period (max 0.20)
  EP (Extreme Point): highest high (uptrend) or lowest low (downtrend)

SAR Flip:
  Dots above → below price = BULLISH FLIP → Long signal
  Dots below → above price = BEARISH FLIP → Short signal

The higher the AF, the faster SAR converges to price → earlier but noisier flips.
```

**Key advantage:** SAR provides both the trade signal AND the stop loss level simultaneously (the dot location = stop).

---

## Indicators Required

| Indicator      | Setting        | Purpose                          |
|----------------|----------------|----------------------------------|
| Parabolic SAR  | 0.02, 0.20     | Entry signal + built-in stop     |
| EMA            | 50-period      | Trend filter                     |
| VWAP           | Daily          | Directional bias                 |
| Volume         | 20-bar MA      | Confirm flip momentum            |
| RSI            | 14-period      | Filter extreme entries           |

---

## Setup & Entry Rules

| Parameter    | Value                                          |
|--------------|------------------------------------------------|
| Timeframe    | 5-min chart                                    |
| Markets      | VN30F, trending HSX stocks (FPT, HPG, VCB)     |
| Session      | 09:30 – 13:30                                  |
| AF Setting   | 0.02/0.20 (standard); try 0.01/0.15 for slower|

### Long Entry (Bullish SAR Flip)
1. SAR flips from above price to below price.
2. Price is above EMA50 (trending upward context).
3. Price is above VWAP.
4. RSI is between 45–65 (not overbought).
5. Volume on flip candle > average.
6. Enter Long at next candle open.
7. Stop Loss: At the SAR dot level (updates each candle).

### Short Entry (Bearish SAR Flip)
1. SAR flips from below price to above price.
2. Price below EMA50.
3. Price below VWAP.
4. RSI between 35–55.
5. Volume confirms.
6. Enter Short at next candle open.
7. Stop Loss: At the SAR dot level above price.

---

## Exit Rules

- **Trailing Exit:** Trail the stop at the SAR dot level each candle (SAR is the exit).
- **Hard Target:** When SAR dot is more than 1.5% away from current price (overextended) → take partial profits.
- **Signal Exit:** When SAR flips against the trade → exit.
- **Time Stop:** Close before 14:00.
- **Early Exit:** If price stalls for 5+ candles without progress → exit manually.

---

## Filters

- [ ] Skip SAR flips that occur during lunch consolidation (12:00–13:00).
- [ ] Skip the first SAR flip of the session (09:15–09:30) — often whipsaw.
- [ ] Only take flips in the direction of the 15-min trend.
- [ ] Skip if AF has just reset (first flip after long trend = can be reliable, but verify volume).
- [ ] Avoid if price is at a major S/R level immediately after the flip (could reverse quickly).

---

## Risk Management

| Rule              | Guideline                        |
|-------------------|----------------------------------|
| Max Risk/Trade    | 0.75% of account equity          |
| Stop Placement    | SAR dot level (dynamic)          |
| Min R:R           | Measure at entry: must be ≥ 1:1.5|
| Max Trades/Day    | 4 SAR flips                      |
| Daily Loss Limit  | −2%                              |

---

## Edge & Statistics

- Win rate: **45–55%** (pure mechanical trailing system).
- Wins are large (catch full trends); losses are small and consistent.
- Best on: Strong trending sessions with clear directional bias.
- Worst on: Whipsaw days (SAR flips 6+ times = chop, stop trading).

---

## Example Trade Log

```
Date:        2026-06-19
Symbol:      VN30F2607
SAR Flip:    10:00 — SAR moves below price at 1,272 (bullish flip)
EMA50:       Price 1,272 > EMA50 1,265 ✓
VWAP:        1,268, price above ✓
RSI:         52 ✓
Volume:      Average ✓
Entry:       1,273 (Long, next candle open)
SAR Stop:    1,267 → 1,269 → 1,271 (trails upward each candle)
Final Exit:  1,285 (SAR flips at 13:00)
Result:      +WIN (+12 pts, caught strong closing drive)
```

---

## Notes & Improvements

- Adjust AF based on market volatility: use **0.01/0.10** on low-volatility days to reduce whipsaws.
- Combine with **ADX filter**: only trade SAR flips when ADX > 20 (confirming a trend exists).
- SAR works best as a **trailing stop** tool even if you use other methods for entry.
- Test SAR on 15-min chart for fewer but higher-quality flips with less noise.

---

*Category: Trend Following / Scalping | Timeframe: Intraday (5-min) | Market: VN30F / HSX Stocks*
