# 72 — Bid/Ask Imbalance Continuation

## Overview

Follow a trend when one side of the book repeatedly refreshes faster than the other side can absorb. The edge comes from joining persistent aggressive flow instead of waiting for a classic chart pattern.

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 1-min execution, 5-min context |
| Markets | VN30F, top liquidity stocks |
| Context | After breakout from a range or VWAP acceptance |

### Long Entry
1. Price is above VWAP and making higher lows.
2. Best bid size refreshes quickly after being hit.
3. Ask liquidity is repeatedly lifted, not just quoted.
4. Enter on a shallow pullback that holds above the last impulse midpoint.
5. Stop below the last higher low.

### Short Entry
1. Price is below VWAP and making lower highs.
2. Best ask size refreshes quickly after being lifted.
3. Bid liquidity is repeatedly sold into.
4. Enter on a weak bounce that fails below the last impulse midpoint.
5. Stop above the last lower high.

## Exit Rules

- Take partial profit after 1R.
- Trail behind the last 1-min swing.
- Exit when the imbalance flips for 3-5 minutes.

## Filters

- Skip if spread widens erratically.
- Prefer the first 90 minutes or the final 45 minutes.
- Avoid when index direction conflicts with the trade.

## Risk Management

Use smaller size than a chart-only setup because book conditions can change quickly. Maximum 2 attempts per symbol per day.

---
*Category: Order Flow / Momentum | Timeframe: Intraday | Market: VN30F / Liquid HSX Stocks*
