# 20 — Fakey / False Breakout Reversal

## Overview

A **Fakey** (False Breakout) occurs when price breaks beyond a key level — enticing breakout traders to enter — then immediately reverses back inside, trapping the late entrants. This is one of the most powerful intraday signals because it exploits the stops of both breakout traders (who get stopped out) and the trapped position holders, creating a cascade of forced selling/buying in the opposite direction.

---

## Concept

```
BULL FAKEY (Short signal):
  Price breaks ABOVE resistance → breakout traders enter Long
  Price reverses BACK BELOW resistance (within 1–3 candles)
  → Long traders stopped out → panic selling → fade Short

BEAR FAKEY (Long signal):
  Price breaks BELOW support → breakdown traders enter Short
  Price reverses BACK ABOVE support
  → Short sellers panic-buy → chase Long
```

The key insight: **every stop-loss order is a market order in disguise**. When a fakey triggers, a cascade of stop-loss orders floods the market in the opposite direction of the failed breakout.

---

## Setup & Entry Rules

| Parameter    | Value                                             |
|--------------|---------------------------------------------------|
| Timeframe    | 5-min chart (1-min for precise entry)             |
| Markets      | VN30F, liquid HSX stocks near key levels          |
| Session      | 09:15 – 13:30                                     |
| Level Types  | ORB High/Low, PDH/PDL, S/R, HOD/LOD              |

### Short Entry (Bull Fakey)
1. Price has a clear resistance level (at least 2 prior tests).
2. Price breaks above resistance — looks like a genuine breakout.
3. **Within 1–3 candles**: price closes BACK BELOW the resistance level.
4. The breakout candle has a long upper wick (rejection visible).
5. Volume on the rejection candle increases (confirms reversal pressure).
6. Enter Short on the close of the reversal candle (back below resistance).
7. Stop Loss: Above the fakey high (the false breakout high).

### Long Entry (Bear Fakey)
1. Clear support level with 2+ prior tests.
2. Price breaks below support.
3. Within 1–3 candles: price closes BACK ABOVE support.
4. Lower wick on rejection candle.
5. Volume confirms.
6. Enter Long on close back above support.
7. Stop Loss: Below the fakey low.

---

## Quality Criteria for High-Probability Fakey

| Criterion                                   | Score |
|---------------------------------------------|-------|
| Level tested 3+ times previously             | +3    |
| False breakout reverses within 1 candle      | +3    |
| Volume spikes on rejection (not just candle) | +2    |
| RSI at extreme on fake breakout candle       | +2    |
| Failed breakout at HOD/LOD or ORB level      | +2    |
| **Trade only if total score ≥ 8**            |       |

---

## Exit Rules

- **Target 1:** Midpoint of the prior consolidation range → close 50%.
- **Target 2:** Opposite S/R level → close 50%.
- **Speed:** Fakey trades move fast initially — capture the cascade quickly.
- **Trail:** Once target 1 hit, trail stop to break-even.
- **Failure:** If price immediately turns and breaks back through — accept the loss quickly.

---

## Filters

- [ ] The level must be well-established (not just 1 prior touch).
- [ ] Skip if the "false breakout" lasted more than 5 candles — may not be a fakey (could be absorption before continuation).
- [ ] Avoid on news-driven days — fundamentals can sustain a breakout.
- [ ] Skip if volume on the initial breakout candle was very low (no trapped buyers → weaker cascade).
- [ ] Confirm that there are no major S/R levels between entry and target.

---

## Risk Management

| Rule              | Guideline                         |
|-------------------|-----------------------------------|
| Max Risk/Trade    | 1% of account equity              |
| Stop Placement    | Beyond fakey high/low             |
| Min R:R           | 1:2 (cascade targets are wide)    |
| Max Trades/Day    | 3                                 |
| Daily Loss Limit  | −2%                               |

---

## Edge & Statistics

- Win rate: **55–65%** at well-tested levels.
- The edge comes from the **asymmetry of trapped positions** — many stops, fast move.
- Best on: Sessions with moderate volume and clear S/R levels.
- Worst on: Very thin sessions (low volume = no trapped positions).

---

## Example Trade Log

```
Date:         2026-06-21
Symbol:       VN30F2607
Resistance:   1,280 (tested 3× in prior 2 hours)
Fakey:        10:45 — price spikes to 1,282.5, closes back below 1,280 (1 candle)
Wick:         Obvious long upper wick on 5-min ✓
Volume:       High on rejection candle ✓
Entry:        1,279 (Short, close back below 1,280)
Stop:         1,284 (above fakey high)
T1:           1,273 (midrange) ← 50% closed at 11:00
T2:           1,268 (prior S/R) ← 50% closed at 11:20
Result:       +WIN, stops of trapped buyers fueled the move
```

---

## Notes & Improvements

- The **ORB Fakey** is particularly powerful: price breaks ORB level, immediately reverses → trade back inside ORB then to the opposite ORB level.
- Combine with **order flow**: if you can see large sell orders stacking above resistance before the fakey, conviction increases.
- **Fakey at HOD**: when price makes a new HOD then immediately reverses = very high short signal.
- Track fakey setups at each level type — some levels (round numbers, PDH) have higher fakey frequency.

---

*Category: Price Action / Reversal | Timeframe: Intraday (5-min) | Market: VN30F / HSX Stocks*
