# 09 — FinBERT Sentiment Arbitrage

## Overview
Utilize a pre-trained FinBERT language model to analyze earnings calls and financial news feeds to exploit sentiment drift.

## Setup & Entry Rules
- Run sentiment analysis on transcripts and news using FinBERT to get sentiment scores (-1 to +1).
- Enter long when the sentiment score is highly positive (>0.80) and has surprised market expectations.
- Enter short or avoid when the sentiment is negative (< -0.50).

## Exit Rules
- Exit after a holding period of 3 to 5 trading days.
- Trailing stop: exit if stock drops 5% from its post-announcement peak.

## Filters
- Skip trades where the volume is highly concentrated in retail brokers.
- Exclude stocks with a high short float to avoid squeeze noise.

## Risk Management
Max allocation of 2% per stock. Stop loss is strictly enforced at entry day low.

---
*Category: NLP / Sentiment | Timeframe: Daily | Market: Stocks*
