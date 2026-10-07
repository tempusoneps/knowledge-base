# 40 — Parabolic Short (Exhaustion Top Fade)

## Overview

A **Parabolic Move** occurs when a stock's price accelerates upwards so aggressively that the trendline curves vertically (like a parabola). These moves are driven by extreme FOMO, short-covering panics, or rumor-based buying. They are inherently unsustainable. The "Parabolic Short" strategy waits for the momentum to break—signaling that the last buyer has bought—and shorts the ensuing rapid collapse.

---

## Concept

```
Phase 1: Acceleration. Price goes up 2%, then 4%, then 7% in a matter of hours.
Phase 2: Climax. Massive volume spike, huge vertical candle.
Phase 3: The Break. Price stalls, makes a lower high on the 1-min/5-min chart, or breaks a steep micro-trendline.
Phase 4: Collapse. Price drops rapidly as late buyers panic and shorts pile in.
```

**Trade Logic:** Do not short just because it's high. Short only when the *rate of ascent* breaks and the backside of the move is confirmed.

---

## Indicators Required

| Indicator      | Setting                      | Purpose                                  |
| -------------- | ---------------------------- | ---------------------------------------- |
| Trendlines     | Manual                       | Track the accelerating angle of ascent   |
| Volume         | 20-bar MA                    | Identify the climax volume spike         |
| VWAP           | Daily                        | Ultimate target for the mean reversion   |

---

## Setup & Entry Rules

| Parameter | Value                                          |
| --------- | ---------------------------------------------- |
| Timeframe | 1-min for entry, 5-min for context             |
| Markets   | Highly volatile HSX/HNX mid/small caps         |
| Context   | Stock is up > 5% intraday on steep angle       |

### Short Entry (Backside of Parabola)
1. **Identify the Parabola:** Stock is up >5% intraday. The angle of ascent has increased at least twice (e.g., 30 deg -> 50 deg -> 80 deg vertical).
2. **Climax:** Look for a massive volume spike on a wide-range green candle.
3. **The Stall:** Price fails to make a new high on the next 1-2 candles.
4. **Trigger (The Break):** Draw a steep trendline under the final vertical push. **Enter Short when a 1-min candle closes below this trendline.**
5. *Alternative Trigger:* Enter Short when the stock makes its first **Lower High** on the 1-min chart after the climax.
6. **Stop Loss:** Just above the High of Day (HOD) climax peak.

---

## Exit Rules

- **Target 1:** The first major consolidation level built on the way up. Take 50%.
- **Target 2:** VWAP. Parabolic moves almost always revert to VWAP eventually. Take remaining 50%.
- **Time Stop:** Close by end of day. Do not hold overnight (short squeeze risk).
- **Failure:** If price breaks above the HOD stop loss, exit immediately. Never average up on a short.

---

## Filters

- [ ] **NEVER Front-run:** Do not short a stock while it is still making higher highs. Wait for the backside (the break of the trendline or a lower high).
- [ ] Avoid shorting stocks with low float/shares outstanding (very prone to being manipulated and squeezed).
- [ ] Ensure your broker has borrow available for the specific stock before planning the trade. (Vietnam context: relies on specific broker margin pools or derivative equivalents if trading VN30F).

---

## Risk Management

| Rule             | Guideline                          |
| ---------------- | ---------------------------------- |
| Max Risk/Trade   | 0.5% of account equity (High risk) |
| Stop Placement   | Hard stop above HOD. NO EXCEPTIONS.|
| Min R:R          | 1:3                                |

---

## Edge & Statistics

- **Win rate:** 45-55%.
- **Edge:** The R:R is massive. When a parabola breaks, it falls much faster than it rose. A 1% stop loss can easily yield a 4-5% gain.

---

## Example Trade Log

```
Date:      2026-06-02
Symbol:    DIG (HSX)
Context:   Stock goes parabolic on rumors, up 6% by 10:30.
Climax:    10:35 candle spikes to 28,500 on highest volume of the day.
Trigger:   At 10:42, price fails to break 28,500 (lower high at 28,400) and breaks the steep 1-min trendline at 28,200.
Entry:     28,200 (Short)
Stop:      28,550 (Above HOD)
Target:    27,000 (VWAP)
Result:    Late buyers panic. Price collapses to 27,200 by 11:30. +WIN (+1,000 pts).
```

---

## Notes & Improvements
- This is one of the most psychologically difficult strategies. It requires extreme discipline to honor the stop loss.
- In the Vietnamese market, true short selling of stocks is restricted. This strategy is applied practically via **Shorting VN30F** when the index goes parabolic, or via **T+0** selling if you already hold long inventory and want to exit at the absolute top.

---
*Category: Mean Reversion / Momentum | Timeframe: 1-min / 5-min | Market: VN30F / Volatile Stocks*
