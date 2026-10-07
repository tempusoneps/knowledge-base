# 24 — SHAP Explainable AI Filter

## Overview
Use SHAP values to explain complex neural net predictions and filter out trades where confidence is driven by unstable features.

## Setup & Entry Rules
- Collect feature set including technical features, volume dynamics, and statistical indicators.
- Train Explainable AI model using historical rolling window or relevant training pipeline.
- Generate signal score daily/intraday; enter long when score crosses entry threshold.

## Exit Rules
- Exit when signal score reverses below entry threshold or hits risk constraints.
- Stop loss: exit position if price drops below 2.0 ATR from entry.

## Filters
- Do not enter trades if spread is wider than historical median.
- Filter out illiquid tokens or stocks.
- Suspend trading during major policy announcement periods.

## Risk Management
- Strict risk budget per position: maximum 1% capital exposure. Dynamic stop-loss based on rolling volatility.

---
*Category: AI / Explainable AI | Timeframe: Daily | Market: Stocks*
