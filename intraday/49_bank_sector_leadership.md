# 49 — Bank Sector Leadership Play

## Overview

In the Vietnamese stock market (HOSE), the Banking sector accounts for over 30% of the total market capitalization. Because of this massive weighting, the VN-Index and VN30 Index are effectively chained to the banking sector. The **Bank Sector Leadership Play** uses the price action of the top 3 banks (usually VCB, BID, CTG or MBB) as a leading indicator to trade the VN30F futures contract or highly correlated mid-cap stocks.

---

## Concept

```
The Correlation:
  If VCB and BID are trending strongly upwards, the VN30F CANNOT sustain a downtrend. It will be pulled up.
  If the top banks are hitting resistance and reversing, the broader market will likely follow.

The Signal:
  Monitor the "Big 3" banks on a 1-minute chart.
  When they exhibit a synchronized breakout or breakdown, use that as the fundamental catalyst to enter a trade on the VN30F or a high-beta stock.
```

**Trade Logic:** Instead of purely reading the chart of the VN30F, you read the chart of its heaviest underlying components. The underlying stocks often move slightly *before* the futures fully price in the move due to index calculation lag and liquidity differences.

---

## Indicators Required

| Indicator      | Setting                      | Purpose                                  |
| -------------- | ---------------------------- | ---------------------------------------- |
| Watchlist      | VCB, BID, CTG, MBB, TCB      | Track the leading sector                 |
| Price Action   | Breakouts / Breakdowns       | Identify synchronized sector moves       |
| VN30F Chart    | 1-min or 5-min               | Execution vehicle                        |

---

## Setup & Entry Rules

| Parameter | Value                                          |
| --------- | ---------------------------------------------- |
| Timeframe | 1-min / 5-min chart                            |
| Markets   | Execution on VN30F                             |
| Context   | Best during morning session (09:15 - 11:00)    |

### Long Entry (Synchronized Bank Breakout)
1. **Monitor:** Watch the top 3-5 bank stocks.
2. **The Tell:** At least 2 of the top banks (e.g., VCB and CTG) simultaneously break above their intraday High of Day (HOD) or a major resistance level.
3. **Check Execution Vehicle:** Look at the VN30F. If it is lagging slightly or just starting to break its own resistance, you have an edge.
4. **Entry:** Go Long VN30F immediately at market.
5. **Stop Loss:** Below the most recent 1-min swing low on the VN30F.

### Short Entry (Synchronized Bank Breakdown)
1. **Monitor:** Watch the top banks.
2. **The Tell:** At least 2 of the top banks break below their VWAP or Low of Day (LOD) simultaneously with increasing volume.
3. **Check Execution Vehicle:** Check VN30F.
4. **Entry:** Go Short VN30F at market.
5. **Stop Loss:** Above the most recent 1-min swing high.

---

## Exit Rules

- **Target 1:** Scalp 3-5 points on the VN30F. Take 50%.
- **Trailing Stop:** Trail the remaining 50% using the 9-EMA on the VN30F 5-min chart.
- **Divergence Exit:** If the banks hit a resistance level and stall, but your VN30F trade is still running, exit the trade. The underlying components drive the index, not vice versa.

---

## Filters

- [ ] **Crucial:** The move in the banks MUST be synchronized. If VCB is up 2% but BID is down 1%, the sector is mixed and the signal is invalid.
- [ ] Skip if the bank move is driven by a stock-specific rumor (e.g., a specific bank's dividend announcement). You want macroeconomic or broad sector flow.
- [ ] Be cautious if the Real Estate sector (VHM, VIC) is moving aggressively in the opposite direction, as they can cancel out the Bank sector's weight on the index.

---

## Risk Management

| Rule             | Guideline                          |
| ---------------- | ---------------------------------- |
| Max Risk/Trade   | 1% of account equity               |
| Stop Placement   | Based on the VN30F chart structure |
| Min R:R          | 1:1.5                              |

---

## Edge & Statistics

- **Win rate:** 60-65% when the sector synchronization is clear.
- **Edge:** You are trading based on the mathematical reality of the index weighting, giving you a slight predictive advantage over traders looking only at the futures chart.

---

## Example Trade Log

```
Date:      2026-06-12
Symbol:    VN30F2607
Monitor:   10:15 - VCB breaks HOD (90,000). BID simultaneously breaks HOD (48,000).
Context:   VN30F is consolidating just below its HOD at 1,270.
Entry:     1,270.5 (Long VN30F, anticipating the bank weight will drag it through resistance)
Stop:      1,268.0 (Below 1-min consolidation)
Target:    1,275 (Scalp target) -> Trailed out at 1,278.
Result:    VN30F breaks out 30 seconds after the banks. Hits target at 10:25. +WIN (+7.5 pts).
```

---

## Notes & Improvements
- Create a custom composite chart or index in your trading software that aggregates the price of the top 5 banks to track the sector momentum as a single line.

---
*Category: Order Flow / Relative Strength | Timeframe: 1-min/5-min | Market: VN30F (Based on HSX Banks)*
