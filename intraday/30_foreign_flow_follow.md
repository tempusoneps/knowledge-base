# 30 — Foreign Investor Net Buy Flow Follow

## Overview

Foreign investors (FI) are the dominant force in the Vietnamese stock market, accounting for a significant portion of market cap and daily turnover. Their buy/sell patterns, visible in **real-time foreign net buy/sell data** published by HOSE, often precede large directional moves. When foreigners are aggressively net buying a specific stock intraday, following their flow provides a statistically positive edge.

---

## Concept

```
Foreign Net Buy = Foreign Buy Volume × Price − Foreign Sell Volume × Price

Published on:   HOSE official website, broker platforms (SSI, VNDIRECT, etc.)
Update frequency: Real-time during session (every few minutes)
Unit:           VND billion (tỷ đồng)

Signals:
  Strong FI Net Buy (> +50B VND in stock) → Institutional accumulation → Long
  Strong FI Net Sell (< −50B VND in stock) → Institutional distribution → Short/Avoid
```

**Why it works:** Foreign institutional investors (funds, ETFs) trade in large sizes, move markets, and tend to be "right" directionally over intraday horizons. Retail following their flow has a positive edge, especially on stocks with limited domestic institutional presence.

---

## Setup & Entry Rules

| Parameter    | Value                                                |
|--------------|------------------------------------------------------|
| Timeframe    | 5-min chart for entry                                |
| Markets      | Top 20 most foreign-traded HSX stocks                |
| Session      | 09:30 – 13:00 (FI most active in morning)            |
| Threshold    | Net buy > +30B VND for mid-cap; > +50B VND for large-cap |

### Long Entry (Strong FI Net Buying)
1. Monitor FI net buy data via broker platform or HOSE API.
2. A specific stock shows FI net buying > +30B VND by 10:00.
3. The stock price has not yet moved significantly (< +0.5% from open) — early stage.
4. Price is above VWAP and EMA9.
5. No fundamental negative news for the stock.
6. Enter Long on a 5-min candle close above the session high.
7. Stop Loss: Below VWAP or below the morning consolidation low.

### Avoid / Short Setup (Strong FI Net Selling)
1. FI net selling > −30B VND in first hour.
2. Stock shows price weakness (below VWAP).
3. Reduce exposure or avoid long; consider short if price breaks support.

---

## FI Data Sources (Vietnam)

| Source                    | Data Type                | Update Speed  |
|---------------------------|--------------------------|---------------|
| HOSE Official Website     | All stocks, net buy/sell | ~5 min delay  |
| SSI iBoard / Fireant      | VN30 + mid-cap           | Near real-time|
| VNDIRECT Trading Platform | Portfolio + market       | Near real-time|
| DNSE Entrade              | VN30 foreign flow        | Real-time     |
| Cafef.vn / StockBiz.vn    | End-of-day summary       | EOD           |

---

## Exit Rules

- **Target 1:** When FI net buy slows or reverses on intraday monitoring → close 60%.
- **Target 2:** Daily high or key resistance → close 40%.
- **FI Reversal Exit:** If FI net position flips to net sell during the session → exit immediately.
- **Time Stop:** Close by 13:30 (FI flow dries up near close often).
- **Hard Exit:** All positions by 14:15.

---

## Filters

- [ ] FI net buy must start in the **morning session** (09:15–11:00) to have time to develop.
- [ ] Confirm FI is buying the stock AND overall market (not just hedging one position).
- [ ] Check FI buy vs. total volume ratio: if FI is > 30% of total daily volume → very significant.
- [ ] Skip stocks near their **foreign ownership limit (room)** — FI can't buy more, fake signal.
- [ ] Skip if FI flow data has a delay >15 min (data quality matters).

---

## Vietnam-Specific: Foreign Ownership Room

```
Foreign Ownership Limit in Vietnam:
  Most stocks: 49% max foreign ownership
  Banking sector: 30% max
  Some sectors: 0% (restricted)

"Room" = Remaining space for foreign buying
If Room < 5%: Foreign can barely buy → FI buy data may be misleading → Skip
If Room > 15%: Plenty of room, genuine accumulation signal
```

---

## Risk Management

| Rule              | Guideline                            |
|-------------------|--------------------------------------|
| Max Risk/Trade    | 0.75% of account equity              |
| Stop Placement    | Below VWAP or morning low            |
| Max Trades/Day    | 2–3 FI flow trades                   |
| Min FI Threshold  | +30B VND minimum before entry        |
| Daily Loss Limit  | −1.5%                                |

---

## Edge & Statistics

- Win rate: **60–68%** when FI net buy > +50B VND in first hour.
- This edge is most pronounced in **emerging market bull cycles**.
- Best on: Stocks with >20% room remaining, no negative news, in uptrending sectors.
- Worst on: Thin stocks where FI buy is a relative anomaly but absolute size is small.

---

## Example Trade Log

```
Date:         2026-06-17
Symbol:       MWG (HSX)
FI Net Buy:   +65B VND by 09:50 (2nd highest FI buy of the day)
Stock Move:   Only +0.3% from open (early stage, not priced in)
VWAP:         62,500, price at 62,800 (above VWAP ✓)
Room:         FI room at 28% (plenty of space ✓)
EMA9:         Price above EMA9 ✓
Entry:        63,000 (Long, 5-min close above session high at 09:55)
Stop:         62,300 (below VWAP)
T1:           64,000 (near resistance) ← 60% at 10:30 (FI net buy slowing)
T2:           64,800 (daily high) ← 40% at 11:00
Result:       +WIN (+1.3%)
```

---

## Notes & Improvements

- Build a **real-time FI dashboard** using HOSE data API or screen-scraping broker platforms.
- Track FI flow per sector: if foreigners buying entire banking sector → sector rotation trade.
- Historical analysis: stocks with top 5 FI net buy today outperform next 3 days ~60% of time.
- **Contra trade**: stocks with largest FI net sell often bounce next day (oversold) — a swing trade angle.

---

*Category: Flow Following | Timeframe: Intraday (5-min) | Market: HSX Stocks (Foreign-Eligible)*
