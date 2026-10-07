# 06 — Momentum Continuation (Bull Flag / Bear Flag)

## Overview

After a strong impulsive move (the "flagpole"), price often consolidates in a tight, counter-trend channel before continuing in the original direction. This pause — the "flag" — represents institutions waiting to add to their positions. Trading the breakout of the flag in the direction of the original impulse captures the continuation move.

---

## Concept

```
BULL FLAG:                    BEAR FLAG:
    /‾‾\                          \__/
   /    \___  ← flag              /    \
  /          \                   /      \___
 / flagpole   \___              / flagpole
              ↓ BO                         ↓ BO
```

**Key Characteristics of a Valid Flag:**
- Flagpole: Sharp, high-volume move (3–8 candles minimum).
- Flag: Low-volume consolidation at 30–50% retracement of flagpole.
- Flag duration: 5–15 candles on 5-min chart (25–75 minutes).
- Breakout: Volume expands sharply, price breaks flag boundary.

---

## Setup & Entry Rules

| Parameter    | Value                                             |
|--------------|---------------------------------------------------|
| Timeframe    | 5-min for entry; also check 15-min for structure  |
| Markets      | VN30F, sector leaders on momentum days            |
| Session      | 09:30 – 12:00 (morning momentum runs)             |

### Bull Flag Long Entry
1. Identify a strong upward impulsive move (flagpole) with high volume.
2. Price consolidates in a downward-sloping or horizontal channel (flag).
3. Volume decreases during consolidation (confirms flag is valid).
4. **Entry trigger:** 5-min candle closes above the upper flag trendline.
5. Volume on breakout candle > 2× flag consolidation average.
6. Stop Loss: Below the midpoint of the flag or below the flag low.

### Bear Flag Short Entry
1. Identify a strong downward impulsive move (flagpole) with high volume.
2. Price consolidates in an upward-sloping or horizontal channel.
3. Volume decreases during consolidation.
4. **Entry trigger:** 5-min candle closes below the lower flag trendline.
5. Volume confirms.
6. Stop Loss: Above the midpoint of the flag or above the flag high.

---

## Flag Measurement & Targets

```
Flagpole Length = |Impulse High − Impulse Low|
Target = Breakout Point + Flagpole Length

Example:
  Flagpole: 1,250 → 1,268 = 18 pts
  Flag consolidation: 1,268 → 1,263 (retracement)
  Breakout: 1,266
  Target: 1,266 + 18 = 1,284
```

---

## Quality Checklist for Flag Setups

| Criterion                               | Required? |
|-----------------------------------------|-----------|
| Flagpole is 3%+ move in < 30 min        | Preferred |
| Consolidation is < 50% retracement      | Required  |
| Volume drops during flag                | Required  |
| Volume spikes on breakout               | Required  |
| Broader market trend aligned            | Preferred |
| Breakout from clean trendline           | Required  |

---

## Exit Rules

- **Target (T1):** 50–75% of flagpole length projection → close 60%.
- **Target (T2):** Full flagpole projection → close remaining 40%.
- **Trail Stop:** Move to break-even after T1 hit; trail below each higher low (bull) or above each lower high (bear).
- **Failure Signal:** If price closes back inside the flag after breakout → immediate exit (failed breakout).

---

## Risk Management

| Rule              | Guideline                      |
|-------------------|--------------------------------|
| Max Risk/Trade    | 1.25% of account equity        |
| Stop Placement    | Flag midpoint (tight) or low   |
| R:R Minimum       | 1:2 before taking the trade    |
| Max Flags/Day     | 3 flags maximum                |
| Daily Loss Limit  | −2.5% → stop trading           |

---

## Example Trade Log

```
Date:          2026-06-22
Symbol:        VN30F2607
Flagpole:      1,255 → 1,273 = +18 pts (09:00–09:25, surge volume)
Flag:          1,273 → 1,267, downsloping channel (09:25–09:55)
Volume Flag:   Low, declining ✓
Breakout:      1,269 close above upper flag line at 10:00
Entry:         1,269.5
Stop:          1,264 (flag midpoint)
T1:            1,278 (+8.5 pts) ← 60% closed at 10:15
T2:            1,287 (+17.5 pts) ← 40% closed at 10:45
Result:        +WIN, near full flagpole projection
```

---

## Notes & Improvements

- Best setups form after **opening drive** (09:00–09:30 flagpole, then 09:30–10:00 flag).
- Combine with **sector rotation scanner**: if entire sector is surging, individual stock flags have higher follow-through.
- **Pennants** (symmetrical triangle consolidation) are a variant with similar edge — include in scan.
- Backtest: filter for flagpoles where the impulse volume is >3× the 20-day average for best results.

---

*Category: Momentum Continuation | Timeframe: Intraday | Market: VN30F / HSX Stocks*
