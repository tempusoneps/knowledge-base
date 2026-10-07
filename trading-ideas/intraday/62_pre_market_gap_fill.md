# 62 — The Pre-Market Gap Fill (ATO Play)

## Overview

In the Vietnamese market, the **ATO (At The Open)** session (09:00 - 09:15) determines the opening price based on order matching. Sometimes, overnight sentiment pushes the theoretical ATO price very high or very low, but institutional algorithms will step in just before 09:15 to push the price back toward yesterday's close. If the stock still gaps, it often spends the first 30 minutes of continuous trading (09:15 - 09:45) reversing to "fill" that overnight gap.

---

## Concept

```
The Logic:
  Gaps represent a sudden imbalance in supply and demand caused by illiquidity (the market being closed).
  Once the market opens and liquidity returns, the market often seeks to re-test the prices that were "skipped" over during the gap.
  "Filling the Gap" means price returns to the previous day's close.
```

**Trade Logic:** Bet against small-to-moderate morning gaps that lack a strong fundamental catalyst, aiming for a reversion to yesterday's closing price.

---

## Indicators Required

| Indicator      | Setting                      | Purpose                                  |
| -------------- | ---------------------------- | ---------------------------------------- |
| Gap Monitor    | > 0.5% but < 2.0%            | Identify the target gap                  |
| Price Line     | Previous Day Close (PDC)     | The Target                               |
| Volume         | 20-bar MA                    | Ensure the gap push is exhausting        |

---

## Setup & Entry Rules

| Parameter | Value                                          |
| --------- | ---------------------------------------------- |
| Timeframe | 5-min chart                                    |
| Markets   | VN30F, High Liquidity HSX Stocks               |
| Context   | The first 30 minutes of continuous trading     |

### Short Entry (Filling a Gap UP)
1. **The Gap:** Stock opens (at 09:15) > 0.5% higher than yesterday's close, but NO major news catalyst exists.
2. **The Exhaustion:** The first 1-2 5-min candles try to push higher but form upper wicks (rejection) or small Dojis. Volume is average, not exceptional.
3. **Trigger:** A 5-min candle breaks below the low of the 09:15 opening candle.
4. **Entry:** Go Short on the break.
5. **Stop Loss:** Above the High of Day (the peak of the initial push).

### Long Entry (Filling a Gap DOWN)
1. **The Gap:** Stock opens > 0.5% lower than yesterday's close without major news.
2. **The Exhaustion:** The first few candles reject lower prices (long lower wicks).
3. **Trigger:** A 5-min candle breaks above the high of the 09:15 opening candle.
4. **Entry:** Go Long on the break.
5. **Stop Loss:** Below the Low of Day.

---

## Exit Rules

- **Target 1:** The Half-Gap Fill (midpoint between today's open and yesterday's close). Take 50%.
- **Target 2:** The Full Gap Fill (Yesterday's Close / PDC line). Take 50%.
- **Time Stop:** The gap fill should happen relatively quickly (before 10:30). If price chops sideways for an hour, the gap is likely going to hold. Exit at break-even.

---

## Filters

- [ ] **Crucial:** Avoid "Runaway Gaps" (> 2.5% gaps with massive volume). These gaps often *never* fill on the same day and will crush a counter-trend trader.
- [ ] Only fade gaps that are "unwarranted" by the news cycle.
- [ ] Best used on range-bound market days. If the daily chart is in a roaring uptrend, fading a gap up is much riskier.

---

## Risk Management

| Rule             | Guideline                          |
| ---------------- | ---------------------------------- |
| Max Risk/Trade   | 1% of account equity               |
| Stop Placement   | Beyond the HOD/LOD of the morning  |
| Min R:R          | 1:1.5                              |

---

## Edge & Statistics

- **Win rate:** 55-65% on moderate (0.5% - 1.5%) gaps without news.
- **Edge:** Statistically, over 60% of small, non-news gaps fill within the first two hours of trading on major equity indices.

---

## Example Trade Log

```
Date:      2026-06-04
Symbol:    VN30F2607
Context:   VN30F closed yesterday at 1,250. Opens today at 1,258 (Gap UP, no major news).
Action:    09:15 to 09:25, price pushes to 1,260 but forms two Doji candles.
Trigger:   09:30 candle closes a solid red bar, breaking below the 09:15 open price.
Entry:     1,257 (Short)
Stop:      1,261 (Above the HOD)
Target:    1,250 (Yesterday's close)
Result:    Steady selling pressure fills the gap. Hits 1,250 at 10:15. +WIN (+7 pts).
```

---

## Notes & Improvements
- Keep a spreadsheet tracking the "Gap Fill Percentage" of the VN30F. (How many gaps > 5 points fill on the same day?). This gives you statistical confidence to take the trade.

---
*Category: Mean Reversion / Gap Fill | Timeframe: Intraday (5-min) | Market: VN30F / HSX Stocks*
