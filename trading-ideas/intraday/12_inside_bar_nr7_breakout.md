# 12 — Inside Bar / NR7 Breakout

## Overview

An **Inside Bar** is a candle whose high and low are completely contained within the previous candle's range, signaling a temporary pause in momentum and a compression of volatility. The **NR7** (Narrowest Range of 7 bars) is an extreme version where the current bar has the smallest range of the past 7 bars. Both patterns act as coiled springs before a directional breakout.

---

## Concept

```
Inside Bar:
  Current High  < Previous High
  Current Low   > Previous Low
  → Volatility compression → Breakout pending

NR7:
  Current Range = smallest of last 7 bars
  → Extreme compression → High-probability directional move
```

The longer and tighter the compression, the stronger the subsequent breakout. Inside bars after a strong trending move are particularly powerful as they represent brief institutional consolidation.

---

## Setup & Entry Rules

| Parameter    | Value                                          |
|--------------|------------------------------------------------|
| Timeframe    | 15-min chart (NR7 more reliable on 15-min+)    |
| Markets      | VN30F, any liquid HSX stock                    |
| Session      | 09:15 – 13:30                                  |
| Trigger      | Breakout above Mother Bar High or below Low    |

### Long Entry (Bullish Breakout)
1. Identify an Inside Bar or NR7 bar on the 15-min chart.
2. Price breaks above the **Mother Bar High** (the bar containing the inside bar).
3. Volume on breakout candle > 1.5× average.
4. Prior trend is bullish (EMA50 upsloping preferred).
5. Enter Long at the Mother Bar High + 0.1% (confirmed breakout).
6. Stop Loss: Below the Inside Bar Low or Mother Bar Low.

### Short Entry (Bearish Breakdown)
1. Inside Bar or NR7 forms.
2. Price breaks below the **Mother Bar Low**.
3. Volume confirms.
4. Prior trend is bearish.
5. Enter Short at Mother Bar Low − 0.1%.
6. Stop Loss: Above Inside Bar High or Mother Bar High.

---

## Exit Rules

- **Target 1:** 1× Mother Bar range from breakout point → close 60%.
- **Target 2:** 2× Mother Bar range → close 40%.
- **Trail:** Trail stop below/above each new 5-min swing low/high.
- **Failure:** If price re-enters the Inside Bar range after breakout → exit.
- **Time Stop:** Close before 14:00.

---

## Filters

- [ ] Skip if Mother Bar is abnormally large (>2% range) — stop too wide.
- [ ] Skip in extreme news/earnings driven sessions.
- [ ] Do not trade inside bars within a prolonged range (multiple consecutive inside bars = choppy).
- [ ] Prefer inside bars that form after a clear impulse move (trend day context).
- [ ] Check volume on Mother Bar: should be higher than the Inside Bar volume.

---

## Risk Management

| Rule              | Guideline                      |
|-------------------|--------------------------------|
| Max Risk/Trade    | 1% of account equity           |
| Stop Placement    | Below/above Inside Bar extreme |
| Min R:R           | 1:1.5                          |
| Max Trades/Day    | 3                              |
| Daily Loss Limit  | −2%                            |

---

## Edge & Statistics

- Win rate: **50–58%** — the edge comes from R:R not win rate.
- NR7 patterns have statistically larger post-pattern moves than random bars.
- Best on: Quiet sessions followed by sudden directional news/flow.
- Worst on: Already-extended trends late in session.

---

## Example Trade Log

```
Date:         2026-06-23
Symbol:       FPT (HSX)
Mother Bar:   14:00–15:00 candle, High 125,000 / Low 123,500 (NR7)
Inside Bar:   Forms at 09:15 on next day
Breakout:     09:30, closes above 125,000
Volume:       2.1× average ✓
Entry:        125,200 (Long)
Stop:         123,400 (below Inside Bar Low)
T1:           126,700 (+1,500) ← 60% closed
T2:           128,200 (+3,000) ← 40% closed
Result:       +WIN
```

---

## Notes & Improvements

- Track consecutive inside bars: **2+ inside bars** in a row = stronger compression → larger move.
- Use **daily NR7** as a pre-market filter: if yesterday was a daily NR7, today likely has a strong directional bias.
- Pair with **opening gap**: NR7 day followed by a gap open is a powerful setup.
- Backtest NR7 on VN30F daily data to find best follow-through day statistics.

---

*Category: Volatility Breakout | Timeframe: Intraday (15-min) | Market: VN30F / HSX Stocks*
