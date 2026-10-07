# 27 — Lunchtime Reversal (Vietnam Break Session)

## Overview

Vietnam's HOSE market has a **mandatory midday break** from 11:30 to 13:00. During this break, news is processed, positions reconsidered, and sentiment shifts. When the afternoon session reopens at 13:00, price frequently **reverses the morning direction** — especially if the morning move was extreme. This creates a highly reliable time-based intraday pattern unique to Vietnamese markets.

---

## Concept

```
Session Structure (HOSE):
  Morning: 09:00–11:30 (continuous trading)
  Break:   11:30–13:00 (no trading, news processing)
  Afternoon: 13:00–14:30 (continuous trading)
  ATC:     14:30–14:45

Lunchtime Reversal Logic:
  IF morning session up >0.8% → Afternoon opens flat/down → SHORT
  IF morning session down >0.8% → Afternoon opens flat/up → LONG

Why: Traders who gained in morning lock in profits at 13:00 open
     News that broke at 11:30 often reverses sentiment
     Foreign orders execute differently in PM session
```

---

## Setup & Entry Rules

| Parameter      | Value                                          |
|----------------|------------------------------------------------|
| Timeframe      | 5-min chart                                    |
| Markets        | VN30F, VN30 index constituents                 |
| Entry Window   | 13:00 – 13:20 (first 20 min of PM session)     |
| Trigger        | Morning change >0.8% in one direction          |

### Short Entry (PM Reversal after Strong Morning Up)
1. VN-Index or target stock up >0.8% by 11:30 close.
2. PM session opens (13:00) with flat or slightly negative first candle.
3. First 5-min candle (13:00–13:05) fails to continue morning uptrend.
4. Price is near or below VWAP at 13:00.
5. Volume on first PM candle is lower than morning average (no new buying).
6. Enter Short at 13:05 open (after first candle confirms reversal intent).
7. Stop Loss: Above the 11:30 session close price (morning high).

### Long Entry (PM Reversal after Strong Morning Down)
1. VN-Index or stock down >0.8% by 11:30.
2. PM session opens with flat or slightly positive first candle.
3. Price fails to make new lows.
4. Enter Long at 13:05.
5. Stop: Below the 11:30 session low.

---

## Exit Rules

- **Target 1:** VWAP (take 60% of position).
- **Target 2:** Morning open price (start of day price) → take 40%.
- **Trail:** After VWAP hit, trail stop to break-even.
- **Failure:** If PM session continues morning direction with volume → exit immediately.
- **Hard Exit:** 14:15 — close everything before ATC.

---

## Morning Condition Assessment (at 11:25, before break)

| Condition                              | Reversal Probability |
|----------------------------------------|----------------------|
| Morning up >1.5%, RSI overbought       | High (~65%)          |
| Morning up 0.8–1.5%, no strong news   | Moderate (~55%)      |
| Morning up >0.8% on major news        | Low (~35%) — skip    |
| Morning flat (< ±0.5%)                | No trade             |
| Morning down >1.5%, RSI oversold      | High (~65%)          |

---

## Filters

- [ ] Skip if the morning move was driven by major market-wide news (rate cut, major macro event).
- [ ] Check if there is afternoon-specific news scheduled (company announcements at 13:00).
- [ ] Skip if VN30F futures are indicating continuation of morning trend at 12:50.
- [ ] Avoid this trade during **quarterly index rebalancing** (PM often continues morning).
- [ ] Skip on ex-dividend days for the stock (abnormal price behavior).

---

## Risk Management

| Rule              | Guideline                              |
|-------------------|----------------------------------------|
| Max Risk/Trade    | 0.75% of account equity                |
| Stop Placement    | Beyond morning session extreme         |
| Min R:R           | 1:1.5 (VWAP target)                    |
| Max Trades/Day    | 1 lunchtime reversal (one clear signal)|
| Daily Loss Limit  | −1.5%                                  |

---

## Edge & Statistics

- Win rate: **55–65%** on extreme morning sessions (>1%).
- Lower win rate (~45%) on moderate 0.8–1% morning moves.
- This strategy is most effective in **range-bound market environments** (no sustained bull/bear run).
- Best months: April–June, October (range-bound periods in Vietnamese market).

---

## Example Trade Log

```
Date:         2026-06-12
Symbol:       VN30F2607
Morning:      VN30F up from 1,265 to 1,282 (+1.34%) by 11:30
Break:        11:30 — RSI 71 (overbought), no specific news driver
PM Open:      13:00 — first candle: 1,280 high, 1,277 low (fails to break 1,282)
VWAP:         1,273 (price above at 13:00 but fading)
Entry:        1,278 (Short at 13:05, after first PM candle confirms reversal)
Stop:         1,284 (above 11:30 high)
T1:           1,273 (VWAP) ← 60% closed at 13:25
T2:           1,265 (morning open) ← 40% closed at 14:00
Result:       +WIN
```

---

## Notes & Improvements

- Build a **pre-break monitor**: at 11:25 each day, auto-calculate morning P&L and RSI to prequalify the setup.
- Track reversal rate by day of week: some analysis suggests Tuesday/Wednesday PM reversals are more common.
- Pair with **VN30F premium/discount** at 12:55: if futures are trading at significant discount to cash, PM likely down → adds conviction to Short setup after strong morning.
- This strategy pairs naturally with a morning ORB or HOD breakout strategy — take profit on morning momentum, then reverse at 13:00.

---

*Category: Time-Based Reversal | Timeframe: Intraday (5-min) | Market: VN30F / VN30 Stocks*
