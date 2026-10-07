# 66 — Open Equals High/Low (O=H / O=L) Trend Play

## Overview

In candlestick charting, when a session opens and immediately drives in one direction without ever looking back, it leaves a candle where the Open equals the High (O=H) or the Open equals the Low (O=L). On an intraday basis, if the first 15-minute or 30-minute candle forms a perfect O=H or O=L, it is a massive signal of institutional conviction. This strategy trades the continuation of this imbalance.

---

## Concept

```
Open = Low (Bullish Conviction):
  The stock opens at 09:15. It never ticks below the opening price.
  Institutions are buying aggressively from the very first second.
  This usually sets the tone for a massive Trend Up day.

Open = High (Bearish Conviction):
  The stock opens and immediately tanks. It never ticks above the open.
  Institutions are dumping at market price.
  Sets the tone for a Trend Down day.
```

**Trade Logic:** If the market was perfectly balanced, price would chop around the open. An O=H or O=L means there is an absolute imbalance of supply or demand. You must align with that flow.

---

## Indicators Required

| Indicator      | Setting                      | Purpose                                  |
| -------------- | ---------------------------- | ---------------------------------------- |
| Candlesticks   | 15-min or 30-min chart       | Identify the O=H or O=L structure        |
| VWAP           | Daily                        | Primary pullback entry level             |
| EMA            | 9-period on 5-min            | Secondary pullback entry level           |

---

## Setup & Entry Rules

| Parameter | Value                                          |
| --------- | ---------------------------------------------- |
| Timeframe | 15-min for context, 5-min for entry            |
| Markets   | VN30F, Major HSX Stocks                        |
| Context   | The first 15 to 30 minutes of the session      |

### Long Entry (Open = Low)
1. **The Signal:** Observe the first 15-min candle (09:15 - 09:30). The low of the candle must be exactly (or within 1-2 ticks of) the opening price.
2. **The Confirmation:** The candle must close as a strong green bar.
3. **The Entry (Aggressive):** Go Long immediately on the close of the 09:30 candle.
4. **The Entry (Conservative):** Wait for the first 5-min pullback to the 9-EMA or VWAP and buy the dip.
5. **Stop Loss:** Below the Open price (the LOD). If it breaks the open, the O=L thesis is destroyed.

### Short Entry (Open = High)
1. **The Signal:** First 15-min candle's high is exactly the open price.
2. **The Confirmation:** Closes as a strong red bar.
3. **Entry:** Go Short on close, or wait for pullback to 9-EMA/VWAP.
4. **Stop Loss:** Above the Open price (the HOD).

---

## Exit Rules

- **Target:** There are no predefined targets because O=H / O=L days are often the biggest trend days of the month.
- **Trailing Stop:** Trail the stop loss aggressively using the 15-min 9-EMA. As long as price closes above the 9-EMA, stay in the trade.
- **Time Stop:** Can hold until the ATC (14:30) to capture the maximum daily range.

---

## Filters

- [ ] **Crucial:** Ensure the volume on the first 15-minute candle is significantly higher than average. An O=L on dead volume means nothing.
- [ ] If the first 15-minute candle is massive (e.g., > 2% range), do NOT enter aggressively. The R:R to the stop loss (the open) is too skewed. You *must* wait for a pullback to the VWAP in this scenario.

---

## Risk Management

| Rule             | Guideline                          |
| ---------------- | ---------------------------------- |
| Max Risk/Trade   | 1% of account equity               |
| Stop Placement   | Hard stop at the Opening Price     |
| Sizing           | Standard size                      |

---

## Edge & Statistics

- **Win rate:** 65-70% for trend continuation.
- **Edge:** Identifying an O=H or O=L day early allows you to hold for massive intraday winners, as these days rarely experience deep counter-trend pullbacks.

---

## Example Trade Log

```
Date:      2026-06-25
Symbol:    VPB (HSX)
Context:   VPB opens at 18,000 at 09:15.
The Signal: At 09:30, the 15-min candle closes at 18,300. The low was exactly 18,000 (O=L). Volume is 3x average.
Entry:     Wait for pullback. At 10:00, price dips to 18,150 (touching 5-min 9-EMA). Go Long.
Stop:      17,950 (Below the Open)
Target:    Trail with 15-min 9-EMA.
Result:    VPB grinds up all day without ever closing below the 9-EMA. Exit at 14:25 at 18,900. +WIN (+750 pts).
```

---

## Notes & Improvements
- This is a very common scanner setup for professional day traders. Build a scanner that alerts you at exactly 09:31 for any VN30 stock where `Low == Open` or `High == Open`.

---
*Category: Momentum / Candlestick Math | Timeframe: Intraday (15-min) | Market: VN30F / VN30 Stocks*
