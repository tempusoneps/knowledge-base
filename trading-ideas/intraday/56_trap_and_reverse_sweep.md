# 56 — The "Trap & Reverse" (Liquidity Sweep)

## Overview

Institutional algorithms often hunt for liquidity (pools of resting stop-loss orders) before initiating a large directional move. The **Trap & Reverse** strategy looks for instances where price breaks a major support or resistance level by just a few ticks—triggering retail stops and breakout traders—only to immediately reverse and surge in the opposite direction. 

---

## Concept

```
The Liquidity Sweep:
  Retail traders place their stop losses just below an obvious Support level.
  Breakout traders place their sell-stop entries just below the same level.
  Result = Massive pool of Sell orders sitting just below Support.
  
  Institutions need to Buy a large position. They push the price below Support to trigger this pool of Sell orders, giving them the liquidity they need to get filled without slippage.
  Once filled, they drive the price back up. The breakout traders are now trapped and forced to cover, adding buying pressure.
```

**Trade Logic:** Don't trade the breakout. Trade the failure of the breakout when price snaps back inside the range.

---

## Indicators Required

| Indicator      | Setting                      | Purpose                                  |
| -------------- | ---------------------------- | ---------------------------------------- |
| Support/Resist | Manual                       | Identify obvious liquidity pools         |
| Candlesticks   | 5-min chart                  | Spot the rejection tail (pin bar)        |
| Volume         | 20-bar MA                    | Confirm heavy volume on the sweep        |

---

## Setup & Entry Rules

| Parameter | Value                                          |
| --------- | ---------------------------------------------- |
| Timeframe | 5-min chart                                    |
| Markets   | VN30F, High Liquidity HSX Stocks               |
| Context   | Obvious daily or intraday Support/Resistance   |

### Long Entry (Support Sweep / Bear Trap)
1. **Identify the Level:** Draw a line at an obvious intraday Support (e.g., the Low of Day or a level tested multiple times).
2. **The Trap:** Price breaks below the Support level.
3. **The Sweep:** Volume spikes significantly as stop-losses trigger.
4. **The Trigger (Reversal):** The 5-min candle fails to hold below the level and closes back *above* the Support line, leaving a long lower wick (a Pin Bar or Hammer).
5. **Entry:** Go Long immediately on the close of the rejection candle.
6. **Stop Loss:** Just below the low of the rejection wick.

### Short Entry (Resistance Sweep / Bull Trap)
1. **Identify the Level:** Obvious Resistance (e.g., High of Day).
2. **The Trap:** Price breaks above Resistance.
3. **The Sweep:** Volume spikes as breakout buyers jump in.
4. **The Trigger:** The candle rejects and closes back *below* the Resistance line, leaving a long upper wick (Shooting Star).
5. **Entry:** Go Short on the close.
6. **Stop Loss:** Just above the high of the rejection wick.

---

## Exit Rules

- **Target 1:** The midpoint of the intraday range. Take 50%.
- **Target 2:** The opposite extreme of the range (e.g., if you bought the LOD sweep, target the HOD). Take 50%.
- **Failure:** If price reverses and breaks past the extreme of your rejection wick, the sweep was actually a genuine breakout -> Exit immediately.

---

## Filters

- [ ] **Crucial:** The rejection must be swift. If price hangs around below Support for 3 or 4 candles before finally crawling back above, it's not a liquidity sweep. A true sweep is a violent "V" shape on the 1-min or 5-min chart.
- [ ] Only trade sweeps of obvious, widely-watched levels. If you are the only one looking at a level, there is no liquidity pool there for institutions to hunt.

---

## Risk Management

| Rule             | Guideline                          |
| ---------------- | ---------------------------------- |
| Max Risk/Trade   | 1% of account equity               |
| Stop Placement   | Tightly beyond the sweep wick      |
| Min R:R          | 1:2.5                              |

---

## Edge & Statistics

- **Win rate:** 55-60%.
- **Edge:** You are trading alongside institutional order flow and against retail panic/greed. The R:R is excellent because the stop loss is very defined (the tip of the wick).

---

## Example Trade Log

```
Date:      2026-06-15
Symbol:    VN30F2607
Context:   Support established at 1,250 during the morning.
The Trap:  At 13:30, price drops sharply to 1,248. Volume is highest of the day.
The Trigger: The 5-min candle aggressively buys back up and closes at 1,251, leaving a 3-point lower wick.
Entry:     1,251 (Long)
Stop:      1,247.5 (Below the wick)
Target:    1,260 (Intraday VWAP/Midpoint)
Result:    Trapped shorts panic cover. Price surges to 1,262 by 14:15. +WIN (+9 pts).
```

---

## Notes & Improvements
- This is a core concept in "Smart Money Concepts" (SMC).
- If the sweep candle is extremely large, wait for a minor pullback into the wick (e.g., 50% retracement of the wick) to enter for a better R:R.

---
*Category: Smart Money / Reversal | Timeframe: Intraday (5-min) | Market: VN30F / HSX Stocks*
