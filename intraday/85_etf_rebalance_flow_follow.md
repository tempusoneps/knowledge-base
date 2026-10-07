# 85 — ETF Rebalance Flow Follow

## Overview

Trade predictable intraday pressure around ETF or index rebalance sessions when additions, removals, or weight changes create directional demand. The trade must be based on confirmed flow, not just a rebalance headline.

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 5-min chart |
| Markets | VN30/VNFIN/VNDiamond related stocks |
| Context | Announced rebalance effective date or close |

### Long Entry
1. Stock is an expected addition or weight increase.
2. It holds above VWAP while market is flat or pulling back.
3. Volume pace is above 2x normal intraday pace.
4. Enter on VWAP pullback hold or HOD breakout.
5. Stop below VWAP or the last higher low.

### Short / Sell Signal
1. Stock is an expected deletion or weight decrease.
2. It cannot reclaim VWAP despite index stabilization.
3. Volume pace remains heavy on down candles.
4. Enter short where available, or use as an exit/avoid signal.
5. Stop above VWAP or last lower high.

## Exit Rules

- Take profit into late-day liquidity or before ATC.
- Exit if volume pace collapses.
- Do not hold solely for the rebalance thesis after flow fades.

## Filters

- Confirm the rebalance date and affected names before trading.
- Avoid crowded moves that already ran for several sessions.
- Prefer names with clear liquidity.

## Risk Management

Cap theme exposure because multiple rebalance names can reverse together.

---
*Category: Event Flow / ETF Rebalance | Timeframe: Intraday | Market: HSX Stocks*
