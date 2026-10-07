# 05 — Support & Resistance Level Bounce

## Overview

Price gravitates toward and respects key horizontal support/resistance levels. When price approaches a well-tested S/R level intraday and shows a rejection reaction, a bounce trade in the opposite direction offers excellent R:R. This is a discretionary-meets-rules-based approach anchored in price action.

---

## Concept

```
Support Level:    Previous swing low, round numbers, prior day low
Resistance Level: Previous swing high, round numbers, prior day high

Bounce Long:  Price touches Support → Rejection → Buy
Bounce Short: Price touches Resistance → Rejection → Sell
```

The more times a level has been tested and held, the stronger it is. **Fresh untested levels** from the prior 1–5 days are the most reliable intraday.

---

## Level Identification (Pre-Market Prep)

Before market open, identify and mark:

| Level Type              | Where to Find It                          |
|-------------------------|-------------------------------------------|
| Prior Day High (PDH)    | Yesterday's session high                  |
| Prior Day Low (PDL)     | Yesterday's session low                   |
| Prior Day Close (PDC)   | Often acts as magnet                      |
| Round Numbers           | Multiples of 100, 500, 1000 (e.g. 1,300)  |
| Weekly Open             | Monday's open price                       |
| Overnight Gap Levels    | Pre-market high/low if applicable         |
| Pivot Points            | Classic Pivot = (H+L+C)/3                 |

---

## Setup & Entry Rules

| Parameter    | Value                                          |
|--------------|------------------------------------------------|
| Timeframe    | 5-min chart for entry; 15-min for level context|
| Markets      | VN30F, VCB, BID, VHM, MSN (liquid, large-cap) |
| Session      | 09:30 – 13:30                                  |

### Long Bounce (Support)
1. Price approaches a pre-identified support level.
2. First touch: price wicks through the level but **closes above** it.
3. Reversal confirmation: next candle opens and moves up (bullish momentum).
4. Optional: RSI < 40, or bullish divergence on MACD.
5. Enter Long on confirmation candle close.
6. Stop Loss: 1 ATR below the support level.

### Short Bounce (Resistance)
1. Price approaches a pre-identified resistance level.
2. First touch: price wicks through but **closes below** it.
3. Confirmation: next candle opens and moves down.
4. Optional: RSI > 60, or bearish divergence.
5. Enter Short on confirmation candle close.
6. Stop Loss: 1 ATR above the resistance level.

---

## Exit Rules

- **Target 1:** Midpoint to the next opposite S/R level (50% position closed).
- **Target 2:** Next major S/R level (50% position closed).
- **Trail Stop:** After T1, trail stop to break-even then follow price with a 2-candle trail.
- **Time Exit:** Close all by 14:00.
- **Failure:** If price closes decisively through the S/R level → immediate exit.

---

## Level Quality Score

Rate each level before trading it:

| Criteria                               | Score |
|----------------------------------------|-------|
| Level tested 3+ times previously       | +3    |
| Round number coincides                 | +2    |
| PDH or PDL                             | +2    |
| Weekly / Monthly level                 | +3    |
| Less than 3 days old (fresh)           | +2    |
| Confluence with VWAP                   | +2    |
| **Minimum score to trade:**            | **7** |

---

## Filters

- [ ] Do not trade at a level that has been tested more than 5× in short time (likely to break).
- [ ] Skip if price approaches the level with extreme momentum (breakout, not bounce).
- [ ] Avoid during lunch hour (12:00–13:00) — lower liquidity, fakeouts common.
- [ ] Confirm broader market direction supports the bounce direction.

---

## Risk Management

| Rule              | Guideline                     |
|-------------------|-------------------------------|
| Max Risk/Trade    | 1% of account equity          |
| Stop Placement    | 1 ATR beyond the S/R level    |
| Max Levels/Day    | Trade max 3 levels per day    |
| Daily Loss Limit  | −2% → stop trading            |

---

## Example Trade Log

```
Date:         2026-06-12
Symbol:       VN30F2607
Level:        1,260 (PDL from June 11, also round number)
Level Score:  PDL +2, Round number +2, Fresh +2, VWAP confluence +2 = 8 ✓
Action:       Price wicks to 1,258, closes at 1,261 (hammer candle)
Entry:        1,262 (Long on confirmation candle)
Stop:         1,254 (1 ATR = 6 pts below level)
T1:           1,274 (+12 pts) ← 50% closed
T2:           1,285 (+23 pts) ← 50% closed
Result:       +WIN
```

---

## Notes & Improvements

- Build a **daily level sheet** each morning before open — take 15 minutes to mark all key levels.
- Use a **multi-timeframe approach**: if the 1H chart also shows an S/R at the same price, double the weight.
- Consider **Options flow** (if available) near key levels as additional confirmation.
- Track level "reliability score" per symbol over time to refine level selection.

---

*Category: Price Action | Timeframe: Intraday | Market: VN30F / HSX Stocks*
