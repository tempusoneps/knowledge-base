# 09 — High-of-Day / Low-of-Day Breakout (HOD/LOD)

## Overview

As price forms and accumulates near the High-of-Day or Low-of-Day during the intraday session, a breakout to a new HOD/LOD often triggers a momentum surge — institutional algorithms with stop orders, retail FOMO buyers, and momentum-chasing algos all pile in simultaneously. This strategy captures that surge by entering as a new HOD/LOD is being made.

---

## Concept

```
HOD (High of Day): Highest price reached so far in the current session
LOD (Low of Day):  Lowest price reached so far in the current session

HOD Breakout: Price clears the HOD → Long (momentum surge)
LOD Breakdown: Price breaks the LOD → Short (panic cascade)
```

**Why it works:**
- Stop-loss orders cluster just above HOD (short sellers' stops).
- Breakout triggers a stop cascade and FOMO buying simultaneously.
- Institutions with TWAP/VWAP algos become more aggressive at new highs.

---

## Setup & Entry Rules

| Parameter    | Value                                                |
|--------------|------------------------------------------------------|
| Timeframe    | 1-min chart for precise entry; 5-min for context     |
| Markets      | VN30F, top momentum movers of the day                |
| Best Session | 09:30–11:00 (morning run) and 13:00–14:00 (afternoon)|
| HOD/LOD Age  | Must be at least 45 minutes old (not just the open)  |

### Long Entry (HOD Breakout)
1. Identify the current HOD (highest price since open).
2. HOD must be at least 45 minutes old (has been tested and held).
3. Price approaches HOD for the **2nd or 3rd time** (building pressure).
4. Watch for a **tight consolidation just below HOD** (< 0.3% below HOD) for 5–10 minutes.
5. **Entry trigger:** A 1-min candle closes **above the HOD** with expanding volume.
6. Stop Loss: Below the consolidation low (or below HOD − 0.5%).

### Short Entry (LOD Breakdown)
1. Identify the current LOD.
2. LOD must be at least 45 minutes old.
3. Price tests LOD for the 2nd or 3rd time.
4. Tight consolidation just above LOD.
5. **Entry trigger:** 1-min candle closes below the LOD with volume surge.
6. Stop Loss: Above the consolidation high (or above LOD + 0.5%).

---

## HOD Setup Quality Criteria

| Criterion                                          | Score |
|----------------------------------------------------|-------|
| HOD held for > 1 hour before breakout              | +3    |
| 2nd test of HOD (not first approach)               | +2    |
| 3rd test of HOD (multiple failed attempts → coil)  | +3    |
| Consolidation below HOD is tight (< 0.2%)          | +2    |
| Volume declining into HOD (dry-up = breakout ready)| +2    |
| Market-wide momentum aligns (VN30 also pushing up) | +2    |
| **Minimum score to trade: 8**                      |       |

---

## Exit Rules

- **Scalp Target (T1):** +0.5% from entry → close 50% of position quickly.
- **Momentum Target (T2):** +1–1.5% from entry (let the momentum run) → close 40%.
- **Runner (10%):** Trail with a 1-min trailing stop until momentum dies.
- **Hard Stop:** If price falls back below HOD (breakout failure) → exit immediately, no questions.
- **Time Stop:** Do not hold HOD/LOD breakouts past 14:00.

---

## Failed Breakout Management

A **failed HOD breakout** (price breaks HOD then immediately reverses back below) is itself a powerful **Short signal**:

```
Scenario: HOD Breakout Failure
1. Price breaks HOD → you enter Long
2. Price immediately reverses back below HOD (within 2-3 candles)
3. FLIP: Exit Long, Enter Short (trapped buyers now selling)
4. Target: VWAP or prior consolidation base
```

This reversal of a failed HOD breakout often produces 1–2% downside moves quickly.

---

## Risk Management

| Rule              | Guideline                          |
|-------------------|------------------------------------|
| Max Risk/Trade    | 0.75% of account equity            |
| Stop Placement    | Below consolidation or HOD − 0.5%  |
| Min R:R           | 1:1.5 minimum                      |
| Max Trades/Day    | 3 HOD/LOD breakouts max            |
| Re-entry          | 1 re-entry allowed if stop was tight|
| Daily Loss Limit  | −2% → stop trading                 |

---

## Intraday Momentum Scanner Criteria

Pre-session and intraday scanner to find HOD/LOD candidates:

```
Filter:
  - Volume > 150% of 20-day average volume
  - Price move > 1% from open
  - Consolidating within 0.3% of intraday HOD or LOD
  - Time: After 09:45 (allow range to establish)
```

---

## Example Trade Log

```
Date:         2026-06-19
Symbol:       VHM (HSX)
HOD:          44,500 (set at 09:10, held for 90 min)
HOD Tests:    2nd test at 10:35, 3rd test at 10:50 (quality: high)
Consolidation: 10:50–11:05, tight range 44,400–44,500
Entry:        44,550 (1-min close above HOD at 11:06, volume 2.3×)
Stop:         44,350 (below consolidation base)
T1:           44,800 (+250 pts, +0.56%) ← 50% at 11:15
T2:           45,200 (+650 pts, +1.46%) ← 40% at 11:40
Runner:       Trailed, stopped out at 45,100 (10% of original size)
Result:       +WIN
```

---

## Notes & Improvements

- **Pairs well with ORB:** If HOD = ORB High, a later HOD breakout above it is a very powerful dual-confirmation setup.
- Track which stocks are the **"biggest movers of the day"** (momentum leaders) — HOD/LOD breakouts on leading stocks have higher follow-through.
- Consider **time of day**: HOD/LOD breakouts after 13:00 in quiet sessions can be traps — volume is low, moves are easily reversed.

---

*Category: Momentum Breakout | Timeframe: Intraday (1-min + 5-min) | Market: VN30F / HSX Stocks*
