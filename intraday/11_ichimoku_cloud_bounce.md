# 11 — Ichimoku Cloud Bounce

## Overview

The Ichimoku Cloud (Kumo) provides a multi-dimensional view of support, resistance, momentum, and trend direction in a single indicator. When price pulls back to the Kumo cloud and bounces — confirmed by Tenkan/Kijun alignment — it represents a high-conviction trend continuation trade used widely by Japanese and Asian institutional traders.

---

## Concept

```
Tenkan-sen (9):  (9-period High + Low) / 2   ← fast line
Kijun-sen (26):  (26-period High + Low) / 2  ← slow line / signal
Senkou A:        (Tenkan + Kijun) / 2, shifted +26
Senkou B:        (52-period High + Low) / 2, shifted +26
Chikou Span:     Current close, shifted -26
Kumo (Cloud):    Zone between Senkou A and Senkou B

Bullish setup:  Price above cloud, Tenkan > Kijun, Chikou above price
Bounce trade:   Price pulls back INTO or just above cloud edge → reversal
```

---

## Indicators Required

| Indicator     | Setting         | Purpose                         |
|---------------|-----------------|---------------------------------|
| Tenkan-sen    | 9-period        | Short-term momentum signal line  |
| Kijun-sen     | 26-period       | Medium-term baseline             |
| Senkou A      | (T+K)/2, +26   | Fast cloud boundary              |
| Senkou B      | 52-period, +26 | Slow cloud boundary              |
| Chikou Span   | Close, −26      | Trend confirmation               |
| Volume        | 20-bar MA       | Bounce confirmation              |

---

## Setup & Entry Rules

| Parameter    | Value                                          |
|--------------|------------------------------------------------|
| Timeframe    | 15-min chart (Ichimoku works best on higher TF)|
| Markets      | VN30F, VHM, VIC, VCB (trending instruments)   |
| Session      | 09:30 – 13:30                                  |
| Cloud State  | Price must be **above** cloud (Long) or **below** cloud (Short) |

### Long Entry (Kumo Bounce)
1. Price is in an uptrend (above cloud, cloud is bullish green).
2. Price pulls back to touch or enter the top edge of Kumo.
3. Tenkan-sen > Kijun-sen (bullish cross or maintained).
4. Chikou Span is above price from 26 periods ago.
5. A bullish reversal candle forms at the cloud edge (hammer, engulfing).
6. Enter Long on the reversal candle close.
7. Stop Loss: Below the bottom of the Kumo cloud.

### Short Entry (Kumo Resistance Bounce)
1. Price is below cloud (bearish trend).
2. Price rallies up to touch the bottom edge of Kumo.
3. Tenkan-sen < Kijun-sen.
4. Chikou Span is below price.
5. Bearish reversal candle at cloud bottom.
6. Enter Short on reversal candle close.
7. Stop Loss: Above the top of the Kumo cloud.

---

## Exit Rules

- **Target 1:** Tenkan-sen level (first resistance for bounce trade) → 50%.
- **Target 2:** Previous swing high/low or next major S/R → 50%.
- **Trail:** Trail stop below Kijun-sen (Long) or above Kijun-sen (Short).
- **Failure:** If price closes through the opposite cloud edge → exit immediately.
- **Time Stop:** Close all by 14:00.

---

## Filters

- [ ] Skip if cloud is flat (Senkou A ≈ Senkou B) — weak support.
- [ ] Skip if Chikou Span is inside price candles (ambiguous trend).
- [ ] Avoid trading a thin cloud (< 0.3% width) — too weak to hold.
- [ ] Skip if overall VN30 is in counter-trend to trade direction.
- [ ] Do not trade the first Kumo touch if approaching with extreme velocity.

---

## Risk Management

| Rule              | Guideline                          |
|-------------------|------------------------------------|
| Max Risk/Trade    | 1% of account equity               |
| Stop Placement    | Beyond far edge of Kumo cloud      |
| Min R:R           | 1:1.5                              |
| Max Trades/Day    | 2                                  |
| Daily Loss Limit  | −2%                                |

---

## Edge & Statistics

- Win rate: **55–65%** on trending days.
- R:R: **1:1.5 to 1:2**.
- Best on: Stocks with clean, sustained intraday trends.
- Worst on: Choppy, low-volatility sessions.

---

## Example Trade Log

```
Date:      2026-06-20
Symbol:    VN30F2607
Cloud:     1,265–1,272 (bullish green)
Pullback:  Price touches 1,273 (top of cloud)
Reversal:  Hammer candle at 10:30
Entry:     1,274 (Long)
Stop:      1,262 (below cloud bottom)
T1:        1,283 (Tenkan level) ← 50% closed
T2:        1,292 (prior high) ← 50% closed
Result:    +WIN
```

---

## Notes & Improvements

- Combine with **Kijun bounce**: when price touches Kijun (not cloud), even higher probability setup.
- Use **26-period settings** adjusted for Vietnamese session length if needed.
- Backtest Ichimoku exclusively on trending days (filter by ADX > 25 on D1).
- Kumo twists (where Senkou A crosses Senkou B ahead) signal upcoming trend change — avoid trading into a twist.

---

*Category: Trend Following | Timeframe: Intraday (15-min) | Market: VN30F / HSX Stocks*
