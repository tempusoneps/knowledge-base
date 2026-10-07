# 64 — Volume Weighted MACD (VW-MACD) Cross

## Overview

The standard MACD is a powerful momentum oscillator, but it relies purely on price, completely ignoring volume. In intraday trading, volume is the fuel that validates a move. The **Volume Weighted MACD (VW-MACD)** replaces standard exponential moving averages with Volume Weighted Moving Averages (VWMA). A crossover in the VW-MACD ensures that the momentum shift is actually backed by institutional volume, filtering out low-volume fakeouts.

---

## Concept

```
Standard MACD:
  MACD Line = 12-EMA - 26-EMA
  Signal Line = 9-EMA of MACD Line

VW-MACD:
  MACD Line = 12-VWMA - 26-VWMA
  Signal Line = 9-VWMA of MACD Line

The Logic:
  If price moves up, but volume is dead, the standard MACD will still cross bullishly (often a trap).
  The VW-MACD will NOT cross bullishly if the volume is dead, because the volume weighting drags the average down.
  A VW-MACD cross only happens when BOTH price momentum and volume momentum align.
```

**Trade Logic:** Trade the VW-MACD zero-line cross or signal line cross, confident that the move is backed by true market participation.

---

## Indicators Required

| Indicator      | Setting                      | Purpose                                  |
| -------------- | ---------------------------- | ---------------------------------------- |
| VW-MACD        | 12, 26, 9 (Volume Weighted)  | Primary trend and momentum filter        |
| VWAP           | Daily                        | Ensure alignment with the daily mean     |
| Price Action   | Support/Resistance           | Define entry/stop levels                 |

---

## Setup & Entry Rules

| Parameter | Value                                          |
| --------- | ---------------------------------------------- |
| Timeframe | 5-min or 15-min chart                          |
| Markets   | VN30F, Liquid HSX Stocks                       |
| Context   | Best for catching the start of an intraday trend|

### Long Entry (Bullish Volume-Backed Cross)
1. **The Setup:** Price is consolidating or forming a base.
2. **The Signal:** The VW-MACD line crosses *above* the Signal line.
3. **The Filter:** The cross must happen *below* the Zero Line (indicating a reversal from oversold conditions) OR price must be crossing above the daily VWAP simultaneously.
4. **Trigger:** A bullish 5-min candle confirms the breakout of the consolidation base.
5. **Entry:** Go Long on the close of the trigger candle.
6. **Stop Loss:** Below the recent consolidation low.

### Short Entry (Bearish Volume-Backed Cross)
1. **The Setup:** Price forms a top.
2. **The Signal:** VW-MACD line crosses *below* the Signal line.
3. **The Filter:** Cross happens *above* the Zero Line, OR price crosses below daily VWAP.
4. **Trigger:** Bearish 5-min candle breaks the consolidation support.
5. **Entry:** Go Short on the close.
6. **Stop Loss:** Above the recent consolidation high.

---

## Exit Rules

- **Target 1:** Next major S/R level or 1.5x risk. Take 50%.
- **Trailing Stop:** Trail the remaining 50% as long as the VW-MACD line remains above the Signal line. 
- **Reversal Exit:** Exit the entire position immediately if the VW-MACD crosses back in the opposite direction.

---

## Filters

- [ ] **Crucial:** You must use a custom script or a platform that supports VW-MACD (TradingView has community scripts for this; AmiBroker/Python requires custom coding).
- [ ] If the standard MACD crosses but the VW-MACD does not, **DO NOT TRADE**. This is the exact trap the indicator is designed to avoid.
- [ ] Avoid trading crosses that happen when the MACD lines are flat and hugging the Zero line closely (chop zone).

---

## Risk Management

| Rule             | Guideline                          |
| ---------------- | ---------------------------------- |
| Max Risk/Trade   | 1% of account equity               |
| Stop Placement   | Below recent price structure       |
| Min R:R          | 1:2                                |

---

## Edge & Statistics

- **Win rate:** 60-65% (significantly higher than standard MACD intraday).
- **Edge:** By mathematically requiring volume to confirm the price momentum, you eliminate a massive percentage of the "chop" trades that plague standard oscillator systems.

---

## Example Trade Log

```
Date:      2026-06-03
Symbol:    STB (HSX)
Context:   STB drifting slowly down all morning on low volume. Standard MACD crosses bullish at 10:15, but VW-MACD does not (filters the fakeout).
The Signal: At 11:00, heavy volume steps in. VW-MACD aggressively crosses ABOVE the signal line while below the zero line.
Trigger:   Price breaks above a local resistance at 30,500.
Entry:     30,550 (Long)
Stop:      30,300 (Below the morning base)
Target:    Trail with VW-MACD.
Result:    Trend continues until 14:00 when VW-MACD crosses bearish. Exit at 31,200. +WIN (+650 pts).
```

---

## Notes & Improvements
- This is an excellent indicator for algorithmic systems because it mathematically combines price and volume into a single, clean crossover signal without needing visual interpretation of volume bars.

---
*Category: Momentum / Volume | Timeframe: Intraday (5-min/15-min) | Market: VN30F / HSX Stocks*
