# 23 — Double Top / Double Bottom Intraday

## Overview

The **Double Top (M pattern)** and **Double Bottom (W pattern)** are among the most recognized reversal formations in technical analysis. Intraday, these patterns form within hours on the 5-min or 15-min chart and signal significant momentum shifts. When the neckline of the pattern is broken with volume, the measured move target is highly predictable.

---

## Concept

```
DOUBLE TOP (M Pattern — Bearish):
    /\    /\
   /  \  /  \   ← Two roughly equal highs (within 0.5%)
  /    \/    \
              \  ← Neckline breaks = Short entry
               ↓ Target = height of M

DOUBLE BOTTOM (W Pattern — Bullish):
              /↑ Target = height of W
  \    /\    /
   \  /  \  /   ← Two roughly equal lows (within 0.5%)
    \/    \/
         ↑ Neckline breaks = Long entry
```

**Critical measurement:**
```
Pattern Height = |First Top/Bottom − Neckline|
Target = Neckline − Height (Double Top)
         Neckline + Height (Double Bottom)
```

---

## Setup & Entry Rules

| Parameter    | Value                                             |
|--------------|---------------------------------------------------|
| Timeframe    | 5-min chart (pattern takes 30–90 minutes to form) |
| Markets      | VN30F, liquid HSX stocks                          |
| Session      | 09:30 – 13:00                                     |
| Equal Highs/Lows | Within 0.5% of each other                    |

### Long Entry (Double Bottom Neckline Break)
1. Two lows form at approximately the same price level (within 0.5%).
2. The second low has **lower volume** than the first (sellers exhausted).
3. A neckline is drawn at the peak between the two lows.
4. **Entry trigger:** 5-min candle closes above the neckline with high volume.
5. Enter Long on the breakout candle close.
6. Stop Loss: Below the second bottom (the lower of the two lows).
7. Target: Neckline + height of the W pattern.

### Short Entry (Double Top Neckline Break)
1. Two highs at approximately the same level.
2. Second high has lower volume than first.
3. Neckline drawn at trough between the two highs.
4. **Entry trigger:** 5-min candle closes below neckline with volume.
5. Enter Short.
6. Stop Loss: Above the higher of the two tops.
7. Target: Neckline − height.

---

## Pattern Validity Checklist

| Criterion                                    | Required? |
|----------------------------------------------|-----------|
| Two highs/lows within 0.5% of each other     | Required  |
| Time between peaks: 20 min – 3 hours         | Required  |
| Volume lower on second peak/trough           | Preferred |
| Clear neckline (not jagged)                  | Required  |
| RSI divergence between two peaks             | +Conviction|
| Neckline breaks with high volume             | Required  |

---

## Exit Rules

- **Target 1:** 50% of measured move → close 60%.
- **Target 2:** Full measured move → close 40%.
- **Retest:** After neckline break, price often retests the neckline (now S/R) → hold if it holds.
- **Trail:** After T1 hit, trail stop to break-even.
- **Failure:** Price closes back above neckline (for Short) → exit immediately.

---

## Filters

- [ ] Do not trade if the two peaks/troughs are less than 20 minutes apart (too fast = whipsaw).
- [ ] Skip if neckline coincides with VWAP (conflicting signals at break).
- [ ] Avoid during lunch hour (12:00–13:00) formation — low volume reduces reliability.
- [ ] If the second top/bottom significantly exceeds the first (by >1%), it's not a double top — it's a continuation.
- [ ] Do not trade the pattern if the overall trend strongly opposes (e.g., double bottom in a major downtrend).

---

## Risk Management

| Rule              | Guideline                        |
|-------------------|----------------------------------|
| Max Risk/Trade    | 1% of account equity             |
| Stop Placement    | Beyond 2nd extreme               |
| Min R:R           | 1:1.5 (measured move confirms)   |
| Max Trades/Day    | 2                                |
| Daily Loss Limit  | −2%                              |

---

## Edge & Statistics

- Win rate: **55–65%** on confirmed neckline breaks with volume.
- Measured move target achieved ~60% of the time.
- Best on: Clear trending sessions that reverse mid-day.
- Worst on: Very choppy days (multiple fake M/W patterns form).

---

## Example Trade Log

```
Date:         2026-06-10
Symbol:       VHM (HSX)
Top 1:        10:00 — 44,800
Top 2:        11:00 — 44,750 (≈ equal, lower volume) ✓
Neckline:     44,300 (trough between tops)
Height:       44,800 − 44,300 = 500 pts
RSI Div:      RSI 68 at top 1, RSI 61 at top 2 ✓
Neckline Break: 11:15, close below 44,300 with high volume
Entry:        44,250 (Short)
Stop:         44,900 (above higher of 2 tops)
T1:           44,050 (50% of 500 pts) ← 60% at 11:30
T2:           43,800 (full 500 pts) ← 40% at 12:00
Result:       +WIN
```

---

## Notes & Improvements

- **Triple tops/bottoms** are a more reliable variant — if 3 peaks/troughs at the same level before neckline break, even stronger signal.
- Use **candlestick patterns** at the second peak/trough for timing: a shooting star at 2nd top or hammer at 2nd bottom increases conviction.
- Combine with **RSI divergence**: if 2nd top comes with RSI lower high → near-certain reversal setup.
- Backtest measured move achievement rate across different M/W heights on VN30F.

---

*Category: Pattern Reversal | Timeframe: Intraday (5-min) | Market: VN30F / HSX Stocks*
