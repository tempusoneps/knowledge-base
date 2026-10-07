# 03 — Random Forest Breakout Probability

## Overview
Classify the likelihood of a chart breakout succeeding using a Random Forest classifier trained on breakout day microstructure features.

## Setup & Entry Rules
- Trigger: Price crosses above the 52-week high.
- Features: Relative volume expansion, bid-ask spread, order book imbalance, and historical volatility.
- Enter long if Random Forest prediction probability of a successful breakout (defined as >5% move within 5 days) exceeds 0.70.

## Exit Rules
- Exit after 5 trading days if target is not hit.
- Take profit: 6% gain. Stop loss: 3% loss from the entry price.

## Filters
- Do not trade if general market index (VN-Index) is below its 200-day MA.
- Skip if breakout happens on lower-than-average volume.

## Risk Management
- Position size based on Kelly Criterion scaled by 0.25. Max risk per trade: 1.5%.

---
*Category: Machine Learning / Ensemble | Timeframe: Weekly / Swing | Market: Stocks*
