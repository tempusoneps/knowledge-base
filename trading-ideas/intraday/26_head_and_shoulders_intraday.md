# 26 — Head and Shoulders Intraday

## Overview

The **Head and Shoulders (H&S)** is a classic reversal pattern consisting of three peaks — a higher middle peak (head) flanked by two lower peaks (shoulders). The **Inverse H&S** is its mirror image and signals bullish reversals. Both patterns complete when the **neckline** is broken with volume, triggering a measured move equal to the height of the head above the neckline.

---

## Concept

```
HEAD & SHOULDERS (Bearish):
     /\
    /  \
   /    \    /\
  /  LS  \  /  \  RS
 /        \/    \
          NL-----\ ← Neckline break = Short entry
                  ↓ Target = Head height below neckline

LS = Left Shoulder, H = Head, RS = Right Shoulder, NL = Neckline

INVERSE H&S (Bullish):
          /↑ Target = Head height above neckline
 /\      /  NL----
/  \  /\/  ↑ Neckline break = Long entry
    \/  RS
    LS    H (deepest point)
```

---

## Setup & Entry Rules

| Parameter      | Value                                          |
|----------------|------------------------------------------------|
| Timeframe      | 5-min or 15-min chart                          |
| Markets        | VN30F, liquid HSX stocks                       |
| Session        | 09:15 – 13:00 (needs time for full pattern)    |
| Pattern Duration | 45 min – 3 hours (shorter patterns less reliable) |

### Short Entry (H&S Neckline Break)
1. Identify Left Shoulder, Head (higher than LS), Right Shoulder (≈ LS height).
2. Draw neckline connecting the troughs between LS-Head and Head-RS.
3. RS forms on lower volume than Head (distribution ending).
4. **Entry trigger:** 5-min candle closes **below neckline** with high volume.
5. Enter Short at neckline close or on a pullback retest.
6. Stop Loss: Above the Right Shoulder high.
7. Target: Neckline − Head Height.

### Long Entry (Inverse H&S Neckline Break)
1. Identify pattern: left trough, deeper head trough, right trough (≈ left depth).
2. Neckline at the peaks between troughs.
3. Right trough on lower volume (exhaustion).
4. **Entry trigger:** Close above neckline with volume.
5. Enter Long.
6. Stop: Below Right Shoulder low.
7. Target: Neckline + Head Height.

---

## Pattern Measurement

```
Head Height = |Head peak/trough − Neckline|
Target = Neckline − Head Height (H&S Short)
         Neckline + Head Height (Inv. H&S Long)

Example (H&S):
  Head top: 1,290
  Neckline: 1,275
  Head Height: 15 pts
  Target: 1,275 − 15 = 1,260
```

---

## Neckline Types

| Neckline Slope | Interpretation                          |
|----------------|-----------------------------------------|
| Flat           | Most reliable, clean break              |
| Slightly up    | H&S slightly weaker (rising neckline)   |
| Strongly up    | Avoid — pattern reliability decreases   |
| Slightly down  | Inv. H&S slightly weaker                |

---

## Exit Rules

- **Target 1:** 50% of measured move → close 60%.
- **Target 2:** Full measured move → close 40%.
- **Retest play:** If price retests the neckline from below (H&S) or above (Inv. H&S) and holds → add to position.
- **Failure:** Price closes back above neckline after break → exit immediately.
- **Time Stop:** Close before 14:00.

---

## Filters

- [ ] Shoulders should be roughly symmetrical (within 0.5% of each other in height).
- [ ] Volume on Head > Volume on Right Shoulder (distribution/accumulation visible).
- [ ] Volume should spike on neckline breakout.
- [ ] Skip if the neckline is sloping too steeply (unreliable break).
- [ ] Do not trade if H&S pattern is very small (< 0.5% head height — target too narrow).

---

## Risk Management

| Rule              | Guideline                        |
|-------------------|----------------------------------|
| Max Risk/Trade    | 1% of account equity             |
| Stop Placement    | Beyond Right Shoulder extreme    |
| Min R:R           | 1:1.5 (measured move target)     |
| Max Trades/Day    | 2                                |
| Daily Loss Limit  | −2%                              |

---

## Edge & Statistics

- Win rate: **55–65%** on confirmed neckline breaks.
- Measured move achieved: ~60% of the time.
- The **retest entry** (entering on neckline retest) has higher win rate (~70%) but occurs only ~40% of the time.
- Best on: After a sustained trend when exhaustion is visible.

---

## Example Trade Log

```
Date:         2026-06-05
Symbol:       VN30F2607
Left Shoulder: 09:30 — peak 1,282
Head:          10:00 — peak 1,290
Right Shoulder: 10:45 — peak 1,283 (lower volume ✓)
Neckline:     1,274 (connecting troughs)
Break:        11:00 — 5-min close below 1,274 with volume spike
Head Height:  1,290 − 1,274 = 16 pts
Entry:        1,273 (Short)
Stop:         1,285 (above RS)
T1:           1,266 (50% of 16) ← 60% at 11:20
T2:           1,258 (full target) ← 40% at 12:00
Result:       +WIN
```

---

## Notes & Improvements

- Complex H&S (with multiple left/right shoulders) are more powerful but harder to trade.
- The **neckline retest** after break is the highest probability entry — be patient for it.
- Combine with **RSI divergence**: if RSI makes lower high on H&S right shoulder = double confirmation.
- H&S patterns on **daily chart** informing intraday bias: if daily H&S neckline is just above today's price, short bias all day.

---

*Category: Pattern Reversal | Timeframe: Intraday (5-min / 15-min) | Market: VN30F / HSX Stocks*
