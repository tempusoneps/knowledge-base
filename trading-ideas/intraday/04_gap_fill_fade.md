# 04 — Gap Fill Fade

## Overview

When a stock or index opens with a significant gap up or gap down versus the previous day's close, price has a strong statistical tendency to "fill" part or all of that gap during the intraday session. This strategy fades the gap direction — selling gap-ups, buying gap-downs — targeting the gap fill level.

---

## Concept

```
Gap Up:   Today's Open > Yesterday's Close  → Fade → Short
Gap Down: Today's Open < Yesterday's Close  → Fade → Long
Gap Fill: Price returns to Yesterday's Close level
```

**Gap Fill Probability (historical general reference):**

| Gap Size       | Fill Probability |
|----------------|-----------------|
| 0.3% – 0.8%    | ~75–80%          |
| 0.8% – 1.5%    | ~60–65%          |
| 1.5% – 3.0%    | ~45–55%          |
| > 3.0%         | ~25–35%          |

Small-to-medium gaps fill with high probability. Large gaps (news-driven) rarely fill on the same day.

---

## Setup & Entry Rules

| Parameter    | Value                                                  |
|--------------|--------------------------------------------------------|
| Timeframe    | 5-min chart                                            |
| Markets      | VN30F, individual HSX/HNX stocks with liquid volume    |
| Gap Range    | 0.3% – 1.5% (sweet spot for high fill probability)     |
| Entry Window | 09:05 – 09:20 after open stabilizes                   |

### Long Entry (Gap Down Fill)
1. Stock gaps down 0.3–1.5% from previous close.
2. First 5-min candle shows bullish body (buyers absorbing the gap).
3. Volume is below average (not a panic sell — just a soft open).
4. Enter Long on the 2nd candle open if 1st candle is bullish.
5. Stop Loss: Below the gap-down low or −1% from entry.
6. Target: Previous day's close price (gap fill).

### Short Entry (Gap Up Fill)
1. Stock gaps up 0.3–1.5% from previous close.
2. First 5-min candle shows bearish or indecisive body.
3. Volume drying up after initial spike (no sustained buying).
4. Enter Short on the 2nd candle open.
5. Stop Loss: Above the gap-up high or +1% from entry.
6. Target: Previous day's close price (gap fill).

---

## Exit Rules

- **Primary Target:** 100% gap fill (previous close).
- **Partial Exit:** Take 60% at 50% gap fill, let 40% ride to full fill.
- **Time Stop:** If gap not filling by 11:00 → exit and reassess.
- **Stop Adjustment:** If price consolidates near entry for 3+ candles without progressing → exit early.

---

## Filters (Critical — Skip These!)

- [ ] **Never fade a gap caused by fundamental news** (earnings surprise, M&A, macro shock).
- [ ] Skip if sector ETF is gapping in the same direction (systemic move, won't fill).
- [ ] Skip if gap is on extremely high volume (institutional accumulation/distribution).
- [ ] Skip gaps > 2% — too risky for fade strategy.
- [ ] Check if there is a key support/resistance level between entry and gap fill target.

---

## Gap Classification Cheatsheet

| Type            | Action            | Reason                            |
|-----------------|-------------------|-----------------------------------|
| Common Gap      | Fade aggressively | No news, likely to fill           |
| Breakaway Gap   | DO NOT fade       | Strong trend initiation           |
| Continuation Gap| DO NOT fade       | Mid-trend momentum                |
| Exhaustion Gap  | Fade cautiously   | End of trend, risky timing        |

---

## Risk Management

| Rule              | Guideline                         |
|-------------------|-----------------------------------|
| Max Risk/Trade    | 1% of account equity              |
| Trades per Day    | Max 3 gap trades (different stocks)|
| Stop Type         | Hard stop, no exceptions          |
| Daily Loss Limit  | −2% → stop trading for the day    |

---

## Example Trade Log

```
Date:         2026-06-10
Symbol:       VHM (HSX)
Prev Close:   43,500
Today Open:   42,800
Gap:          -1.6% (Gap Down)
Type:         Common gap, no news
1st Candle:   Bullish engulfing, low volume ✓
Entry:        42,850 (Long at 09:07)
Stop:         42,400 (-450 pts, -1.05%)
Target:       43,500 (full fill, +650 pts)
Result:       Gap filled at 10:45 → +WIN
```

---

## Notes & Improvements

- Track gap fill statistics by symbol to identify which stocks are "consistent gap fillers."
- Add a **half-fill partial exit** rule to protect profits on volatile sessions.
- Combine with VWAP: if gap-down stock bounces from VWAP, conviction increases.
- Best months: Low-volatility periods (April–June, October) when gaps are mechanically driven.

---

*Category: Fade / Mean Reversion | Timeframe: Intraday | Market: VN30F / HSX Stocks*
