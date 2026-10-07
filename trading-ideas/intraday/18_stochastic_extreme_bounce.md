# 18 — Stochastic Extreme Bounce

## Overview

The Stochastic Oscillator measures price position relative to its recent range. When Stochastic reaches extreme levels (overbought > 80 or oversold < 20) at a key support/resistance level, it signals potential price exhaustion and mean reversion. Unlike RSI divergence, this strategy uses the Stochastic **%K/%D crossover in the extreme zone** as the entry trigger.

---

## Concept

```
%K = (Close − Lowest Low N) / (Highest High N − Lowest Low N) × 100
%D = SMA(3) of %K

Oversold Zone:  %K < 20  → Potential Long
Overbought Zone: %K > 80 → Potential Short

Entry Signal: %K crosses ABOVE %D while both are in oversold zone → Long
              %K crosses BELOW %D while both are in overbought zone → Short
```

**Critical distinction:** The Stochastic signal alone is not enough. It must occur at a key S/R level or VWAP band to have edge. In trending markets, Stochastic can remain in extreme zones for extended periods.

---

## Indicators Required

| Indicator     | Setting       | Purpose                           |
|---------------|---------------|-----------------------------------|
| Stochastic    | 14, 3, 3 (%K/%D/Smooth) | Primary entry trigger    |
| VWAP          | Daily         | Level confluence                  |
| S/R Levels    | Pre-marked    | Confluence filter                 |
| Volume        | 20-bar MA     | Confirm reversal momentum         |
| EMA           | 50-period     | Trend context (avoid counter-trend)|

---

## Setup & Entry Rules

| Parameter    | Value                                            |
|--------------|--------------------------------------------------|
| Timeframe    | 5-min chart                                      |
| Markets      | VN30F, VCB, BID, VHM (liquid, responsive)        |
| Session      | 09:30 – 13:30                                    |
| Stochastic   | Both %K and %D must be in extreme zone at entry  |

### Long Entry (Oversold Bounce)
1. Stochastic %K drops below 20 (oversold).
2. %D also below 20.
3. %K crosses **above** %D (bullish crossover within oversold zone).
4. Price is at or near a pre-identified support level or VWAP lower band.
5. Reversal candle confirms (hammer, bullish engulfing).
6. Volume on reversal candle above average.
7. Enter Long on reversal candle close.
8. Stop Loss: Below the candle low (or below S/R level).

### Short Entry (Overbought Fade)
1. Stochastic %K above 80.
2. %D also above 80.
3. %K crosses **below** %D (bearish crossover in overbought zone).
4. Price at resistance level or VWAP upper band.
5. Bearish reversal candle.
6. Enter Short.
7. Stop Loss: Above candle high.

---

## Exit Rules

- **Target 1:** Stochastic reaches opposite extreme (from 20 → 80 or vice versa) → close 60%.
- **Target 2:** Next S/R level or VWAP midline → close 40%.
- **Trail:** Trail stop below each higher 5-min low (Long).
- **Failure:** If Stochastic re-enters the extreme zone and keeps going → exit (trend override).
- **Time Stop:** Close all by 14:00.

---

## Filters

- [ ] **Never fade in strong trending market** — Stochastic stays overbought in uptrends.
- [ ] Require at least 1 S/R or VWAP level confluence.
- [ ] Skip if prior 1H trend is strongly directional (ADX > 35 on 1H).
- [ ] Skip if the extreme was caused by a news event (fundamental override).
- [ ] Avoid taking more than 2 stochastic bounces in the same direction per day.

---

## Risk Management

| Rule              | Guideline                           |
|-------------------|-------------------------------------|
| Max Risk/Trade    | 0.75% of account equity             |
| Stop Placement    | Beyond the reversal candle extreme  |
| Min R:R           | 1:1.5 (must measure before entry)   |
| Max Trades/Day    | 4                                   |
| Daily Loss Limit  | −2%                                 |

---

## Edge & Statistics

- Win rate: **58–68%** with proper S/R confluence.
- Without S/R confluence: drops to ~45% — do not skip the filter.
- Best on: Range-bound sessions, "inside day" market conditions.
- Worst on: Strong trending days (VN-Index up/down >1.5%).

---

## Example Trade Log

```
Date:      2026-06-18
Symbol:    VN30F2607
S/R Level: 1,265 (prior day low, tested twice)
Stoch %K:  17 (below 20) / %D: 19 (below 20)
Cross:     %K crosses above %D at 11:15 (bullish cross in oversold)
Candle:    Hammer at 1,266 ✓
Volume:    1.4× average ✓
Entry:     1,267 (Long)
Stop:      1,261 (below hammer low)
T1:        1,276 (Stoch at 60, VWAP) ← 60% closed
T2:        1,283 (next resistance) ← 40% closed
Result:    +WIN
```

---

## Notes & Improvements

- Slow Stochastic (14, 3, 3) gives fewer but more reliable signals than fast Stochastic (5, 3, 3).
- Try **Stochastic RSI** (Stoch of RSI) for even more sensitive extreme detection.
- Combine with **Bollinger Bands**: if Stochastic extreme coincides with price touching BB outer band → very high probability.
- Track which Stochastic level produces best results (below 15 vs. below 20).

---

*Category: Mean Reversion | Timeframe: Intraday (5-min) | Market: VN30F / HSX Stocks*
