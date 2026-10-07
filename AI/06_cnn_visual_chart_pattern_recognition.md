# 06 — CNN Visual Chart Pattern Recognition

## Overview
Convert 2D chart data into images and use a Convolutional Neural Network (CNN) to detect classic continuation and reversal patterns.

## Setup & Entry Rules
- Generate 64x64 pixel images of normalized stock price history (last 60 bars).
- Train CNN to recognize Head & Shoulders, Double Bottoms, and Bull Flags.
- Enter long when the CNN detects a high-probability Bull Flag or Double Bottom.

## Exit Rules
- Stop loss placed below the swing low of the detected pattern.
- Target: 2x the vertical height of the pattern projected from breakout.

## Filters
- Confirm breakout with a breakout volume filter.
- Do not trade patterns that form in highly illiquid tickers.

## Risk Management
- Risk 1% of account equity per pattern trade. Cap maximum concurrent pattern trades at 3.

---
*Category: Deep Learning / Vision | Timeframe: Daily / Hourly | Market: Stocks*
