# 35 — Volume Dry-Up Breakout

## Overview

The **Volume Dry-Up Breakout** strategy capitalizes on the principle of volatility compression. As a stock consolidates within a tight range, volume often steadily declines (dries up), indicating that selling pressure has been exhausted and the market has reached equilibrium. When volume suddenly expands alongside a price breakout from this tight range, it signals the start of a new, energetic directional move.

---

## Concept

```
Phase 1: Impulse (Strong move up or down)
Phase 2: Consolidation (Price trades sideways in a tight range)
         -> Volume steadily declines (Dry-up)
         -> Volatility compresses
Phase 3: Breakout
         -> Price breaks range boundary
         -> Volume spikes > 2x average
```

**Key insight:** The longer the dry-up period and the tighter the price range, the more explosive the subsequent breakout tends to be.

---

## Indicators Required

| Indicator | Setting        | Purpose                                       |
| --------- | -------------- | --------------------------------------------- |
| Volume    | Raw + 20-MA    | Identify dry-up phase and breakout spike      |
| BB Width  | 20, 2          | Quantify volatility compression (optional)    |
| EMA       | 50-period      | Determine prior trend context                 |

---

## Setup & Entry Rules

| Parameter | Value                                           |
| --------- | ----------------------------------------------- |
| Timeframe | 5-min or 15-min chart                           |
| Markets   | VN30F, Mid/Large-cap HSX stocks with liquidity  |
| Session   | 09:30 – 14:00 (Breakouts best before afternoon) |

### Long Entry (Bullish Breakout)
1. **Context:** Price is in a broader uptrend (above EMA50).
2. **Consolidation:** Price trades in a tight range (e.g., < 1% width) for at least 1-2 hours.
3. **Volume Dry-Up:** Volume bars consistently shrink during consolidation, dipping well below the 20-bar average.
4. **Trigger:** A 5-min candle closes **above** the consolidation resistance.
5. **Confirmation:** Volume on the breakout candle is **> 2x** the average volume of the dry-up phase.
6. **Entry:** Go Long at the close of the breakout candle.
7. **Stop Loss:** Below the midpoint of the consolidation range (or the bottom, if the range is very tight).

### Short Entry (Bearish Breakdown)
1. **Context:** Price is in a downtrend (below EMA50).
2. **Consolidation & Dry-Up:** Tight range + shrinking volume.
3. **Trigger:** Candle closes **below** the consolidation support.
4. **Confirmation:** Volume spike > 2x average.
5. **Entry:** Go Short on breakout candle close.
6. **Stop Loss:** Above the midpoint of the consolidation range.

---

## Exit Rules

- **Target 1:** Distance equal to the height of the preceding impulse move (measured from breakout point). Take 50%.
- **Target 2:** Next major S/R level. Take remaining 50%.
- **Trailing Stop:** Move stop to break-even after T1. Trail below EMA9 or each new swing low.
- **Failure:** If price immediately reverses and closes back inside the range on high volume (Fakey) -> Exit.
- **Time Stop:** Close positions by 14:15.

---

## Filters

- [ ] **Crucial:** Ensure the volume during consolidation is genuinely low (drying up), not erratic.
- [ ] Skip if the breakout occurs on light volume (high chance of failure).
- [ ] Avoid trading breakouts right into a major higher-timeframe resistance level.
- [ ] Prefer setups that align with the daily trend direction.
- [ ] Do not trade in the final 30 minutes of the session.

---

## Risk Management

| Rule             | Guideline                                |
| ---------------- | ---------------------------------------- |
| Max Risk/Trade   | 1% of account equity                     |
| Stop Placement   | Midpoint or opposite edge of tight range |
| Min R:R          | 1:2                                      |
| Max Trades/Day   | 2-3                                      |
| Daily Loss Limit | -2%                                      |

---

## Edge & Statistics

- **Win rate:** 55-65% when volume expansion is strict (>2x).
- **R:R:** Often very high (1:3 or more) because the stop (tight range) is small relative to the breakout potential.
- Works exceptionally well in "boring" markets that suddenly wake up.

---

## Example Trade Log

```
Date:      2026-06-15
Symbol:    VNM (HSX)
Context:   Uptrend, then consolidates 09:30-11:00
Range:     66,000 - 66,500 (tight)
Volume:    Declined steadily, dropping to 30% of average.
Breakout:  11:05 candle closes at 66,800.
Vol Spike: 3.5x the consolidation average. ✓
Entry:     66,800 (Long)
Stop:      66,250 (Midpoint of range)
Target:    68,000 (Based on morning impulse)
Result:    Hit T1 at 67,500 (+700), T2 at 68,000 (+1,200). +WIN.
```

---

## Notes & Improvements
- This is fundamentally similar to the Bollinger Band Squeeze, but focuses strictly on price action and volume visually rather than indicator bands.
- You can scan for this by looking for stocks with historically low 60-minute volume that suddenly experience a 5-minute volume spike.

---
*Category: Volume-Based / Breakout | Timeframe: Intraday (5-min) | Market: VN30F / HSX Stocks*
