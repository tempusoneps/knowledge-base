# 16 — Rising / Falling Wedge Breakout

## Overview

A **Wedge** is a converging pattern where both the upper and lower trendlines slope in the same direction. A **Rising Wedge** slopes upward but signals distribution (bearish reversal) as buying momentum weakens. A **Falling Wedge** slopes downward but signals accumulation (bullish reversal) as selling pressure wanes. Wedges are powerful reversal patterns — the breakout is *against* the direction of the wedge.

---

## Concept

```
RISING WEDGE (Bearish Signal):          FALLING WEDGE (Bullish Signal):
    /‾‾/‾‾/‾‾  ← upper trendline            \__\__\  ← upper trendline
   /  /  /                                    \  \  \
  /  /  /  ← lower trendline (steeper)         \  \  \  ← lower trendline (steeper)
 /  /  /                                        \  \  \

Both lines slope UP but converge         Both lines slope DOWN but converge
→ Breakout DOWN (reversal short)         → Breakout UP (reversal long)
```

**Key insight:** In a rising wedge, higher highs are being made but on *declining volume* — momentum divergence signals the move is running out of fuel.

---

## Setup & Entry Rules

| Parameter    | Value                                            |
|--------------|--------------------------------------------------|
| Timeframe    | 5-min or 15-min chart                            |
| Markets      | VN30F, trending HSX stocks                       |
| Duration     | Wedge must have at least 5 candle touches (2+ on each trendline) |
| Session      | 09:30 – 13:00                                    |

### Short Entry (Rising Wedge Breakdown)
1. Identify a rising wedge: both upper and lower trendlines slope up and converge.
2. Volume decreases as wedge progresses (confirms weakening momentum).
3. RSI showing bearish divergence (price makes higher high, RSI doesn't).
4. **Entry trigger:** 5-min candle closes **below the lower trendline** of the wedge.
5. Volume spikes on the breakdown candle.
6. Stop Loss: Above the most recent wedge high.
7. Target: Measured from wedge start (height at widest point, subtracted from breakdown).

### Long Entry (Falling Wedge Breakout)
1. Identify a falling wedge: both trendlines slope down and converge.
2. Volume decreasing within wedge (accumulation).
3. RSI bullish divergence forming.
4. **Entry trigger:** 5-min candle closes **above upper trendline**.
5. Volume surge confirms.
6. Stop Loss: Below the most recent wedge low.
7. Target: Wedge height added to breakout point.

---

## Wedge Target Measurement

```
Wedge Height = Distance from the first candle (left-most) high to low
Target = Breakout Point + Wedge Height (for long)
         Breakout Point − Wedge Height (for short)

Example (Falling Wedge):
  Wedge start: High 1,290, Low 1,275 → Height 15 pts
  Breakout at: 1,268 (above upper trendline)
  Target: 1,268 + 15 = 1,283
```

---

## Exit Rules

- **Target 1:** 50% of measured move → close 60%.
- **Target 2:** Full measured move → close 40%.
- **Retest:** After breakout, price often retests the broken trendline → hold if it holds.
- **Failure:** Re-entry into wedge → immediate exit.
- **Time Stop:** Close before 14:00.

---

## Filters

- [ ] Volume must be declining within the wedge (minimum 3 consecutive lower-volume bars).
- [ ] RSI divergence is required for highest probability setups.
- [ ] Wedge must have at least 5 candle touches total (2 on each line minimum).
- [ ] Skip wedges forming during lunch session (12:00–13:00) — low volume, unreliable.
- [ ] Avoid trading rising wedge in strong bull market — market can override.

---

## Risk Management

| Rule              | Guideline                         |
|-------------------|-----------------------------------|
| Max Risk/Trade    | 1% of account equity              |
| Stop Placement    | Beyond last wedge swing extreme   |
| Min R:R           | 1:2                               |
| Max Trades/Day    | 2                                 |
| Daily Loss Limit  | −2%                               |

---

## Edge & Statistics

- Win rate: **55–60%** with confirmed volume divergence.
- Measured move achieved ~55% of the time.
- Best context: Rising wedge after extended uptrend, falling wedge after downtrend.
- Worse on: Range-bound market without clear prior trend.

---

## Example Trade Log

```
Date:         2026-06-14
Symbol:       VN30F2607
Pattern:      Rising wedge (09:15–10:30)
Wedge High:   1,282 (first bar) / Low: 1,273 → Height = 9 pts
Breakdown:    10:35, close below lower trendline at 1,275
Volume:       High, confirming breakdown ✓
RSI Div:      Price higher high but RSI lower high ✓
Entry:        1,274.5 (Short)
Stop:         1,280 (above last wedge high)
T1:           1,270 (50% of 9 pts) ← 60% at 10:50
T2:           1,265.5 (full 9 pts) ← 40% at 11:15
Result:       +WIN
```

---

## Notes & Improvements

- Combine wedge pattern with **MACD divergence** for dual indicator confirmation.
- Use **trendline drawing tools**: manually draw lines through at least 2 confirmed swing highs and 2 swing lows.
- Rising wedge at all-time high or multi-month high = particularly powerful reversal signal.
- Automate pattern detection using linear regression on swing highs/lows with Python.

---

*Category: Pattern Reversal | Timeframe: Intraday (5-min / 15-min) | Market: VN30F / HSX Stocks*
