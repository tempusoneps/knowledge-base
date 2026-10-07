# 03 — EMA Crossover Momentum Scalp

## Overview

A dual EMA crossover on the 5-minute chart used as a momentum scalping system. The fast EMA crossing above the slow EMA signals bullish momentum; crossing below signals bearish momentum. This strategy is mechanical, rules-based, and designed for systematic intraday scalping with tight stops.

---

## Concept

```
Fast EMA: 9-period EMA (reacts quickly to price changes)
Slow EMA: 21-period EMA (filters noise, shows trend direction)
Signal:   Crossover direction determines trade bias
```

Price momentum shifts when short-term average crosses long-term average. Trades are taken in the direction of the cross, filtered by the 50 EMA acting as a trend baseline.

---

## Indicators Required

| Indicator  | Setting   | Purpose                       |
|------------|-----------|-------------------------------|
| EMA Fast   | 9-period  | Short-term momentum           |
| EMA Slow   | 21-period | Medium-term trend             |
| EMA Trend  | 50-period | Filter: only trade above/below|
| Volume     | 20-period MA | Confirm momentum            |
| RSI        | 14-period | Avoid overbought/oversold entries |

---

## Setup & Entry Rules

| Parameter   | Value                                          |
|-------------|------------------------------------------------|
| Timeframe   | 5-min chart                                    |
| Markets     | VN30F, VHM, VIC, HPG, VCB, BID (liquid)        |
| Session     | 09:30 – 13:30                                  |

### Long Entry (Bullish Cross)
1. EMA9 crosses **above** EMA21 on a 5-min close.
2. Price is **above** EMA50 (uptrend filter).
3. Volume on cross candle > 20-period average volume.
4. RSI between 45–70 (not overbought).
5. Enter at open of next candle after confirmed cross.
6. Stop Loss: below EMA21 or below the cross candle low.

### Short Entry (Bearish Cross)
1. EMA9 crosses **below** EMA21 on a 5-min close.
2. Price is **below** EMA50 (downtrend filter).
3. Volume confirms.
4. RSI between 30–55 (not oversold).
5. Enter at open of next candle.
6. Stop Loss: above EMA21 or above the cross candle high.

---

## Exit Rules

- **Profit Target:** 1.5× to 2× risk (R:R minimum 1:1.5).
- **Signal Exit:** Exit when EMA9 crosses back against the trade direction.
- **EMA Trail:** Once in profit, trail stop below EMA21 (Long) or above EMA21 (Short).
- **Time Exit:** Close all positions at 14:00.

---

## Filters to Improve Win Rate

- [ ] Only trade in direction of D1 trend (check daily chart first).
- [ ] Avoid crossovers that happen in tight range zones (EMAs flat = avoid).
- [ ] Skip if the crossover candle has >2× normal spread (slippage risk).
- [ ] Do not trade the first cross of the day (often a false signal during volatile open).
- [ ] Prefer the 2nd or 3rd cross of the day after trend is established.

---

## Risk Management

| Rule              | Guideline                      |
|-------------------|--------------------------------|
| Max Risk/Trade    | 0.75% of account               |
| Position Size     | `Risk / (Entry − Stop)`        |
| Max Trades/Day    | 4 scalps maximum               |
| Consecutive Loss  | 3 losses in a row → stop today |
| Daily Loss Limit  | −2% → done for the day         |

---

## Edge & Statistics

- Win rate: **45–55%** (pure mechanical, no discretion).
- Average R:R: **1:1.8** → positive expectancy at >40% win rate.
- Best markets: Trending, not range-bound.
- Worst condition: Inside-day, VIX crush, no volume.

---

## Example Trade Log

```
Date:       2026-06-15
Symbol:     VN30F2607
EMA9 > 21:  09:35 cross confirmed
EMA50 Filter: Price above 50 EMA ✓
Volume:     1.8× average ✓
RSI:        52 ✓
Entry:      1,270.0 (Long at 09:40 open)
Stop:       1,265.5 (below EMA21)
Target:     1,278.0 (+8 pts, R:R = 1:1.8)
Result:     +WIN, exited at 1,277.5
```

---

## Automation Notes

```python
# Pseudocode for systematic scanner
for symbol in watchlist:
    ema9  = EMA(close, 9)
    ema21 = EMA(close, 21)
    ema50 = EMA(close, 50)
    
    long_signal  = crossover(ema9, ema21) and close > ema50 and volume > avg_vol * 1.2
    short_signal = crossunder(ema9, ema21) and close < ema50 and volume > avg_vol * 1.2
```

---

## Notes & Improvements

- Add **ATR filter**: skip trades when ATR(14) < 0.3% of price (too quiet).
- Optimize EMA periods per symbol via backtest (VN30F may suit 8/20 better).
- Consider switching to **EMA on close vs. open** for smoother signals.

---

*Category: Momentum Scalping | Timeframe: Intraday (5-min) | Market: VN30F / HSX Stocks*
