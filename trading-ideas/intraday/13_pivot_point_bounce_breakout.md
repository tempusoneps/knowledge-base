# 13 — Pivot Point Bounce & Breakout

## Overview

Pivot Points are mathematically derived price levels calculated from the prior day's High, Low, and Close. They act as predictive support and resistance for the current session and are widely followed by floor traders, institutions, and retail algorithmic systems — creating self-fulfilling precision at these levels. Both bounce trades (from pivot levels) and breakout trades (through pivot levels) are viable intraday strategies.

---

## Concept

```
Classic Pivot:
  PP  = (PDH + PDL + PDC) / 3
  R1  = 2 × PP − PDL
  R2  = PP + (PDH − PDL)
  R3  = PDH + 2 × (PP − PDL)
  S1  = 2 × PP − PDH
  S2  = PP − (PDH − PDL)
  S3  = PDL − 2 × (PDH − PDL)

Camarilla Pivot (tighter, for mean reversion):
  H4 = PDC + (PDH − PDL) × 1.1/2
  L4 = PDC − (PDH − PDL) × 1.1/2
  H3 = PDC + (PDH − PDL) × 1.1/4
  L3 = PDC − (PDH − PDL) × 1.1/4
```

**Usage:**
- Price near PP/S1/R1 → **Bounce trade** (mean reversion).
- Price breaks through R1/R2 or S1/S2 → **Breakout trade** (momentum).

---

## Indicators Required

| Indicator          | Setting            | Purpose                       |
|--------------------|--------------------|-------------------------------|
| Classic Pivot      | Daily (PDH/PDL/PDC)| Primary S/R framework         |
| Camarilla H3/H4    | Daily calculation  | Mean reversion tight levels   |
| Volume             | 20-bar MA          | Confirms bounce/breakout      |
| RSI                | 14-period          | Momentum confirmation         |

---

## Setup & Entry Rules

| Parameter    | Value                                          |
|--------------|------------------------------------------------|
| Timeframe    | 5-min chart                                    |
| Markets      | VN30F (most reliable pivot response)           |
| Calculation  | Use previous day's H/L/C (HOSE session)        |
| Session      | 09:15 – 14:00                                  |

### Long Entry — Pivot Bounce (at S1/S2/PP)
1. Price falls to S1 or S2 level.
2. A reversal candle forms (hammer, bullish engulfing).
3. RSI < 40 and turning up.
4. Enter Long on candle close. Stop: 0.5% below the pivot level.
5. Target: Next pivot level above (S1 → PP → R1).

### Long Entry — Pivot Breakout (above R1/R2)
1. Price consolidates just below R1 for at least 3 candles.
2. Strong 5-min candle closes above R1 with high volume.
3. Enter Long on next candle open. Stop: Back below R1.
4. Target: R2, then R3.

### Short Entry — Mirror logic at R1/R2 bounce and S1/S2 breakdown.

---

## Exit Rules

- **Bounce Target:** Next pivot level (S1 → PP = 1 level move).
- **Breakout Target:** R1 to R2 distance applied from breakout.
- **Trail:** After first target hit, trail stop to break-even.
- **Failure:** Price closes back through pivot level → exit immediately.
- **Time Stop:** No new pivot trades after 14:00.

---

## Filters

- [ ] Calculate pivots correctly using prior HOSE session only (no overnight data).
- [ ] Skip if PP is within 0.2% of a round number (conflicting levels).
- [ ] Avoid first touch of any pivot in first 15 min (volatile open).
- [ ] Skip breakout if range between pivot levels < 0.4% (levels too compressed).
- [ ] Check if VN30F is trading in Premium or Discount vs. cash index.

---

## Risk Management

| Rule              | Guideline                       |
|-------------------|---------------------------------|
| Max Risk/Trade    | 0.75% of account equity         |
| Stop Placement    | 0.5% beyond pivot level         |
| Min R:R           | 1:1.5                           |
| Max Trades/Day    | 4 (bounce + breakout each side) |
| Daily Loss Limit  | −2%                             |

---

## Edge & Statistics

- Win rate: **55–65%** for bounce trades at S1/PP/R1.
- Breakout through R2/S2: lower win rate (~45%) but higher R:R (1:3+).
- Best on: Normal to moderately trending days.
- Worst on: Days with major economic releases that shift volatility regime.

---

## Example Trade Log

```
Date:      2026-06-11
Symbol:    VN30F2607
PDH:       1,285 / PDL: 1,265 / PDC: 1,278
PP:        1,276   S1: 1,267   R1: 1,285   R2: 1,294
Action:    Price falls to S1 (1,267) at 10:15 → hammer candle
RSI:       34 ↑
Entry:     1,268 (Long)
Stop:      1,261 (-7 pts)
T1:        1,276 (PP) ← 60% closed
T2:        1,285 (R1) ← 40% closed
Result:    +WIN
```

---

## Notes & Improvements

- Pre-market: Calculate and mark ALL pivot levels before open (automate with Python).
- Add **weekly pivot** levels for stronger confluence signals.
- Camarilla H4/L4 levels work best for **morning gap fade** trades.
- Compare pivot levels with VWAP: if VWAP coincides with a pivot, conviction doubles.

---

*Category: Price Action | Timeframe: Intraday (5-min) | Market: VN30F / HSX Stocks*
