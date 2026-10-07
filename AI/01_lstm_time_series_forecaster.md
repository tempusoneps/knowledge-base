# 01 — LSTM Time-Series Forecaster

## Overview
Use a Long Short-Term Memory (LSTM) network to predict the next-day price direction of liquid equities based on historical price and volume sequences.

## Setup & Entry Rules
- Input features: 30 days of normalized OHLCV, RSI, and MACD data.
- Model architecture: 2 LSTM layers (64 units) followed by a Dense layer with sigmoid activation.
- Buy signal: Model predicts probability of positive return > 0.60.
- Short/Avoid signal: Model predicts probability of positive return < 0.40.

## Exit Rules
- Exit at market close on the next trading day.
- Stop loss: exit immediately if position moves 1.5 ATR against the trade.

## Filters
- Filter out stocks with daily trading volume below the 30-day average.
- Avoid entry during earnings announcement weeks.
- Ensure overall market regime (VN30) is not in a high-volatility drawdown.

## Risk Management
- Limit exposure to 1% of total portfolio capital per trade. Max 5 concurrent positions.

---
*Category: Deep Learning / Sequence | Timeframe: Daily | Market: Stocks / VN30F*
