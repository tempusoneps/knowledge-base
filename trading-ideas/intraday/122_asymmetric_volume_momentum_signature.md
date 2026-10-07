# 122 — Asymmetric Volume Momentum Signature (AVMS)

## Overview

Institutional buying and selling leaves footprint signatures in volume distribution before major price trends occur. The **Asymmetric Volume Momentum Signature (AVMS)** is a mathematical indicator that measures the ratio of volume during positive price velocity bars vs. negative price velocity bars within a rolling window. It identifies subtle accumulation or distribution patterns during range-bound consolidations, giving an early warning before the actual price breakout.

---

## Concept

We define the Asymmetric Volume Momentum Indicator ($AVMI$) as:
$$AVMI_t = \frac{\sum_{i=0}^{N-1} (Volume_{t-i} \times \text{sgn}(\Delta Price_{t-i}))}{\sum_{i=0}^{N-1} Volume_{t-i}}$$

Where:
- $\text{sgn}(\Delta Price) = 1$ if $Close > Close_{prev}$, $-1$ if $Close < Close_{prev}$, and $0$ otherwise.
- $N$ is the rolling window (e.g., 14 bars).

When $AVMI$ reaches positive extremes (e.g., $> 0.35$) while price is moving sideways, it indicates strong buying absorption (accumulation). When it reaches negative extremes (e.g., $< -0.35$), it indicates distribution.

```
Accumulation Signature:
  Price Consolidation (Max-Min Close over 14 bars < 0.3%)
  AND Rolling AVMI rises above +0.30
  → Triggers an early Long Entry before price breaks out.
```

---

## Indicators Required

| Indicator | Setting | Purpose |
| --- | --- | --- |
| AVMI | Lookback: 14 bars | Measure volume-price asymmetry |
| Consolidation Filter | Lookback: 14 bars | Detect sideways price range |
| RSI | Length: 14 | Confirm momentum momentum alignment |

---

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 5-min chart |
| Markets | VN30F1M |
| Entry Window | 09:30 – 14:00 |

### Long Entry
1. Market is in a tight consolidation: `(Max(Close, 14) - Min(Close, 14)) / Close < 0.003` (0.3% range).
2. The $AVMI(14)$ cross above $+0.30$, indicating aggressive buying absorption.
3. The RSI(14) is above 50.
4. Enter Long on the next bar open.
5. Stop Loss: Below the 14-bar low.

### Short Entry
1. Market is in a tight consolidation: `(Max(Close, 14) - Min(Close, 14)) / Close < 0.003` (0.3% range).
2. The $AVMI(14)$ crosses below $-0.30$, indicating aggressive selling absorption.
3. The RSI(14) is below 50.
4. Enter Short on the next bar open.
5. Stop Loss: Above the 14-bar high.

---

## Exit Rules

- **Target 1:** 1.5x the consolidation height from the entry price → close 60%.
- **Target 2:** Trailing stop using the 9-period EMA.
- **Time Stop:** Force close at 14:25 to avoid overnight gaps.

---

## Filters

- Do not enter if the consolidation range is too wide ($> 0.6\%$), as the risk-to-reward ratio becomes unfavorable.
- Avoid entry during the first 15 minutes of the morning session (09:00 - 09:15) to allow the initial open volatility to settle.

---

## Risk Management

| Rule | Guideline |
| --- | --- |
| Max Risk/Trade | 1.0% of account equity |
| Stop Placement | Stop Loss based on consolidation boundary or `utils.py` levels |
| Min R:R | 1:2 (extremely favorable due to entering inside consolidation) |

---

## Edge & Statistics

- **Hypothesis:** Retail traders breakout-chase after price moves, leading to high slippage. By using $AVMI$ to detect institutional absorption *inside* the consolidation, we enter early with a very tight stop loss and exit as the public chases the resulting breakout.
- **Expected Win Rate:** 53% - 58%.

---

## Notes & Improvements

- AVMI can be smoothed with a 3-period EMA to reduce noise.
- This strategy works best in range-to-trend transition phases and pairs perfectly with the Hurst Exponent filter to confirm regime changes.

---
*Category: Volumetric / Accumulation | Timeframe: Intraday (5-min) | Market: VN30F1M*
