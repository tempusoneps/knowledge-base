# 33 — Donchian Channel Intraday Breakout

## Overview

**Donchian Channels** track the highest high and lowest low over N periods — effectively showing the N-period price range. Breakouts above the upper channel or below the lower channel signal the beginning of new short-term trends. Unlike moving average crossovers, Donchian breakouts are pure price-based and filter out noise by requiring price to exceed a definitive multi-period extreme.

---

## Concept

```
Donchian Channel (N-period):
  Upper Band = Highest High of last N bars
  Lower Band = Lowest Low of last N bars
  Midline    = (Upper + Lower) / 2

Breakout Signal:
  New Upper Band HIGH = bullish breakout → Long
  New Lower Band LOW  = bearish breakdown → Short

Period Settings:
  N = 20 bars on 5-min = 100 minutes of trading range
  N = 12 bars on 5-min = 60 minutes (more sensitive)
```

**Turtle Trading connection:** The original Turtle Trading system used Donchian Channel breakouts on daily charts. The same principle adapted to intraday captures momentum breakouts with mechanical precision.

---

## Indicators Required

| Indicator        | Setting          | Purpose                         |
|------------------|------------------|---------------------------------|
| Donchian Channel | N=20 on 5-min    | Define breakout levels          |
| Donchian Midline | (Upper+Lower)/2  | Mean reversion target           |
| Volume           | 20-bar MA        | Confirm breakout momentum       |
| ATR              | 14-period        | Set trailing stop distance      |
| EMA              | 50-period        | Trend direction filter          |

---

## Setup & Entry Rules

| Parameter    | Value                                          |
|--------------|------------------------------------------------|
| Timeframe    | 5-min chart                                    |
| Markets      | VN30F, trending HSX stocks                     |
| N Period     | 20 bars (100 min of history)                   |
| Session      | 09:30 – 13:00                                  |

### Long Entry (Upper Channel Breakout)
1. Price closes above the 20-bar Donchian upper band (new 100-min high).
2. This high must not have been touched in the prior 20 bars (genuine new range).
3. Volume on breakout candle > 1.5× average.
4. Price is above EMA(50) (trend filter).
5. Enter Long on the next candle open after confirmed breakout.
6. Stop Loss: 1.5× ATR below entry or Donchian midline (whichever is closer).

### Short Entry (Lower Channel Breakdown)
1. Price closes below 20-bar Donchian lower band (new 100-min low).
2. Volume confirms.
3. Price below EMA(50).
4. Enter Short on next candle open.
5. Stop: 1.5× ATR above entry or midline.

---

## Exit Rules

- **Target 1:** 1× ATR from entry → close 40%.
- **Target 2:** 2× ATR from entry → close 40%.
- **Trail Exit:** Exit remaining 20% when price closes back inside the Donchian channel (momentum lost).
- **Failure:** If price immediately returns inside the channel after breakout → exit within 2 candles.
- **Time Stop:** Close before 14:00.

---

## Channel Width Analysis

```
Narrow Channel (small Upper-Lower difference):
  → Squeeze condition → Breakout likely to be large

Wide Channel (large Upper-Lower difference):
  → Market already moved → Breakout less meaningful

Optimal: Channel width 0.5–1.5% of price before breakout
```

---

## Filters

- [ ] Skip breakouts where channel width > 2% (overextended market).
- [ ] Skip if market has had 3+ Donchian breakouts in same direction already (exhaustion).
- [ ] Avoid breakouts in first 20 candles of session (channel still forming).
- [ ] Skip during lunch break (12:00–13:00) — thin volume.
- [ ] Do not take a breakout that immediately retraces 50% of the breakout candle.

---

## Risk Management

| Rule              | Guideline                          |
|-------------------|------------------------------------|
| Max Risk/Trade    | 1% of account equity               |
| Stop Placement    | 1.5× ATR from entry                |
| Min R:R           | 1:2 (ATR-based targets)            |
| Max Trades/Day    | 3                                  |
| Daily Loss Limit  | −2%                                |

---

## Edge & Statistics

- Win rate: **45–55%** (trend-following system — many small losses, fewer big wins).
- Average win/loss ratio: ~2.5:1 (one large win covers 2+ losses).
- Best on: Trending market days with clear directional bias.
- Worst on: Range-bound days (many false breakouts).

---

## Example Trade Log

```
Date:         2026-06-21
Symbol:       VN30F2607
20-bar High:  1,278 (100-min high prior to 10:30)
Breakout:     10:30 — 5-min closes at 1,279.5 (new 100-min high)
Volume:       1.7× average ✓
EMA50:        Price above ✓
Channel Width: 1,278 − 1,264 = 14 pts (1.1%) — reasonable
Entry:        1,280 (next candle open)
ATR14:        6 pts
Stop:         1,271 (1.5× ATR below)
T1:           1,286 (1× ATR) ← 40% at 10:45
T2:           1,292 (2× ATR) ← 40% at 11:15
Runner Exit:  Closed back inside channel at 11:30 → 20% closed at 1,289
Result:       +WIN
```

---

## Notes & Improvements

- Backtest multiple N values (12, 16, 20, 24) on VN30F to find optimal channel period.
- Combine with **ORB**: if the ORB high equals the 20-bar Donchian high → double breakout signal = very strong setup.
- The **Donchian midline reversion** is itself a valid separate strategy: price returning to (Upper+Lower)/2 from extremes.
- For a pure mechanical system: Long on Upper break, Short on Lower break, exit at midline — test as a systematic algo.

---

*Category: Momentum Breakout | Timeframe: Intraday (5-min) | Market: VN30F / HSX Stocks*
