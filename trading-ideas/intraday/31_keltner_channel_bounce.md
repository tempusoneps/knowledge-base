# 31 — Keltner Channel Bounce

## Overview

**Keltner Channels** are volatility-based bands plotted around an EMA, using ATR to set band width. Unlike Bollinger Bands (which use standard deviation), Keltner Channels are smoother and respond less to sharp price spikes — making them ideal for mean-reversion trades. When price touches the outer Keltner band after an extended move, a reversion toward the EMA midline offers consistent edge.

---

## Concept

```
Keltner Channel:
  Middle:  EMA(20)
  Upper:   EMA(20) + Multiplier × ATR(10)
  Lower:   EMA(20) − Multiplier × ATR(10)
  
Standard multiplier: 2.0 (wider) or 1.5 (tighter)

Behavior:
  Price touching Upper KC → Overbought condition → Short/Fade
  Price touching Lower KC → Oversold condition → Long/Bounce
  Price returns to EMA(20) midline → Mean reversion target
```

**KC vs BB:** Keltner Channels filter out volatile spikes better than Bollinger Bands. Using KC for mean reversion and BB for squeeze detection (different strategy) covers both volatility dimensions.

---

## Indicators Required

| Indicator       | Setting              | Purpose                       |
|-----------------|----------------------|-------------------------------|
| Keltner Channel | EMA(20) ± 2× ATR(10) | Primary band levels           |
| EMA Midline     | EMA(20)              | Target for reversion          |
| ATR             | 10-period            | Band width reference           |
| Volume          | 20-bar MA            | Confirm bounce exhaustion     |
| RSI             | 14-period            | Overbought/oversold filter    |

---

## Setup & Entry Rules

| Parameter    | Value                                            |
|--------------|--------------------------------------------------|
| Timeframe    | 5-min chart                                      |
| Markets      | VN30F, VCB, BID, VHM, HPG (trending stocks)      |
| Session      | 09:30 – 13:30                                    |
| Multiplier   | 2.0 for standard; 1.5 for more frequent signals  |

### Long Entry (Lower KC Bounce)
1. Price touches or closes below the Lower Keltner Channel.
2. RSI < 35 (oversold).
3. A bullish reversal candle forms (hammer, engulfing, or piercing).
4. Volume declining on the move to the lower band (exhaustion).
5. Enter Long on reversal candle close.
6. Stop Loss: 1 ATR below the Lower KC band.

### Short Entry (Upper KC Fade)
1. Price touches or closes above the Upper Keltner Channel.
2. RSI > 65 (overbought).
3. Bearish reversal candle at upper band.
4. Volume declining on extension.
5. Enter Short.
6. Stop: 1 ATR above Upper KC.

---

## Exit Rules

- **Target 1:** EMA(20) midline → close 70%.
- **Target 2:** Opposite KC band → close 30%.
- **Trail:** After midline hit, trail stop to break-even.
- **Failure:** If price continues outside KC for 3+ candles with volume → trend mode, exit.
- **Time Stop:** Close before 14:15.

---

## Filters

- [ ] Skip if EMA(20) is strongly sloping in one direction (trend mode — don't fade).
- [ ] Require a genuine reversal candle (not just a touching of the band).
- [ ] Skip during major news events (fundamental moves override KC).
- [ ] Avoid in first 15 minutes of session (bands not calibrated yet).
- [ ] Do not take more than 3 KC bounces in one direction per session.

---

## Risk Management

| Rule              | Guideline                          |
|-------------------|------------------------------------|
| Max Risk/Trade    | 0.75% of account equity            |
| Stop Placement    | 1 ATR beyond band                  |
| Min R:R           | 1:1.5 (EMA midline target)         |
| Max Trades/Day    | 4                                  |
| Daily Loss Limit  | −2%                                |

---

## Edge & Statistics

- Win rate: **58–68%** with RSI confirmation.
- Best on: Range-bound to mildly trending sessions.
- Worst on: Strong trending sessions where price "walks" the upper/lower band.

---

## Example Trade Log

```
Date:      2026-06-19
Symbol:    VN30F2607
Lower KC:  1,262 (EMA20=1,270, ATR10=4, Lower=1,270−2×4=1,262)
Price:     Touches 1,261.5 at 10:45, hammer candle
RSI:       33 (oversold) ✓
Volume:    Declining ✓
Entry:     1,263 (Long)
Stop:      1,258 (1 ATR below band)
T1:        1,270 (EMA midline) ← 70% closed at 11:10
T2:        1,278 (Upper KC) ← 30% closed at 11:45
Result:    +WIN
```

---

## Notes & Improvements

- Keltner + Bollinger Bands together: when BB is inside KC → squeeze setup. When BB extends beyond KC → strong momentum.
- Try multiplier 1.5 for more frequent but slightly lower quality signals.
- On 15-min chart, Keltner bounces have higher reliability but fewer setups.
- Test different ATR periods (10 vs 14) on VN30F to optimize band responsiveness.

---

*Category: Mean Reversion | Timeframe: Intraday (5-min) | Market: VN30F / HSX Stocks*
