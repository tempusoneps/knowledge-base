# 121 — Fractal Regime-Switching Breakout

## Overview

Most trend-following systems suffer during chop because they cannot distinguish between random walk (mean-reverting noise) and a true persistent trend. This strategy uses a rolling intraday **Hurst Exponent (H)** or **Fractal Dimension (D)** calculated on 5-minute bars as a regime-switching filter. It identifies when the VN30F1M market transitions from a mean-reverting regime ($H < 0.45$) to a trending regime ($H > 0.55$) and triggers breakouts only in the trending regime.

---

## Concept

The Hurst Exponent ($H$) measures the long-term memory of time series:
- $H \approx 0.5$: Random walk (Brownian motion).
- $H < 0.5$: Mean-reverting (sub-diffusive) behavior.
- $H > 0.5$: Trending (persistent, super-diffusive) behavior.

We calculate a rolling $H$ over a lookback window of 30 bars (2.5 hours on 5m chart) using a simplified variance-ratio or range-rescaled method to prevent look-ahead bias and keep it computationally efficient for intraday backtesting.

```
Regime Switch Signal:
  IF Rolling Hurst Exponent (H) transitions from < 0.45 (compressed range) to > 0.55
  AND Price breaks out of the 15-bar channel High/Low
  → Trigger high-conviction breakout entry.
```

---

## Indicators Required

| Indicator | Setting | Purpose |
| --- | --- | --- |
| Rolling Hurst (H) | Lookback: 30 bars | Quantify regime persistence |
| Donchian Channel | Lookback: 15 bars | Define entry boundaries |
| ATR | Lookback: 14 bars | Volatility threshold and stop sizing |

---

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 5-min chart |
| Markets | VN30F1M |
| Entry Window | 09:30 – 14:00 |

### Long Entry
1. The rolling Hurst exponent ($H$) rises above $0.55$ (signaling persistent momentum).
2. The current 5-min close breaks above the 15-bar Donchian Channel High.
3. The breakout bar has an expansion in volatility (Close - Open > 0.5 * ATR).
4. Enter Long on the close of the breakout candle.
5. Stop Loss: Calculated using the `get_trade_levels` helper or placed below the 15-bar Donchian Channel Low.

### Short Entry
1. The rolling Hurst exponent ($H$) rises above $0.55$.
2. The current 5-min close breaks below the 15-bar Donchian Channel Low.
3. Volatility expands on the down bar (Open - Close > 0.5 * ATR).
4. Enter Short on the close of the breakout candle.
5. Stop Loss: Calculated using `get_trade_levels` or placed above the 15-bar Donchian Channel High.

---

## Exit Rules

- **Target 1:** 2x ATR distance from entry → close 50%.
- **Target 2:** Trailing stop based on the 15-bar Donchian opposite band (or trailing SL from `utils.py`).
- **Time Stop:** Force close at 14:25 to avoid overnight gap risks.

---

## Filters

- Skip entries if the Hurst exponent is in the chop zone ($0.45 \le H \le 0.55$).
- Do not trade if the Donchian channel range is wider than 2% of the price (already overextended).
- Confirm that the slope of the 50-period EMA matches the breakout direction to ensure macro alignment.

---

## Risk Management

| Rule | Guideline |
| --- | --- |
| Max Risk/Trade | 1.0% of account equity |
| Stop Placement | Stop Loss based on standard structure or `utils.py` levels |
| Min R:R | 1:1.5 |

---

## Edge & Statistics

- **Hypothesis:** VN30F1M is highly trending once institutional volume drives price beyond the daily balance. Filtering out range-bound days using a rolling Hurst metric reduces false breakouts by up to 40% compared to standard Donchian or ORB strategies.
- **Expected Win Rate:** 52% - 56% with a high profit factor due to avoiding whipsaws.

---

## Notes & Improvements

- Calculate the Hurst exponent using Python's rolling variance: $H \approx \log(\text{Variance Ratio}) / \log(\text{Window})$.
- Test on different lookbacks (e.g., 20 to 45 bars) to match the morning vs. afternoon session cycles.

---
*Category: Regime-Switching / Momentum | Timeframe: Intraday (5-min) | Market: VN30F1M*
