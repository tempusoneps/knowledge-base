# 29 — Anchored VWAP Deviation Trade

## Overview

While the standard daily VWAP resets at market open, an **Anchored VWAP (AVWAP)** is calculated from a significant price event — a major swing high, swing low, gap, or earnings release. Anchored VWAP acts as a dynamic support/resistance level that reflects the "average cost" for all participants who entered since that anchor point. Deviations from AVWAP and subsequent returns offer systematic mean-reversion opportunities.

---

## Concept

```
Standard VWAP:  Resets daily at open (only intraday context)
Anchored VWAP:  Starts calculation from user-selected anchor point
                Persists across multiple sessions
                Tracks cumulative fair value since the anchor

Common Anchor Points:
  - Prior swing high or low
  - Gap open day
  - Major news event date
  - Weekly or monthly open
  - IPO price or major breakout date

Formula:
  AVWAP(t) = Σ(Price × Volume from anchor to t) / Σ(Volume from anchor to t)
```

**Deviation Bands:** Use Standard Deviation bands around AVWAP (±1σ, ±2σ) for entry signals.

---

## Indicators Required

| Indicator      | Setting                  | Purpose                          |
|----------------|--------------------------|----------------------------------|
| Anchored VWAP  | From prior swing extreme | Dynamic fair value reference     |
| AVWAP ±1σ      | 1 StdDev from AVWAP      | Normal deviation zone            |
| AVWAP ±2σ      | 2 StdDev from AVWAP      | Extreme deviation entry zone     |
| Volume         | 20-bar MA                | Confirm reversion momentum       |
| RSI            | 14-period                | Extreme level confirmation       |

---

## Setup & Entry Rules

| Parameter    | Value                                              |
|--------------|----------------------------------------------------|
| Timeframe    | 5-min or 15-min chart                              |
| Markets      | VN30F, any liquid HSX stock                        |
| Session      | 09:15 – 13:30                                      |
| Anchor       | Most recent significant swing high/low (3–10 days) |

### Long Entry (Below AVWAP, −2σ Bounce)
1. Set AVWAP anchor at the most recent significant swing low (past 5–10 sessions).
2. Price deviates to AVWAP −2σ band intraday.
3. Reversal candle forms at the −2σ level (hammer, bullish engulfing).
4. RSI < 35.
5. Volume decreasing on the pullback (no aggressive selling).
6. Enter Long on reversal candle close.
7. Stop Loss: Below −2σ by 1 ATR.

### Short Entry (Above AVWAP, +2σ Fade)
1. AVWAP anchor at recent significant swing high.
2. Price extends to AVWAP +2σ.
3. Bearish reversal candle.
4. RSI > 65.
5. Enter Short.
6. Stop: Above +2σ by 1 ATR.

---

## Anchor Selection Guide

| Anchor Type                    | Strength of AVWAP Level |
|--------------------------------|------------------------|
| Major swing low (3–5 sessions ago) | ★★★★★              |
| Weekly open                    | ★★★★                   |
| Gap close date                 | ★★★★                   |
| IPO / listing date             | ★★★                    |
| Daily VWAP (standard)          | ★★★                    |
| Monthly open                   | ★★★★★                  |

---

## Exit Rules

- **Target 1:** AVWAP midline (the anchored VWAP line itself) → close 70%.
- **Target 2:** AVWAP +1σ (for long from −2σ) → close 30%.
- **Trail:** Move stop to break-even after T1.
- **Failure:** If price closes through the entry deviation band in the wrong direction → exit.
- **Time Stop:** Close before 14:15.

---

## Filters

- [ ] Anchor must be a **meaningful** price event (not just any random candle).
- [ ] Skip if AVWAP bands are very narrow (< 0.3% width) — insufficient deviation to trade.
- [ ] Avoid if multiple conflicting AVWAPs are at the same level (confused signals).
- [ ] Skip during first 15 min of session (AVWAP not yet meaningful today).
- [ ] Do not trade AVWAP deviation when there is a strong fundamental catalyst driving price away.

---

## Risk Management

| Rule              | Guideline                          |
|-------------------|------------------------------------|
| Max Risk/Trade    | 1% of account equity               |
| Stop Placement    | 1 ATR beyond the deviation band    |
| Min R:R           | 1:1.5 (AVWAP target distance)      |
| Max Trades/Day    | 3 AVWAP setups                     |
| Daily Loss Limit  | −2%                                |

---

## Edge & Statistics

- Win rate: **60–70%** with proper anchor selection.
- Superior to daily VWAP for multi-day momentum situations.
- Best on: Stocks recovering from a significant sell-off (anchor at the low).
- Worst on: Strong trending stocks breaking away from AVWAP permanently.

---

## Example Trade Log

```
Date:         2026-06-20
Symbol:       VHM (HSX)
Anchor:       2026-06-10 swing low (44,000) — major support retest 10 days ago
AVWAP:        45,200 today
AVWAP −2σ:    44,300
Price Action: Pulls back to 44,350 (near −2σ) at 10:00
RSI:          32 ✓
Candle:       Bullish engulfing at 44,300 ✓
Entry:        44,400 (Long)
Stop:         43,900 (below −2σ)
T1:           45,200 (AVWAP) ← 70% at 11:15
T2:           45,750 (AVWAP +1σ) ← 30% at 12:30
Result:       +WIN
```

---

## Notes & Improvements

- Combine with **standard daily VWAP**: if AVWAP and daily VWAP coincide at the same level → very strong S/R confluence.
- Use **weekly AVWAP** (anchored at Monday's open) as a medium-term guide.
- Stack multiple AVWAPs: if 3 different anchors all point to the same price level → highest conviction long/short area.
- Build a Python tool to auto-calculate AVWAP from any anchor date using historical OHLCV + volume data.

---

*Category: Mean Reversion | Timeframe: Intraday (5-min / 15-min) | Market: VN30F / HSX Stocks*
