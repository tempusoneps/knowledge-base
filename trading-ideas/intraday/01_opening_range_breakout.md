# 01 — Opening Range Breakout (ORB)

## Overview

Trade the breakout of the first 15-minute (or 30-minute) candle range after market open. This is one of the most battle-tested intraday strategies, exploiting the directional momentum that often forms in the first hour of trading as institutions execute their opening orders.

---

## Concept

The **Opening Range** is defined as the High and Low of the first N minutes after market open. When price breaks above the High → **Long**. When price breaks below the Low → **Short**.

```
Opening Range = [High_of_first_N_min, Low_of_first_N_min]
```

---

## Setup & Entry Rules

| Parameter        | Value                                      |
|------------------|--------------------------------------------|
| Timeframe        | 5-min chart for execution; 15-min for range |
| Markets          | VN30 Futures (VN30F), Liquid stocks (HSX)  |
| Session          | 09:00 – 09:15 = range formation period     |
| Entry            | First 5-min close **above ORB High** (Long) / **below ORB Low** (Short) |
| Confirmation     | Volume on breakout candle > 1.5× average   |

### Long Entry
1. Wait for 09:15 to close the opening range.
2. Enter **Long** when a 5-min candle closes above `ORB_High`.
3. Confirm with volume surge.
4. Stop Loss: below `ORB_Low` or below the breakout candle low.

### Short Entry
1. Enter **Short** when a 5-min candle closes below `ORB_Low`.
2. Confirm with volume surge.
3. Stop Loss: above `ORB_High` or above the breakout candle high.

---

## Exit Rules

- **Target 1 (T1):** 1× ORB range (range = ORB_High − ORB_Low), take 50% position.
- **Target 2 (T2):** 2× ORB range, exit remaining 50%.
- **Time Stop:** Close all positions before 14:00 (last 30 min of session is volatile).
- **Trailing Stop:** After T1 hit, move stop to break-even.

---

## Filters (Avoid False Breakouts)

- [ ] Skip if ORB range is **too narrow** (< 0.3% of price) → likely choppy day.
- [ ] Skip if ORB range is **too wide** (> 2% of price) → risk too high.
- [ ] Check D1 trend: prefer Long setups on uptrend days, Short on downtrend days.
- [ ] Avoid on days with major macro news (FOMC, CPI releases).
- [ ] VIX/market sentiment alignment preferred.

---

## Risk Management

| Rule             | Guideline                        |
|------------------|----------------------------------|
| Max Risk/Trade   | 1% of account equity             |
| Position Size    | `Risk / (Entry − Stop)`          |
| Max Trades/Day   | 2 (Long + Short if both trigger) |
| Daily Loss Limit | −2% of account → stop trading    |

---

## Edge & Statistics

- Works best on **trending days** (Monday/Tuesday after gap open).
- Win rate typically **50–60%** with 1:2 R:R → positive expectancy.
- Performs poorly in sideways/choppy sessions (Thursday/Friday pre-close).

---

## Example Trade Log

```
Date:      2026-06-20
Symbol:    VN30F2607
ORB High:  1,280.5
ORB Low:   1,274.0
Range:     6.5 pts
Entry:     1,281.5 (Long, breakout confirmed at 09:22)
Stop:      1,273.0 (-8.5 pts)
T1:        1,287.0 (+5.5 pts) ← 50% closed
T2:        1,293.5 (+12 pts)  ← 50% closed
Result:    +WIN
```

---

## Notes & Improvements

- Can combine with **VWAP**: only take Long if breakout happens above VWAP.
- Add **pre-market gap analysis**: stocks gapping up >0.5% have higher ORB success.
- Backtest window: 2023–2025 on VN30F, at least 200 trading days.

---

*Category: Momentum | Timeframe: Intraday | Market: VN30F / HSX Stocks*
