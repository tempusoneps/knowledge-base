# 07 — Bollinger Band Squeeze Breakout

## Overview

The Bollinger Band Squeeze occurs when volatility contracts to an extreme, compressing the bands to their narrowest point in recent history. This compression is a coiled spring — when price finally breaks out, the resulting move is typically sharp and sustained. This strategy identifies the squeeze and enters on the expansion breakout.

---

## Concept

```
Bollinger Bands:
  Upper Band = SMA(20) + 2 × StdDev(20)
  Middle Band = SMA(20)
  Lower Band = SMA(20) - 2 × StdDev(20)
  Band Width = (Upper - Lower) / Middle

Squeeze = Band Width at multi-session LOW → compression → breakout incoming
```

**Bollinger Band Width (BBW):** When BBW reaches its lowest level in the last 20–30 bars, a squeeze is active. The direction of the breakout determines trade direction.

**Keltner Channel Enhancement:** Some traders overlay Keltner Channels (EMA ± 1.5×ATR). When Bollinger Bands are *inside* Keltner Channels → confirmed squeeze.

---

## Indicators Required

| Indicator         | Setting            | Purpose                            |
|-------------------|--------------------|------------------------------------|
| Bollinger Bands   | SMA 20, ±2 StdDev  | Volatility envelope                |
| BB Width          | (Upper-Lower)/Mid  | Squeeze detection                  |
| Keltner Channel   | EMA 20, ±1.5× ATR  | Squeeze confirmation (optional)    |
| Volume            | 20-bar MA          | Breakout confirmation              |
| Momentum (TTM)    | TTM Squeeze dot    | Direction of squeeze release       |

---

## Setup & Entry Rules

| Parameter    | Value                                              |
|--------------|----------------------------------------------------|
| Timeframe    | 5-min or 15-min chart                              |
| Markets      | VN30F, any liquid stock with range-bound history   |
| Trigger      | BBW at lowest point in past 20 bars                |

### Long Entry (Upside Breakout)
1. BBW is at 20-bar low (squeeze confirmed).
2. Price breaks **above** the Upper Bollinger Band on a 5-min close.
3. Volume spikes > 1.5× the 20-bar average.
4. TTM Squeeze momentum turns positive (green dots) if available.
5. Enter Long on the close of the breakout candle.
6. Stop Loss: Middle Band (SMA 20) or the close of the squeeze candle.

### Short Entry (Downside Breakout)
1. BBW is at 20-bar low.
2. Price breaks **below** the Lower Bollinger Band.
3. Volume confirms.
4. TTM Squeeze momentum turns negative.
5. Enter Short on breakout candle close.
6. Stop Loss: Middle Band.

---

## Squeeze Scoring

| Signal                                    | Strength |
|-------------------------------------------|----------|
| BBW at 5-session low                      | ★★★★★    |
| BBW at 2-session low                      | ★★★      |
| Bollinger inside Keltner confirmed        | +★★      |
| Low-volume squeeze (accumulation)         | +★★      |
| Pre-market or overnight consolidation     | +★       |

**Trade only if overall squeeze score ≥ ★★★★**

---

## Exit Rules

- **Target 1:** Price reaches opposite BB band (walk from lower to upper band).
- **Target 2:** 2× the band width from breakout point.
- **Trail Stop:** Trail below the Middle Band (SMA 20) for Long trades.
- **Failure:** If price breaks back inside the bands within 2 candles → exit immediately (failed squeeze breakout).
- **Time Stop:** Close before 14:15.

---

## Risk Management

| Rule              | Guideline                                 |
|-------------------|-------------------------------------------|
| Max Risk/Trade    | 1% of account equity                      |
| Stop Placement    | Middle Band (SMA 20)                      |
| R:R Minimum       | 1:2 (band width target ÷ stop distance)   |
| Max Trades/Day    | 2 squeeze breakouts maximum               |
| Daily Loss Limit  | −2% → stop trading                        |

---

## Common Mistakes to Avoid

- ❌ Entering during the squeeze (before breakout) — too early, direction unknown.
- ❌ Ignoring volume on the breakout candle — low-volume breakouts fail more often.
- ❌ Trading a squeeze during a strong trending market — band squeeze is less meaningful.
- ❌ Entering too late (3rd candle after breakout) — most of the move is already done.

---

## Example Trade Log

```
Date:          2026-06-16
Symbol:        VN30F2607
BBW:           At 25-bar low (09:05–10:30 compression)
Squeeze End:   10:35 — candle closes above Upper BB (1,269)
Volume:        2.1× average ✓
Entry:         1,270 (Long)
Stop:          1,263 (Middle Band)
T1:            1,279 (opposite band) ← 60% closed at 11:00
T2:            1,285 (2× BBW projection) ← 40% closed at 11:30
Result:        +WIN
```

---

## Notes & Improvements

- **Pre-market scan:** Run a BBW scan at 08:45 to identify stocks already in squeeze before open — these often break out dramatically at the open.
- Combine with **ORB**: if ORB forms inside a squeeze, the ORB breakout is the squeeze breakout → double confirmation.
- Track **squeeze duration**: longer squeezes (more bars compressed) tend to produce larger post-breakout moves.

---

*Category: Volatility Breakout | Timeframe: Intraday (5-min / 15-min) | Market: VN30F / HSX Stocks*
