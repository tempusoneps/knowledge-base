# 14 — Open-to-Close Seasonality

## Overview
Exploit recurring intraday return patterns by day-of-week, month-end, or event calendar.

## Setup & Entry Rules
- Backtest open-to-close returns by calendar bucket.
- Trade only buckets with stable positive expectancy.
- Enter at open and exit at close or specified time.
- Revalidate quarterly.

## Exit Rules
- Exit at planned close/time stop.
- Disable signal if rolling expectancy turns negative.

## Filters
- Include realistic fees and slippage.
- Avoid days with major unscheduled news.

## Risk Management
Small fixed risk per trade; calendar edges decay quickly.

---
*Category: Seasonality / Intraday Quant | Timeframe: Intraday | Market: Stocks / Index*
