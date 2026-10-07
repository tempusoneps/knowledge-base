# 21 — Volume Profile Point of Control (POC) Bounce

## Overview

**Volume Profile** shows how much volume traded at each price level during a session. The **Point of Control (POC)** is the price level with the most volume traded — representing the "fairest price" in the market's collective opinion. Price has a strong statistical tendency to return to the POC after deviating from it, and to bounce when it reaches the **High Value Area (VAH)** and **Low Value Area (VAL)** boundaries.

---

## Concept

```
Volume Profile Structure:
  POC  = Price level with MOST volume (market consensus = "fair value")
  VAH  = Value Area High (upper boundary of 70% of all volume)
  VAL  = Value Area Low (lower boundary of 70% of all volume)
  HVN  = High Volume Node (price level with above-average volume)
  LVN  = Low Volume Node (price level with below-average volume)

Behavior:
  Price at VAL → tends to bounce LONG back to POC
  Price at VAH → tends to bounce SHORT back to POC
  Price breaks VAL/VAH → moves to next LVN/HVN
```

---

## Indicators Required

| Indicator       | Setting              | Purpose                       |
|-----------------|----------------------|-------------------------------|
| Volume Profile  | Session (daily reset)| Identify POC, VAH, VAL        |
| VWAP            | Daily                | Complement to POC analysis    |
| Volume          | 20-bar MA            | Confirm bounce momentum       |
| RSI             | 14-period            | Overbought/oversold at levels |

---

## Setup & Entry Rules

| Parameter    | Value                                           |
|--------------|-------------------------------------------------|
| Timeframe    | 5-min chart with volume profile sidebar        |
| Markets      | VN30F (cleanest volume profile patterns)        |
| Profile Type | Session profile (reset daily)                  |
| Session      | 09:30 – 13:30 (after profile has enough data)  |

### Long Entry (VAL Bounce → POC)
1. Session VAL has formed with sufficient trading history (after 10:00).
2. Price pulls back to VAL level.
3. A bullish reversal candle forms at VAL (hammer, bullish engulfing).
4. RSI < 40 at VAL (oversold context).
5. Enter Long on the reversal candle close.
6. Stop Loss: 1 ATR below VAL.
7. Target: Session POC (primary), VAH (extended).

### Short Entry (VAH Fade → POC)
1. Price rises to VAH level.
2. Bearish reversal candle at VAH.
3. RSI > 60.
4. Enter Short.
5. Stop: 1 ATR above VAH.
6. Target: Session POC.

---

## Exit Rules

- **Target 1:** Session POC (close 70% of position).
- **Target 2:** Opposite Value Area boundary (VAH for longs, VAL for shorts) — close 30%.
- **Trail:** After POC hit, trail stop to break-even.
- **Failure:** If price closes decisively outside the value area → level breakdown → exit.
- **Time Stop:** Close before 14:15.

---

## Filters

- [ ] Only trade VAL/VAH bounces after 10:00 (profile needs time to develop).
- [ ] Skip if VAL = VAH (very narrow value area — no meaningful structure yet).
- [ ] POC must be between VAL and VAH (obvious, but software glitches happen).
- [ ] Skip if price has already touched the level 3× today without bouncing (likely to break).
- [ ] Check if yesterday's POC aligns with today's VAL/VAH for stronger confluence.

---

## Risk Management

| Rule              | Guideline                        |
|-------------------|----------------------------------|
| Max Risk/Trade    | 1% of account equity             |
| Stop Placement    | 1 ATR beyond VAL or VAH          |
| Min R:R           | 1:1.5 (POC distance ÷ stop)      |
| Max Trades/Day    | 3                                |
| Daily Loss Limit  | −2%                              |

---

## Edge & Statistics

- Win rate: **60–68%** on mature session profiles (after 10:00).
- POC as target is achieved ~70% of the time when entering from VAL/VAH.
- Best on: Range days where price oscillates within the value area.
- Worst on: Trend days where price breaks VAH/VAL and never returns.

---

## Example Trade Log

```
Date:         2026-06-16
Symbol:       VN30F2607
Session POC:  1,274 (developed by 10:30)
Session VAL:  1,268
Session VAH:  1,280
Action:       Price pulls back to 1,268 (VAL) at 11:00
Candle:       Hammer, RSI = 36 ✓
Entry:        1,269 (Long)
Stop:         1,264 (1 ATR below VAL)
T1:           1,274 (POC) ← 70% closed at 11:25
T2:           1,280 (VAH) ← 30% closed at 12:00
Result:       +WIN
```

---

## Notes & Improvements

- Use **Composite Volume Profile** (multi-session, 5-day or 20-day) for higher-timeframe POC levels that act as stronger S/R.
- When today's price is trading **inside yesterday's value area** → expect range-bound behavior, ideal for VAL/VAH bounce.
- When today's price is **outside yesterday's value area** → trend day likely → skip bounce trades.
- Build automated POC/VAH/VAL calculation using tick data or OHLCV approximation.

---

*Category: Volume Analysis / Mean Reversion | Timeframe: Intraday | Market: VN30F / HSX Stocks*
