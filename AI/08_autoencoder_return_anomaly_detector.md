# 08 — Autoencoder Return Anomaly Detector

## Overview
Train an Autoencoder neural network on normal cross-sectional returns to detect statistical arbitrage opportunities through reconstruction error anomalies.

## Setup & Entry Rules
- Train a deep Autoencoder with a bottleneck layer on 100 liquid stock returns.
- Stocks with high reconstruction error are identified as anomalies (diverging from peer group).
- Enter long on negative anomaly stocks, and short/avoid on positive anomaly stocks.

## Exit Rules
- Exit when reconstruction error converges back to mean level (reconstruction error < threshold).
- Time stop: exit after 10 trading days if no convergence.

## Filters
- Filter out stocks with company-specific news (earnings, M&A) causing the anomaly.
- Verify that pairwise correlations are still historically active.

## Risk Management
- Use beta-neutral allocations. Equal risk contribution per asset pair/anomaly.

---
*Category: Deep Learning / Unsupervised | Timeframe: Daily | Market: Stocks*
