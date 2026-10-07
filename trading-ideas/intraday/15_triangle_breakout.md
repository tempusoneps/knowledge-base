# 15 — Ascending / Descending Triangle Breakout

## Overview

Triangles are one of the most reliable classical chart patterns. An **Ascending Triangle** has a flat top resistance with rising lows — indicating buyers becoming more aggressive with each test. A **Descending Triangle** has a flat bottom support with lower highs — indicating sellers dominating. Both resolve with a high-probability breakout in the direction of the dominant pressure, typically with strong momentum.

---

## Concept

```
ASCENDING TRIANGLE (Bullish):
    ________________  ← flat resistance
   /    /    /
  /    /    /         ← rising lows (buyers more aggressive)
 /    /    /
       ↓ breakout UP

DESCENDING TRIANGLE (Bearish):
 \    \    \          ← lower highs (sellers more aggressive)
  \    \    \
   \________________  ← flat support
       ↓ breakout DOWN
```

**Key Measurement:** The height of the triangle at its widest point (left side) is the projected target after breakout.

---

## Setup & Entry Rules

| Parameter    | Value                                            |
|--------------|--------------------------------------------------|
| Timeframe    | 5-min or 15-min chart                            |
| Markets      | VN30F, liquid HSX stocks with clear price action |
| Session      | 09:30 – 13:00 (avoid late session triangles)     |
| Duration     | Triangle must span at least 30 minutes (6+ candles on 5-min) |

### Long Entry (Ascending Triangle Breakout)
1. Identify flat resistance level (2+ equal highs) and rising lows.
2. Triangle duration: at least 6 candles on 5-min (30+ min).
3. Volume decreases through the triangle (compression).
4. **Entry trigger:** 5-min candle closes **above flat resistance** with volume > 2× average.
5. Stop Loss: Below the last higher low within the triangle.
6. Target: Resistance + triangle height.

### Short Entry (Descending Triangle Breakdown)
1. Identify flat support and lower highs.
2. Compression forms as price narrows.
3. **Entry trigger:** 5-min candle closes **below flat support** with high volume.
4. Stop Loss: Above the last lower high within the triangle.
5. Target: Support − triangle height.

---

## Triangle Measurement

```
Triangle Height = Flat Level − (First swing high/low on left side)

Example (Ascending):
  Flat Resistance: 1,280
  First Low on left: 1,265
  Height: 15 pts
  Breakout at: 1,280
  Target: 1,280 + 15 = 1,295
```

---

## Exit Rules

- **Target 1:** 50% of measured move → close 60%.
- **Target 2:** Full measured move → close 40%.
- **Trail:** After T1, trail stop below each 5-min higher low.
- **Retest Entry:** Often price retests the breakout level — if it holds → re-enter.
- **Failure:** Price closes back inside triangle within 2 candles → exit immediately.

---

## Filters

- [ ] Minimum 4 touches of the flat level (2 at resistance for ascending, 2 at support for descending).
- [ ] Skip triangles lasting > 3 hours — too much time decay, pattern stales.
- [ ] Avoid if the flat level coincides with VWAP (conflicting signals).
- [ ] Skip near session close — breakout needs time to develop.
- [ ] Do not trade a triangle that forms after a major reversal (exhaustion pattern context).

---

## Risk Management

| Rule              | Guideline                      |
|-------------------|--------------------------------|
| Max Risk/Trade    | 1% of account equity           |
| Stop Placement    | Inside triangle (below last HL or above last LH) |
| Min R:R           | 1:2 (measured move target)     |
| Max Trades/Day    | 2                              |
| Daily Loss Limit  | −2%                            |

---

## Edge & Statistics

- Win rate: **55–65%** for ascending/descending triangles.
- Measured move target achieved ~60% of the time on confirmed breakouts.
- Best on: Stock-specific catalysts (earnings, sector news driving the pattern).
- Worst on: Broad market choppy days (triangles form everywhere, most fail).

---

## Example Trade Log

```
Date:         2026-06-17
Symbol:       HPG (HSX)
Flat Top:     27,500 (tested at 09:30, 10:00, 10:30)
Rising Lows:  27,100 → 27,200 → 27,300 (ascending)
Height:       27,500 − 27,100 = 400 pts
Breakout:     10:45, closes above 27,500 at high volume
Entry:        27,550 (Long)
Stop:         27,280 (below last higher low)
T1:           27,750 (+200 pts) ← 60% closed at 11:00
T2:           27,950 (+400 pts) ← 40% closed at 11:30
Result:       +WIN
```

---

## Notes & Improvements

- Add **symmetrical triangle** as a neutral variant (wait for breakout direction).
- Scan for triangles forming on stocks near **52-week highs** — ascending triangles there have stronger breakout statistics.
- Use Python with `scipy` convex hull or trendline fitting to automate triangle detection.
- Track "time in triangle" vs. "post-breakout move" relationship to find optimal entry timing.

---

*Category: Pattern Breakout | Timeframe: Intraday (5-min / 15-min) | Market: VN30F / HSX Stocks*
