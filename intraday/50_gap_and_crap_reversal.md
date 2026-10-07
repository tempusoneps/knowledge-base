# 50 — The "Gap and Crap" (Morning Gap Reversal)

## Overview

A **Gap and Crap** (also known as a Gap Reversal or Fade the Gap) occurs when a stock opens significantly higher than its previous day's close due to overnight news, retail excitement, or pre-market manipulation, but immediately faces relentless selling pressure. Institutions use the artificially high opening price as liquidity to unload shares onto excited retail buyers. The strategy involves shorting the failure of the morning gap.

---

## Concept

```
The Setup:
  1. Stock gaps up > 2% at the open (ATO).
  2. Retail traders chase the gap, expecting a massive trend day.
  3. Institutions sell into this buying pressure.
  4. Price fails to make a new high after the first 5-15 minutes and breaks below the opening price.
  5. As retail buyers realize they are trapped, they panic sell, accelerating the move down to fill the gap.
```

**Trade Logic:** Gaps that are unsupported by true institutional accumulation will fail quickly. Fading the gap relies on the mechanical necessity of trapped buyers having to sell to cut their losses.

---

## Indicators Required

| Indicator      | Setting                      | Purpose                                  |
| -------------- | ---------------------------- | ---------------------------------------- |
| Gap Size       | > 2%                         | Ensure the gap is significant enough     |
| VWAP           | Daily                        | Important intraday support/resistance    |
| Volume         | 20-bar MA                    | Confirm the selling pressure             |

---

## Setup & Entry Rules

| Parameter | Value                                          |
| --------- | ---------------------------------------------- |
| Timeframe | 5-min chart                                    |
| Markets   | Volatile HSX Stocks, Mid/Small caps            |
| Context   | High-volume gap up at ATO (09:15)              |

### Short Entry (Fade the Gap)
1. **The Gap:** Stock opens at least 2% higher than yesterday's close.
2. **The Initial Push:** The first 5-min candle (09:15 - 09:20) is often green, or a Doji.
3. **The Weakness:** The stock fails to break the high of the first 5-min candle.
4. **The Trigger:** A 5-min candle closes **below the Opening Price (ATO price)**.
5. **Confirmation:** If price also breaks below the daily VWAP, the signal is extremely strong.
6. **Entry:** Go Short on the close below the Open/VWAP.
7. **Stop Loss:** Above the High of Day (HOD) established in the first 15 minutes.

---

## Exit Rules

- **Target 1:** The Half-Gap Fill (midpoint between today's open and yesterday's close). Take 50%.
- **Target 2:** The Full Gap Fill (yesterday's closing price). Take 40%.
- **Runner:** Trail the remaining 10% behind the 9-EMA in case it turns into a massive trend-down day.
- **Failure:** If price breaks back above the VWAP or Opening price and holds for >2 candles, the short thesis is wrong -> Exit.

---

## Filters

- [ ] **Crucial:** Do NOT short gaps driven by massive, undeniable fundamental news (e.g., a buyout offer, a surprise 500% earnings beat). These are "Runaway Gaps" and will destroy you.
- [ ] This strategy works best on exhaustion gaps (a gap up after a stock has already rallied for 3-4 days).
- [ ] Only trade gaps where the opening volume is exceptionally high, indicating a frenzy that can quickly turn to panic.

---

## Risk Management

| Rule             | Guideline                          |
| ---------------- | ---------------------------------- |
| Max Risk/Trade   | 0.75% of account equity            |
| Stop Placement   | Hard stop above the HOD. NO EXCEPTIONS. |
| Min R:R          | 1:2                                |

---

## Edge & Statistics

- **Win rate:** 55-60%.
- **Edge:** The psychological panic of trapped long buyers provides the fuel for the downside move. The target (Gap fill) is usually far away, offering excellent R:R.

---

## Example Trade Log

```
Date:      2026-06-22
Symbol:    NVL (HSX)
Context:   NVL gaps up 3.5% at the ATO (09:15) to 15,500 on vague rumors.
Setup:     First 5-min candle pushes to 15,650 but closes as a shooting star.
Trigger:   09:25 candle closes at 15,400 (Below the 15,500 open and below VWAP).
Entry:     15,400 (Short)
Stop:      15,700 (Above HOD)
Target:    14,950 (Yesterday's close / Full gap fill)
Result:    Rumor is faded. Stock grinds down all morning, hits 14,950 at 11:30. +WIN (+450 pts).
```

---

## Notes & Improvements
- This is the exact inverse of the "Gap and Go" strategy. You must read the first 15 minutes carefully to determine if the gap is being bought (Go) or sold (Crap).
- In Vietnam, execute this via T+0 (selling existing inventory on the gap up and buying back at the gap fill) or via VN30F if the entire index gaps up.

---
*Category: Reversal / Gap Play | Timeframe: Intraday (5-min) | Market: Volatile HSX Stocks*
