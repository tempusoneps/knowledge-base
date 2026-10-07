# 08 — Intraday RSI Divergence Reversal

## Overview

RSI Divergence occurs when price makes a new high (or low) but the RSI indicator fails to confirm it — printing a lower high (or higher low) instead. This divergence signals weakening momentum and often precedes a price reversal. Combined with key S/R levels or VWAP, RSI divergence becomes one of the highest-conviction intraday reversal signals.

---

## Concept

```
BEARISH DIVERGENCE:
  Price: Higher High (HH) ──────────── New High
  RSI:   Lower High (LH) ──────────── Fails to confirm
  → Momentum weakening → Reversal Short

BULLISH DIVERGENCE:
  Price: Lower Low (LL) ──────────── New Low
  RSI:   Higher Low (HL) ──────────── Fails to confirm
  → Momentum exhausted → Reversal Long
```

**Types of Divergence:**

| Type               | Description                                    | Reliability |
|--------------------|------------------------------------------------|-------------|
| Regular Divergence | Price new extreme, RSI fails to confirm        | ★★★★★       |
| Hidden Divergence  | RSI new extreme, price fails to confirm        | ★★★         |
| Extended Divergence | Multiple failed confirmations over time       | ★★★★        |

---

## Indicators Required

| Indicator | Setting         | Purpose                          |
|-----------|-----------------|----------------------------------|
| RSI       | 14-period       | Primary divergence indicator     |
| RSI Levels| 70 overbought, 30 oversold | Filter zone          |
| VWAP      | Daily reset     | Level confluence                 |
| Volume    | 20-bar MA       | Confirmation                     |

---

## Setup & Entry Rules

| Parameter    | Value                                              |
|--------------|----------------------------------------------------|
| Timeframe    | 5-min for detection; confirm on 15-min             |
| Markets      | VN30F, liquid HSX stocks                           |
| Best Session | 10:00 – 13:30 (avoid volatile open)                |

### Long Entry (Bullish Regular Divergence)
1. Price makes a **Lower Low** on the chart (new intraday low).
2. RSI makes a **Higher Low** (RSI fails to confirm, divergence confirmed).
3. RSI must be below 40 on both lows (oversold zone preferred).
4. Convergence with support level or VWAP band increases conviction.
5. **Entry:** Buy on close of the candle that completes the higher RSI low, or on the next candle open.
6. **Stop Loss:** Below the new price low (the 2nd low point).

### Short Entry (Bearish Regular Divergence)
1. Price makes a **Higher High** on the chart (new intraday high).
2. RSI makes a **Lower High** (RSI diverges, weakening momentum).
3. RSI must be above 60 on both highs (overbought zone preferred).
4. Convergence with resistance level or VWAP upper band.
5. **Entry:** Sell on close of candle completing the lower RSI high.
6. **Stop Loss:** Above the new price high.

---

## Divergence Confirmation Checklist

- [ ] Two clear price pivots visible (not just 1 candle apart — needs swing structure).
- [ ] RSI clearly diverging (obvious visual slope difference).
- [ ] RSI in extreme zone (> 65 for bearish, < 35 for bullish).
- [ ] Reversal candlestick at the 2nd pivot (hammer, engulfing, pin bar).
- [ ] Volume declining on 2nd price extreme (confirming exhaustion).
- [ ] At least 1 key S/R level or VWAP nearby for confluence.

---

## Exit Rules

- **Target 1:** Swing midpoint between the two pivots (50% position).
- **Target 2:** Opposite S/R level or VWAP (50% position).
- **Trail Stop:** Move stop to break-even after T1 hit.
- **Invalidation:** If price closes beyond the stop before entry is triggered → cancel setup.
- **Time Stop:** Close all divergence trades before 14:00.

---

## Risk Management

| Rule              | Guideline                       |
|-------------------|---------------------------------|
| Max Risk/Trade    | 1% of account equity            |
| Stop Placement    | Beyond 2nd pivot extreme        |
| Min R:R           | 1:1.5 (measure before entry)    |
| Max Divergence Trades | 3 per day                  |
| Daily Loss Limit  | −2% → stop for the day          |

---

## False Divergence Traps

**Avoid these high-failure scenarios:**

- 🚫 Divergence during strong trending move — trend can override RSI.
- 🚫 Very short time between two pivots (< 10 bars on 5-min chart).
- 🚫 Divergence on the first touch of a new level (needs confirmation bounce first).
- 🚫 Taking the trade on major news day (fundamentals override technicals).

---

## Example Trade Log

```
Date:         2026-06-17
Symbol:       VN30F2607
Pivot 1:      09:45 — Price 1,258, RSI 28
Pivot 2:      10:30 — Price 1,254 (Lower Low), RSI 34 (Higher Low)
Divergence:   Bullish Regular ✓
RSI Zone:     28/34 < 40 ✓
S/R Confluence: 1,253 is PDL support ✓
Volume:       Declining on 2nd low ✓
Entry:        1,255 (Long, close of divergence candle)
Stop:         1,250 (-5 pts, below 2nd pivot)
T1:           1,262 (swing midpoint) ← 50% closed
T2:           1,270 (next resistance) ← 50% closed
Result:       +WIN
```

---

## Notes & Improvements

- **Multi-timeframe divergence**: If 5-min AND 15-min both show divergence simultaneously → very high probability setup.
- Consider using **MACD divergence** as a secondary confirmation (same logic, different oscillator).
- Build a **divergence tracker spreadsheet** to log all setups — identify which RSI levels and market conditions produce the best setups.
- Works excellently near session highs/lows when price is extended and volume is waning.

---

*Category: Reversal / Price Action | Timeframe: Intraday (5-min + 15-min) | Market: VN30F / HSX Stocks*
