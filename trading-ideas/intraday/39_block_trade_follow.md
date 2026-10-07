# 39 — Block Trade Follow (Tape Reading)

## Overview

In the Vietnamese market, institutional players often execute large orders (Block Trades or "Lệnh lớn") during continuous trading. While true block trades are negotiated off-exchange, institutions often split large orders and execute them on the active limit order book, creating sudden, massive volume spikes on a single price level. "Following the block" means identifying these aggressive, oversized market orders and trading in the direction of the institutional footprint.

---

## Concept

```
Tape Reading / Order Flow:
  Retail orders: Usually < 5,000 shares per tick.
  Institutional orders: Suddenly prints 100,000+ or 500,000+ shares taking the Ask (Aggressive Buy).

Signal:
  When an abnormally large market order lifts the offer (buys at Ask), it indicates urgency.
  If this occurs after a period of consolidation, it often triggers a momentum run as algorithms and retail traders jump on board.
```

**Trade Logic:** Detect aggressive, oversized volume prints that cross the spread, and ride the momentum wave they create.

---

## Indicators Required

| Indicator      | Setting                      | Purpose                                  |
| -------------- | ---------------------------- | ---------------------------------------- |
| Time & Sales   | Real-time tape (Order Flow)  | Spot aggressive block trades             |
| Volume         | Per-candle volume            | Confirm the spike visually               |
| VWAP           | Daily                        | Ensure trade aligns with intraday bias   |

---

## Setup & Entry Rules

| Parameter | Value                                          |
| --------- | ---------------------------------------------- |
| Timeframe | 1-min chart + Real-time Time & Sales (Tape)    |
| Markets   | VN30 Constituents, Mid-caps with catalyst      |
| Trigger   | Single trade size > 10x average trade size     |

### Long Entry (Aggressive Block Buy)
1. **Context:** Stock is consolidating or in a steady uptrend (above VWAP).
2. **The Signal:** Time & Sales shows a massive buy order(s) hitting the ASK (e.g., a print of 200k shares on a stock that usually trades 5k per print).
3. **Price Reaction:** Price immediately ticks up; the level the block bought at is defended.
4. **Entry:** Go Long immediately at market or place a limit order at the price of the block trade (the "Institutional Cost Basis").
5. **Stop Loss:** Just below the low of the 1-min candle where the block trade occurred.

### Short Entry (Aggressive Block Sell)
1. **Context:** Stock is weak, below VWAP.
2. **The Signal:** Massive sell order hits the BID.
3. **Price Reaction:** Price ticks down.
4. **Entry:** Go Short.
5. **Stop Loss:** Just above the high of the 1-min block candle.

---

## Exit Rules

- **Target 1:** Next intraday resistance/support level. Take 50%.
- **Trailing Stop:** These trades rely on immediate momentum. If the momentum stalls for more than 3-5 minutes, exit the trade. Trail stop tightly below 1-min higher lows.
- **Failure Exit:** If price drops BELOW the price where the massive buy block occurred, the institution is underwater and may puke the position -> EXIT IMMEDIATELY.

---

## Filters

- [ ] Block size must be visually anomalous on the tape (at least 10x normal size).
- [ ] Ensure the block was *aggressive* (market order crossing the spread), not a passive limit order getting filled.
- [ ] Avoid trading block prints that occur directly into major resistance levels.
- [ ] Skip late-day blocks (after 14:15) as they may be closing positions, not initiating new trends.

---

## Risk Management

| Rule             | Guideline                          |
| ---------------- | ---------------------------------- |
| Max Risk/Trade   | 0.5% - 0.75% of account equity     |
| Stop Placement   | Extremely tight (below the block candle) |
| Max Trades/Day   | Variable (depends on tape action)  |

---

## Edge & Statistics

- **Win rate:** 50-60%.
- **Edge:** The stop loss is exceptionally tight (often just 0.2% - 0.3%), allowing for massive R:R (1:3 or 1:4) when the momentum catches.

---

## Example Trade Log

```
Date:      2026-06-19
Symbol:    STB (HSX)
Context:   Consolidating at 30,000 for 45 minutes.
Signal:    At 10:15, tape prints consecutive buys hitting the Ask: 150k, 200k, 300k shares at 30,050.
Entry:     30,050 (Long, bought alongside the tape)
Stop:      29,950 (Below the 1-min candle low)
Target:    Trail stop.
Result:    Price runs quickly to 30,600 as volume pours in. Sold at 30,500. +WIN.
```

---

## Notes & Improvements
- Requires a broker terminal with a fast, unaggregated Time & Sales window (e.g., SSI iBoard Pro, Fireant Pro).
- Can be automated via API by filtering real-time tick data for anomalous trade sizes at the bid/ask.

---
*Category: Order Flow / Tape Reading | Timeframe: 1-min / Tick | Market: HSX Stocks*
