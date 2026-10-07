# 04 — Overnight Gap Reversion Model

## Overview
Systematically fade large overnight gaps when there is no confirmed catalyst and liquidity is normal.

## Setup & Entry Rules
- Gap exceeds 1.5x 20-day average gap.
- Exclude earnings, dividends, and major news.
- Enter against the gap after first 15-30 minutes if price fails to extend.
- Hold intraday to 3 days depending on test results.

## Exit Rules
- Target 50% gap fill or previous close.
- Stop if price breaks opening extreme.

## Filters
- Require adequate volume and spread.
- Market regime filter: avoid strong trend days.

## Risk Management
Cap gap-fade exposure by sector and market beta.

---
*Category: Quant Gap Reversion | Timeframe: Intraday-Days | Market: Stocks*
