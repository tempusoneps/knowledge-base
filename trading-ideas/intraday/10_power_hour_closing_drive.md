# 10 — End-of-Day Closing Drive (Power Hour)

## Overview

The last 45–60 minutes of the trading session (13:15–14:30 on HOSE) often sees a directional "closing drive" as institutional traders rebalance portfolios, mutual funds mark end-of-day NAV positions, and index-tracking products execute their closing-price orders. This systematic end-of-day flow creates predictable momentum in the final session window.

---

## Concept

```
Session Close (HOSE): 14:30 (continuous) → 14:45 (ATC)
Power Hour Window:    13:15 – 14:20

Key Drivers:
  - Fund rebalancing → systematic buy/sell pressure
  - Index constituent buying (VN30, VNMidcap funds)
  - Retail closing positions before end-of-day
  - T+2 settlement considerations
```

**Statistical Bias:** Days where the market trends from 09:00–12:00 tend to **continue** in the same direction during Power Hour ~65% of the time. Days that reverse mid-session are less predictable.

---

## Pre-Condition Analysis (11:30–13:00 Preparation)

Before executing the closing drive strategy, assess market conditions:

| Condition                                          | Bias      |
|----------------------------------------------------|-----------|
| Market up >1% at midday, no reversal signal        | Bullish PM|
| Market down >1% at midday, no bounce               | Bearish PM|
| Market flat (±0.3%) at midday                      | No trade  |
| Strong sector rotation into close (e.g. banks up)  | Bullish PM|
| VN30F futures premium over cash index              | Bullish PM|
| VN30F futures discount under cash index            | Bearish PM|

---

## Setup & Entry Rules

| Parameter    | Value                                                   |
|--------------|---------------------------------------------------------|
| Timeframe    | 5-min chart                                             |
| Markets      | VN30F (primary), VN30 index stocks (VCB, BID, VHM, VIC)|
| Entry Window | 13:15 – 13:45 (first 30 min of Power Hour)             |
| Avoid        | After 14:15 (ATC volatility too unpredictable)          |

### Long Entry (Bullish Closing Drive)
1. Market/stock has been trending up all morning.
2. VWAP is upward sloping and price is above VWAP at 13:00.
3. After lunch dip (12:00–13:00), price reclaims VWAP at 13:15.
4. A 5-min candle closes above the 13:00 high (resumption signal).
5. Volume starts recovering toward closing levels.
6. **Entry:** Buy on the confirmed resumption candle.
7. **Stop Loss:** Below VWAP or below the 13:00–13:15 consolidation low.

### Short Entry (Bearish Closing Drive)
1. Market has been trending down all morning.
2. Price is below VWAP, VWAP sloping down.
3. Weak bounce at lunch → fails to reclaim VWAP.
4. After 13:15, price resumes below the 13:00 low.
5. **Entry:** Sell on the resumption candle close below 13:00 low.
6. **Stop Loss:** Above VWAP or above the 13:15 consolidation high.

---

## Exit Rules

- **Hard Time Exit:** Close ALL positions by **14:20** — no exceptions.
  - ATC (14:30–14:45) is unpredictable and has wide spreads.
- **Target:** Previous session closing price OR PDH/PDL.
- **Partial Exit (T1):** Close 50% at +0.5% gain.
- **Remainder:** Trail with 3-min trailing stop until 14:20 exit.
- **Quick Scalp Mode:** If entered at 13:15 and at +0.3% by 13:30 → close all, take the easy profit.

---

## VN30F Futures vs. Cash Spread Monitor

```
Premium = VN30F Price − VN30 Index × (1 + r × t/365)
  r = risk-free rate (~4.5% annual)
  t = days to expiry

Positive Premium → Futures overpriced → Bullish expectation
Negative Premium → Futures underpriced → Bearish expectation
```

Use futures premium/discount as an additional directional filter.

---

## Closing Drive Risk Management

| Rule              | Guideline                                      |
|-------------------|------------------------------------------------|
| Max Risk/Trade    | 0.75% of account equity                        |
| Hard Time Stop    | 14:20 — exit everything                        |
| Entry Window      | Only enter between 13:15–13:45                 |
| Avoid ATC         | Never hold into 14:30 ATC auction              |
| Max Trades        | 1–2 closing drive trades                       |
| Daily Loss Limit  | If already −1.5% on day, skip power hour trade |

---

## Day Type Classification

| Day Type          | Power Hour Strategy              |
|-------------------|----------------------------------|
| Strong Trend Day  | Ride the trend with trail stop   |
| Reversal Day      | Cautious, smaller size           |
| Inside Day (Flat) | Skip — no directional edge       |
| News-Driven Day   | Skip — fundamental override      |
| Options Expiry    | Increased volatility — use 0.5× size |

---

## Example Trade Log

```
Date:          2026-06-24 (VN30F July expiry week)
Symbol:        VN30F2607
Morning Trend: Up 1.2% by 12:00 (strong uptrend)
Lunch Dip:     Pulled back 0.4%, held above VWAP
13:00 High:    1,290
VWAP:          1,286 (price above VWAP at 13:15 ✓)
Entry:         1,291 (Long, 5-min close above 13:00 high at 13:20)
Stop:          1,284 (below VWAP)
T1:            1,297 (+6 pts, +0.46%) ← 50% closed at 13:45
Hard Exit:     1,301 (+10 pts) ← remaining 50% closed at 14:18
Result:        +WIN (captured closing drive to day's high)
```

---

## Notes & Improvements

- **Index rebalancing calendar:** Track quarterly index rebalancing dates (VN30, MSCI, FTSE) — closing drives on rebalancing days are far stronger and more predictable.
- **Foreign investor flow:** If foreign net buy is strong (available on HOSE data feed), it reinforces the bullish closing drive thesis.
- **Combine with VN30F/VN30 cash arbitrage:** If futures are trading at a large premium near close, futures may converge to cash → provides a shorting opportunity in futures.
- **Monthly expiry:** VN30F on expiry month is subject to final settlement price = average last 30 min — this creates strong convergence pressure that can be exploited.

---

## Summary Comparison: All 10 Strategies

| # | Strategy                  | Type            | Best Time     | Avg R:R |
|---|---------------------------|-----------------|---------------|---------|
| 1 | Opening Range Breakout    | Momentum        | 09:15–10:30   | 1:2     |
| 2 | VWAP Mean Reversion       | Mean Reversion  | 09:30–13:00   | 1:1.8   |
| 3 | EMA Crossover Scalp       | Momentum        | 09:30–13:30   | 1:1.8   |
| 4 | Gap Fill Fade             | Fade            | 09:05–11:00   | 1:1.5   |
| 5 | S/R Bounce                | Price Action    | 09:30–13:30   | 1:2     |
| 6 | Flag Continuation         | Momentum        | 09:30–12:00   | 1:2.5   |
| 7 | BB Squeeze Breakout       | Volatility      | 09:30–13:00   | 1:2     |
| 8 | RSI Divergence Reversal   | Reversal        | 10:00–13:30   | 1:1.8   |
| 9 | HOD/LOD Breakout          | Momentum        | 09:30–13:00   | 1:1.5   |
| 10| Power Hour Closing Drive  | Trend Following | 13:15–14:20   | 1:1.5   |

---

*Category: Trend Following / Closing Drive | Timeframe: Intraday (5-min) | Market: VN30F / HSX Stocks*
