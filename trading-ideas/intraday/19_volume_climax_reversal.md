# 19 — Volume Climax Reversal

## Overview

A **Volume Climax** occurs when a stock experiences an extraordinary spike in volume — often 3–5× the average — accompanied by a wide-range price candle. This represents a final burst of panic selling (climax low) or euphoric buying (climax top), where the last weak hands capitulate and institutional buyers/sellers absorb the order flow. The subsequent reversal from a climax can be swift and powerful.

---

## Concept

```
Climax Sell (Bottom):
  → Panic selling → Volume spike 3–5× normal
  → Wide down candle (often a hammer or long wick)
  → Institutions absorb supply at extreme low price
  → Price reverses sharply

Climax Buy (Top):
  → FOMO buying → Volume spike 3–5× normal
  → Wide up candle, often closes near its HIGH
  → But next candle: price gaps down or reverses
  → Last buyers trapped

Signals:
  Volume Ratio = Current Volume / 20-bar Average Volume
  Climax threshold: Volume Ratio > 3.0
```

---

## Indicators Required

| Indicator     | Setting         | Purpose                               |
|---------------|-----------------|---------------------------------------|
| Volume        | Raw + 20-bar MA | Detect climax (>3× average)           |
| Volume Ratio  | Current/MA(20)  | Quantify climax intensity             |
| Candle        | Visual          | Wide-range + wick = absorption signal |
| RSI           | 14-period       | Extreme level confirmation            |
| VWAP          | Daily           | Trend context and target              |

---

## Setup & Entry Rules

| Parameter    | Value                                                |
|--------------|------------------------------------------------------|
| Timeframe    | 5-min chart                                          |
| Markets      | Any liquid HSX stock, VN30F during news events       |
| Session      | Any time, but most common 09:15–10:30 and 13:00–14:00|
| Threshold    | Volume Ratio > 3.0 on climax candle                  |

### Long Entry (Climax Sell Reversal)
1. Volume on the current 5-min candle is > 3× the 20-bar average.
2. The candle is a **wide-range DOWN candle** with a lower wick (absorption).
3. RSI < 30 (oversold context).
4. Price is near a key support level (S1, PDL, or VWAP lower band).
5. **Entry:** Enter Long on the **NEXT candle** after the climax candle (wait for confirmation).
6. Confirmation: Next candle opens flat or up, not continuing down.
7. Stop Loss: Below the climax candle low.

### Short Entry (Climax Buy Reversal)
1. Volume > 3× average on a wide-range UP candle.
2. Candle closes near its HIGH (buyers exhausted).
3. RSI > 70.
4. Price at key resistance.
5. Enter Short on the **next candle** after confirmation of reversal.
6. Stop Loss: Above the climax candle high.

---

## Exit Rules

- **Target 1:** VWAP (for climax from extreme) → close 70%.
- **Target 2:** Prior consolidation or opposite S/R → close 30%.
- **Speed:** Climax reversals move fast — take profits quickly.
- **Failure:** If next candle continues in the climax direction → no entry (trend, not exhaustion).
- **Time Stop:** Close within 1–2 hours of entry.

---

## Filters

- [ ] Volume ratio must be **> 3×** — lower ratios are not true climaxes.
- [ ] Climax candle must have a **visible wick** (shows rejection/absorption).
- [ ] Skip if this is a news-driven move that may continue (e.g., earnings, material disclosure).
- [ ] Require S/R confluence near the climax price.
- [ ] Do not average into a climax — wait for the next candle to confirm reversal first.

---

## Risk Management

| Rule              | Guideline                              |
|-------------------|----------------------------------------|
| Max Risk/Trade    | 1% of account equity                   |
| Stop Placement    | Beyond climax candle extreme           |
| R:R               | 1:2 minimum (climax moves are large)   |
| Trade Size        | Can use larger size — well-defined stop|
| Daily Loss Limit  | −2%                                    |

---

## Edge & Statistics

- Win rate: **60–70%** when all filters applied (S/R + RSI + volume threshold).
- The stop loss is large (climax candle range), but the move after is also large.
- Best on: Individual stocks with specific catalysts or market-wide panic sessions.
- Worst on: Trending momentum stocks where climax volume is just continuation, not reversal.

---

## Example Trade Log

```
Date:         2026-06-06
Symbol:       NVL (HSX)
Context:      Stock dropped 4% pre-session on developer news
Climax Candle: 09:20 — Volume 5.2× average, wide down candle with long lower wick
RSI:          22 (oversold) ✓
S/R:          45,000 = strong prior support ✓
Price:        45,200 close on climax candle (wick to 44,800)
Next Candle:  Opens at 45,300, moves up → confirmation ✓
Entry:        45,400 (Long)
Stop:         44,750 (below climax wick)
T1:           47,200 (VWAP) ← 70% closed
T2:           48,500 (prior S/R) ← 30% closed
Result:       +WIN
```

---

## Notes & Improvements

- Combine with **T+0 same-day trading**: climax reversal stocks are ideal T+0 long setups (buy at panic, sell the same day bounce).
- Build a real-time **Volume Ratio Alert** system: alert when any VN30 constituent hits 3× volume within a 5-min candle.
- Study each climax: classify as "true reversal" vs "continuation" to build a predictive model.
- After a climax low reversal, the stock often tests the climax low again the next day — watch for a double-bottom setup.

---

*Category: Reversal | Timeframe: Intraday (5-min) | Market: VN30F / HSX Stocks*
