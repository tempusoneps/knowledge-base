# 02 — VWAP Mean Reversion

## Overview

VWAP (Volume Weighted Average Price) acts as a dynamic intraday "fair value" line. Institutional algorithms constantly reference VWAP to benchmark execution quality. When price deviates significantly from VWAP and shows reversal signals, a mean-reversion trade back toward VWAP offers a high-probability setup.

---

## Concept

```
VWAP = Σ(Price × Volume) / Σ(Volume)   [reset daily at open]
```

Price tends to return to VWAP throughout the session. Extreme deviations (measured by standard deviation bands) provide fade/reversion opportunities.

**VWAP Bands:**
- Upper Band 1 = VWAP + 1σ
- Upper Band 2 = VWAP + 2σ
- Lower Band 1 = VWAP − 1σ
- Lower Band 2 = VWAP − 2σ

---

## Setup & Entry Rules

| Parameter     | Value                                         |
|---------------|-----------------------------------------------|
| Timeframe     | 5-min chart                                   |
| Markets       | VN30F, top 20 liquid HSX stocks               |
| Best Session  | 09:30 – 13:00 (avoid first 15 min)            |
| Entry Signal  | Price touches VWAP ±2σ band + reversal candle |
| Confirmation  | RSI(14) divergence or engulfing candle        |

### Long Setup (Reversion from Below)
1. Price pulls back to VWAP Lower Band 2 (VWAP − 2σ).
2. A bullish reversal candle forms (hammer, engulfing, doji + follow-up).
3. RSI(14) < 35 and turning up.
4. Enter Long at the close of the reversal candle.
5. Stop Loss: 0.5% below the entry candle low.

### Short Setup (Reversion from Above)
1. Price extends to VWAP Upper Band 2 (VWAP + 2σ).
2. A bearish reversal candle forms (shooting star, bearish engulfing).
3. RSI(14) > 65 and turning down.
4. Enter Short at the close of the reversal candle.
5. Stop Loss: 0.5% above the entry candle high.

---

## Exit Rules

- **Primary Target:** VWAP midline (take 70% of position).
- **Extended Target:** Opposite 1σ band (take remaining 30%).
- **Time Stop:** Close before 14:15 regardless of P&L.
- **Invalidation:** If price consolidates at the band for >3 candles without reversing → skip trade.

---

## Filters

- [ ] Avoid during the first 15 minutes (VWAP not yet meaningful).
- [ ] Skip if overall market trend is extremely strong (price won't revert).
- [ ] Confirm volume is declining on the extended move (exhaustion signal).
- [ ] Do not trade against strong gap days (gap >1.5%).
- [ ] Best results when D1 candle is inside the previous day's range (range day).

---

## Risk Management

| Rule              | Guideline                     |
|-------------------|-------------------------------|
| Max Risk/Trade    | 0.8% of account equity        |
| Entries per Side  | Max 2 Long + 2 Short per day  |
| Stop Type         | Fixed % stop (0.5% from entry)|
| Daily Loss Limit  | −1.5% → stop trading          |

---

## Edge & Statistics

- Mean reversion has higher win rate (~60–70%) but smaller average wins.
- R:R typically 1:1.5 to 1:2.
- Works excellently on liquid, large-cap stocks with tight spreads.
- Underperforms on news-driven spike days.

---

## Example Trade Log

```
Date:     2026-06-18
Symbol:   HPG (HSX)
VWAP:     26,800
-2σ Band: 26,200
Entry:    26,250 (Long, hammer candle + RSI 31)
Stop:     26,115 (-135 pts, -0.51%)
T1:       26,800 (+550 pts) ← 70% closed
T2:       27,100 (+850 pts) ← 30% closed
Result:   +WIN
```

---

## Notes & Improvements

- Use **anchored VWAP** from swing high/low for even stronger signals.
- Combine with **order flow** (bid/ask imbalance) for higher conviction entries.
- Works well as a complement to ORB: if ORB setup fails and price returns to VWAP, this strategy captures the reversion.

---

*Category: Mean Reversion | Timeframe: Intraday | Market: VN30F / HSX Stocks*
