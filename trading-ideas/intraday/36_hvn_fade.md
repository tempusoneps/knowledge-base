# 36 — High Volume Node (HVN) Fade

## Overview

In Volume Profile analysis, a **High Volume Node (HVN)** is a price level where a significant amount of trading volume occurred in the past (either earlier in the session or in recent days). HVNs represent areas of "fair value" consensus. Because many traders have established positions at these levels, price tends to slow down, consolidate, or reverse when it returns to an HVN. This strategy looks to fade momentum as price enters a prominent HVN.

---

## Concept

```
Volume Profile:
  HVN = Peak in the volume profile histogram (price level with heavy volume).
  LVN = Valley in the histogram (low volume).

Behavior:
  Price moving rapidly through LVNs acts like a vacuum.
  When price hits an HVN, it acts like a sponge or magnet.
  Momentum dies as orders are absorbed by traders defending or unwinding positions at their break-even point.
```

**Trade Logic:** Fade the move as price hits the HVN, anticipating a stall and a bounce back toward the origin of the move or the nearest LVN.

---

## Indicators Required

| Indicator      | Setting                      | Purpose                                  |
| -------------- | ---------------------------- | ---------------------------------------- |
| Volume Profile | Session or Multi-Day         | Identify prominent HVNs                  |
| RSI / Stoch    | 14-period                    | Confirm momentum exhaustion (overbought) |
| Candlesticks   | Price Action                 | Look for rejection wicks                 |

---

## Setup & Entry Rules

| Parameter | Value                                          |
| --------- | ---------------------------------------------- |
| Timeframe | 5-min chart                                    |
| Markets   | VN30F, Liquid VN30 stocks                      |
| Profile   | Composite profile (last 3-5 days) preferred    |

### Short Entry (Fade Rally into HVN)
1. **Identify HVN:** Locate a prominent HVN above current price from the past few sessions.
2. **Approach:** Price rallies aggressively toward the HVN.
3. **Exhaustion:** As price enters the HVN zone, momentum slows (candles get smaller, wicks appear).
4. **Trigger:** A bearish reversal candle (shooting star, engulfing) forms right at the HVN peak.
5. **Confirmation:** RSI is overbought (> 65) or showing bearish divergence.
6. **Entry:** Short on the close of the reversal candle.
7. **Stop Loss:** 1 ATR above the HVN zone.

### Long Entry (Fade Drop into HVN)
1. **Identify HVN:** Locate a prominent HVN below current price.
2. **Approach:** Price drops rapidly into the HVN.
3. **Exhaustion:** Bearish momentum stalls; lower wicks form.
4. **Trigger:** Bullish reversal candle forms at the HVN peak.
5. **Confirmation:** RSI oversold (< 35).
6. **Entry:** Long on close.
7. **Stop Loss:** 1 ATR below the HVN zone.

---

## Exit Rules

- **Target 1:** The nearest LVN (Low Volume Node) in the direction of the trade -> 50%
- **Target 2:** The starting point of the original aggressive move (mean reversion) -> 50%
- **Time Stop:** Close by 14:15.
- **Failure:** If price blasts straight through the HVN without stalling, the thesis is wrong (trend override) -> Exit if stopped.

---

## Filters

- [ ] Ensure the HVN is prominent (a clear peak, not a minor bump).
- [ ] Skip if the move into the HVN is driven by major breaking news.
- [ ] The best fades occur when price has traveled a long distance quickly before hitting the HVN (exhaustion).
- [ ] Do not try to fade small intraday HVNs; use multi-day HVNs for stronger reactions.

---

## Risk Management

| Rule             | Guideline                          |
| ---------------- | ---------------------------------- |
| Max Risk/Trade   | 1% of account equity               |
| Stop Placement   | 1 ATR beyond the HVN structure     |
| Min R:R          | 1:1.5                              |
| Max Trades/Day   | 2-3                                |

---

## Edge & Statistics

- **Win rate:** ~60% when relying on multi-day composite HVNs.
- Price almost always pauses at major HVNs, allowing for tight stops and quick break-even adjustments.

---

## Example Trade Log

```
Date:      2026-06-12
Symbol:    VN30F2607
Context:   Multi-day HVN identified at 1,280 (heavy trading area 2 days ago).
Action:    Price rallies from 1,265 to 1,279 rapidly at 10:30.
Rejection: Pin bar forms right at 1,280. RSI hits 72.
Entry:     1,279 (Short)
Stop:      1,284 (Above HVN structure)
Target:    1,272 (Nearest LVN / support)
Result:    Price bounces off HVN, hits target at 11:15. +WIN (+7 pts).
```

---

## Notes & Improvements
- HVNs are excellent targets for other strategies (e.g., if you are Long from a breakout, the next HVN above is your logical profit target).
- This strategy pairs perfectly with VWAP. If an HVN aligns with the daily VWAP, it is an extremely strong fade location.

---
*Category: Volume Profile / Mean Reversion | Timeframe: Intraday | Market: VN30F / HSX Stocks*
