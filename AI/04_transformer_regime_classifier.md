# 04 — Transformer Regime Classifier

## Overview
Use a Transformer encoder architecture to capture long-range attention dependencies across global macro data and classify the current market regime.

## Setup & Entry Rules
- Input: Multi-channel time-series of bond yields, currency indices, commodity prices, and equity indices.
- Model outputs one of three regimes: Bull, Bear, or Sideways.
- Enter long risk assets when the model signals a transition into a Bull regime.

## Exit Rules
- Exit or hedge long assets when the model signals a transition into Bear or Sideways regime.
- Rebalance when a new regime classification persists for 3 consecutive days.

## Filters
- Verify regime classification consistency across multiple model training checkpoints.
- Do not trade if model attention weights are highly dispersed.

## Risk Management
- De-leverage portfolio by 50% during Sideways regimes. Max target volatility capped at 12%.

---
*Category: Deep Learning / Attention | Timeframe: Daily / Weekly | Market: Multi-Asset*
