# 90 — Opening Auction Mismatch Fade

## Overview

Fade an opening auction price that is far away from fair value when the post-open tape immediately rejects it. This is distinct from a normal gap fade because the trigger is auction mismatch plus failed acceptance.

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 1-min and 5-min |
| Markets | Liquid HSX stocks |
| Context | ATO open with abnormal auction volume or price dislocation |

### Short Entry
1. ATO opens far above PDC or expected fair value.
2. First 5-10 minutes fail to build higher lows.
3. Price breaks below ATO low or VWAP.
4. Enter short where available, or use as sell/avoid signal.
5. Stop above opening auction high.

### Long Entry
1. ATO opens far below PDC or fair value.
2. First 5-10 minutes fail to continue lower.
3. Price reclaims ATO high or VWAP.
4. Enter long on reclaim confirmation.
5. Stop below opening auction low.

## Exit Rules

- Target PDC, VWAP, or midpoint of the opening dislocation.
- Exit if price accepts beyond the auction extreme.
- Take profits quickly if liquidity is thin.

## Filters

- Avoid if the auction move is backed by confirmed major news.
- Require abnormal auction volume or visible imbalance.
- Do not trade stocks with poor post-open liquidity.

## Risk Management

Use wider-than-normal slippage assumptions during the first 10 minutes.

---
*Category: Opening Auction / Mean Reversion | Timeframe: Intraday | Market: HSX Stocks*
