# 61 — The "Fade the News" (Sell the Fact)

## Overview

A classic market adage is "Buy the rumor, sell the news." Often, by the time a positive news catalyst is officially announced, institutional players have already accumulated their positions over the preceding days or weeks. When retail traders rush in to buy the official headline, institutions use that liquidity to exit their positions. The **Fade the News** strategy looks for an intraday price spike exactly on a major news release, and fades (shorts) the inevitable pullback.

---

## Concept

```
The Setup:
  1. A stock has been in a steady uptrend for weeks leading up to an expected event (e.g., earnings, dividend announcement, contract win).
  2. The news officially hits the wires during the trading day (or overnight).
  3. The stock spikes aggressively on high volume (Retail buying).
  4. The price suddenly hits a brick wall and fails to push higher despite the massive volume (Institutional selling/distribution).
  5. The stock reverses and wipes out the news spike.
```

**Trade Logic:** You are not betting that the news is bad; you are betting that the news is already fully priced in, and the institutional unloading will overwhelm the late retail buying.

---

## Indicators Required

| Indicator      | Setting                      | Purpose                                  |
| -------------- | ---------------------------- | ---------------------------------------- |
| Real-time News | CafeF, NDH, Bloomberg        | Pinpoint the exact catalyst              |
| Volume         | 20-bar MA                    | Confirm the climax/exhaustion volume     |
| Price Action   | 5-min chart                  | Spot the reversal candle                 |

---

## Setup & Entry Rules

| Parameter | Value                                          |
| --------- | ---------------------------------------------- |
| Timeframe | 5-min chart                                    |
| Markets   | Individual HSX Stocks                          |
| Context   | Stock must have rallied *prior* to the news    |

### Short Entry (Sell the Fact)
1. **The Catalyst:** A major positive news headline drops for the stock.
2. **The Climax Spike:** The stock spikes aggressively (e.g., +2% to +4% within minutes).
3. **The Wall (Exhaustion):** The stock hits a resistance level and forms a massive upper wick (Shooting Star) on the 5-min chart. Volume is the highest of the day.
4. **Trigger:** The next 5-min candle breaks below the low of the Shooting Star candle.
5. **Entry:** Go Short on the break of the low.
6. **Stop Loss:** Just above the high of the news spike.

*(Note: The exact reverse applies for bad news -> "Buy the Fact". If a stock has crashed for weeks on rumors of bad earnings, and the bad earnings are finally released, it often spikes down and then rips higher).*

---

## Exit Rules

- **Target 1:** The base of the news spike (where the price was immediately before the headline hit). Take 50%.
- **Target 2:** The Daily VWAP. Take remaining 50%.
- **Failure:** If price breaks above the high of the news spike and holds, the news is genuinely repricing the company (e.g., a buyout offer). Exit immediately.

---

## Filters

- [ ] **Crucial:** Did the stock rally for weeks *before* this news? If the news is a complete, 100% unforeseeable surprise (like a sudden M&A announcement), **DO NOT FADE IT**. The strategy only works when the event was expected and priced in.
- [ ] If the news spike happens on low volume, stay away. You need massive volume to confirm that retail is exhausted and institutions are unloading.

---

## Risk Management

| Rule             | Guideline                          |
| ---------------- | ---------------------------------- |
| Max Risk/Trade   | 0.75% of account equity            |
| Stop Placement   | Strict stop above the climax high  |
| Min R:R          | 1:2                                |

---

## Edge & Statistics

- **Win rate:** 55-65% on highly anticipated scheduled events (Earnings, Dividend dates).
- **Edge:** Market psychology. Retail traders consistently underestimate how efficient the market is at pricing in expectations.

---

## Example Trade Log

```
Date:      2026-06-12
Symbol:    FPT (HSX)
Context:   FPT has rallied 15% over 3 weeks heading into its Q2 earnings report.
The News:  At 10:30, FPT reports record profits (beating expectations).
The Spike: Stock spikes instantly from 135,000 to 138,000.
The Wall:  10:35 candle leaves a huge upper wick. Volume is 4x average.
Trigger:   10:40 candle breaks below 136,500 (low of the climax candle).
Entry:     136,500 (Short)
Stop:      138,200 (Above the spike)
Target:    135,000 (Base of the spike)
Result:    Institutions unload into the retail hype. Hits target at 11:15. +WIN (+1,500 pts).
```

---

## Notes & Improvements
- This is a very common play during the Vietnamese "Earnings Season" (January, April, July, October). Mark your calendar for when major companies report.

---
*Category: Event Driven / Mean Reversion | Timeframe: Intraday (5-min) | Market: Individual HSX Stocks*
