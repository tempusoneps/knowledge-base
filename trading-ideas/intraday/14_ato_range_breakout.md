# 14 — Pre-Market High / Low Breakout (ATO Range)

## Overview

In the Vietnamese market, the **ATO (At The Open)** auction session (09:00–09:15) establishes the opening price through a batch auction. The high and low of the first few matched prices form a **pre-market range** that often acts as the day's initial directional trigger. A breakout from this ATO range in the continuous session signals strong institutional directional intent.

---

## Concept

```
ATO Session:     09:00 – 09:15 (batch auction, HOSE)
ATO Price:       Single matched price at 09:15
Pre-market Range: Based on ATO order book imbalance signals

Continuous Session: 09:15 onwards
First Candle Range: 09:15–09:20 (first 5-min candle)

ATO Breakout: If 2nd candle (09:20–09:25) breaks ABOVE first candle High → Long
              If 2nd candle breaks BELOW first candle Low → Short
```

**Why it works:** The ATO price often represents the market's initial "best guess" of fair value. Institutional order flow that didn't fully execute in ATO continues into continuous session, driving the first directional move.

---

## Indicators Required

| Indicator   | Setting     | Purpose                                    |
|-------------|-------------|--------------------------------------------|
| ATO Price   | 09:15 fix   | Reference for gap vs. prior day            |
| VWAP        | Daily       | Directional bias post-open                 |
| Volume      | 1st candle  | Confirm directional conviction             |
| EMA         | 9-period    | Short-term trend after ATO                 |

---

## Setup & Entry Rules

| Parameter    | Value                                            |
|--------------|--------------------------------------------------|
| Timeframe    | 1-min and 5-min chart                            |
| Markets      | VN30F, VN30 index stocks (VCB, VHM, HPG, VIC)   |
| Range Period | First 5-min candle (09:15–09:20)                 |
| Entry Window | 09:20 – 09:45                                    |

### Long Entry
1. ATO price is above prior day close (gap up context).
2. First 5-min candle (09:15–09:20) closes bullishly.
3. Second 5-min candle breaks above first candle high with volume.
4. VWAP trending up from session open.
5. Enter Long on close of second candle above range.
6. Stop Loss: Below first candle low.

### Short Entry
1. ATO price below prior day close (gap down or flat-to-down open).
2. First 5-min candle closes bearishly.
3. Second candle breaks below first candle low with volume.
4. VWAP trending down.
5. Enter Short.
6. Stop Loss: Above first candle high.

---

## Exit Rules

- **Target 1:** 1.5× the ATO range distance from entry → 60%.
- **Target 2:** Prior day high/low or next major S/R → 40%.
- **Trail:** Move stop to break-even after T1.
- **Failure:** If price re-enters the first candle range → exit.
- **Time Stop:** This is an early-session trade; exit by 11:00 at latest.

---

## Filters

- [ ] Skip if ATO range (first candle) is larger than 1% — risk too wide.
- [ ] Skip if ATO range is smaller than 0.2% — too tight, unclear direction.
- [ ] Avoid on ex-dividend days (erratic open prices).
- [ ] Check ATO order book before open if broker provides data.
- [ ] Skip if there is major pre-market news impacting the entire market.

---

## Risk Management

| Rule              | Guideline                          |
|-------------------|------------------------------------|
| Max Risk/Trade    | 0.75% of account equity            |
| Stop Placement    | Beyond first candle extreme        |
| Min R:R           | 1:1.5                              |
| Max Trades/Day    | 2 (this is an early-session only trade) |
| Daily Loss Limit  | −1.5%                              |

---

## Edge & Statistics

- Win rate: **55–65%** on gap-driven open days.
- Works exceptionally well when ATO price is driven by overnight news.
- Worst on: Inside-open days (ATO ≈ prior close, no clear gap bias).

---

## Example Trade Log

```
Date:      2026-06-09
Symbol:    VCB (HSX)
Prior Close: 89,500
ATO Price: 90,200 (gap up 0.78%)
1st Candle: 09:15–09:20 High 90,500 / Low 90,000 (bullish)
2nd Candle: Breaks above 90,500 at 09:22, volume 2× ✓
VWAP:      90,150 and rising ✓
Entry:     90,600 (Long)
Stop:      89,950 (below 1st candle low)
T1:        91,550 (+950, R:R 1:1.5) ← 60% closed
T2:        92,300 (prior resistance) ← 40% closed
Result:    +WIN
```

---

## Notes & Improvements

- Automate ATO range capture: log the 09:15 matched price and first candle H/L daily.
- Combine with **sector momentum**: if entire banking sector gaps up, ATO breakout on VCB has higher conviction.
- Track statistics by gap size bucket: gaps 0.5–1% have best ATO breakout follow-through.
- On low-volume ATO (thin order book), skip — price can spike and reverse rapidly.

---

*Category: Momentum Breakout | Timeframe: Intraday (1-min / 5-min) | Market: VN30F / HSX Stocks*
