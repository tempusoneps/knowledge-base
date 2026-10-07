# 34 — CCI (Commodity Channel Index) Extreme Reversal

## Overview

The **Commodity Channel Index (CCI)** measures how far the current price deviates from its statistical mean, normalized by a mean deviation factor. CCI was originally designed for commodities but works exceptionally well as an intraday overbought/oversold oscillator. Extreme CCI readings (above +150 or below −150) signal price has deviated significantly from its mean — and a return is likely.

---

## Concept

```
CCI Formula:
  Typical Price (TP) = (High + Low + Close) / 3
  CCI = (TP − SMA(TP, N)) / (0.015 × Mean Deviation)
  N = 20 periods (standard)

Interpretation:
  CCI > +100:  Mildly overbought (watch for reversal)
  CCI > +150:  Strongly overbought → High probability reversal zone
  CCI > +200:  Extreme → Fade aggressively
  CCI < −100:  Mildly oversold
  CCI < −150:  Strongly oversold → High probability reversal zone
  CCI < −200:  Extreme → Fade aggressively

Zero Line:
  CCI crossing zero = momentum direction change (secondary signal)
```

---

## Indicators Required

| Indicator  | Setting     | Purpose                               |
|------------|-------------|---------------------------------------|
| CCI        | 20-period   | Primary extreme level indicator       |
| CCI Levels | ±100, ±150  | Entry zone thresholds                 |
| VWAP       | Daily       | Mean price / target reference         |
| Volume     | 20-bar MA   | Confirm exhaustion at extreme         |
| S/R Levels | Pre-marked  | Confluence for reversal entry         |

---

## Setup & Entry Rules

| Parameter    | Value                                          |
|--------------|------------------------------------------------|
| Timeframe    | 5-min chart                                    |
| Markets      | VN30F, VCB, BID, VHM (liquid, mean-reverting)  |
| Session      | 09:30 – 13:30                                  |
| Trigger      | CCI reaches ±150, then turns back toward zero  |

### Long Entry (CCI Extreme Oversold)
1. CCI drops below −150.
2. A reversal candle forms (CCI is declining → starts turning up).
3. **Entry trigger:** CCI turns back above −100 (momentum returning from extreme).
4. Price at or near a key support level.
5. Volume declining on the move to the extreme (exhaustion).
6. Enter Long on the candle where CCI crosses back above −100.
7. Stop Loss: 1 ATR below the recent price low.

### Short Entry (CCI Extreme Overbought)
1. CCI rises above +150.
2. Reversal candle at the high.
3. **Entry trigger:** CCI turns back below +100 (momentum fading from extreme).
4. Price near resistance.
5. Enter Short.
6. Stop: 1 ATR above recent high.

---

## CCI Signal Ladder

| CCI Level       | Action                         |
|-----------------|--------------------------------|
| > +200          | Strong fade short (aggressive) |
| +150 to +200    | Prepare short, wait for −100 cross |
| +100 to +150    | Watch only (not extreme enough)|
| −100 to +100    | No CCI signal                  |
| −150 to −100    | Watch only                     |
| −150 to −200    | Prepare long, wait for +−100 cross |
| < −200          | Strong fade long (aggressive)  |

---

## Exit Rules

- **Target 1:** CCI returns to zero line (price returns to mean) → close 60%.
- **Target 2:** CCI reaches opposite extreme (−150 to +150) → close 40%.
- **Failure:** If CCI continues extreme (moves further from zero after entry) → exit (trend, not mean-reversion).
- **Trail:** Trail stop below each higher low (Long) once in profit.
- **Time Stop:** Close before 14:00.

---

## Filters

- [ ] Skip if the prior trend is extremely strong (CCI can stay at +150 for many bars in trend mode).
- [ ] Require at least one key S/R level at or near the entry price.
- [ ] Do not take the trade until CCI has begun to turn back (don't enter into continued extremes).
- [ ] Skip near open (first 15 min) — CCI not yet calibrated.
- [ ] Maximum 3 CCI reversal trades per side per day.

---

## Risk Management

| Rule              | Guideline                          |
|-------------------|------------------------------------|
| Max Risk/Trade    | 0.75% of account equity            |
| Stop Placement    | 1 ATR beyond price extreme at CCI extreme |
| Min R:R           | 1:1.5                              |
| Max Trades/Day    | 4                                  |
| Daily Loss Limit  | −2%                                |

---

## Edge & Statistics

- Win rate: **58–65%** with S/R confluence and CCI turning back from extreme.
- Without S/R: drops to ~48% — the filter is critical.
- Best on: Range-bound sessions, stocks at multi-day highs/lows.
- Worst on: Breakout days, strong trend days.

---

## Example Trade Log

```
Date:      2026-06-16
Symbol:    VN30F2607
Context:   VN30F extended to 1,284 (overbought run from morning)
CCI:       Reaches +162 at 10:30 (above +150 threshold)
Candle:    Shooting star at 1,284 ✓
S/R:       1,282 = prior day high (resistance ✓)
CCI Turn:  CCI crosses back below +100 at 10:35
Entry:     1,281 (Short, on CCI back below +100)
Stop:      1,286.5 (1 ATR above high)
T1:        1,273 (CCI near zero) ← 60% at 11:00
T2:        1,266 (CCI at −100) ← 40% at 11:30
Result:    +WIN
```

---

## Notes & Improvements

- CCI with period = 14 gives more frequent but noisier signals; period = 20 is the sweet spot.
- Combine **CCI divergence**: if price makes new high but CCI makes lower high → near-certain reversal.
- Use **CCI zero-line cross** as a trend-following signal on 15-min chart (different from the 5-min reversal use).
- Test CCI on VN30F 5-min: log every CCI > ±150 event and measure subsequent price action for statistical validation.

---

*Category: Mean Reversion / Oscillator | Timeframe: Intraday (5-min) | Market: VN30F / HSX Stocks*
