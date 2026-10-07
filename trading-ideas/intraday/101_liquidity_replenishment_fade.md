# 101 — Liquidity Replenishment Fade

## Overview

Fade a breakout attempt when liquidity quickly replenishes against the move after an initial level break. The market shows that the breakout consumed visible orders but uncovered even more opposite interest.

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 1-min chart plus DOM |
| Markets | VN30F, liquid stocks |
| Context | Break above/below a clear intraday level |

### Short Entry
1. Price breaks above resistance.
2. Ask liquidity immediately reloads above the breakout.
3. Aggressive buying slows and price cannot hold above the level.
4. Enter short when price closes back below resistance.
5. Stop above the replenishment high.

### Long Entry
1. Price breaks below support.
2. Bid liquidity quickly reloads below the breakdown.
3. Aggressive selling slows.
4. Enter long when price reclaims support.
5. Stop below the replenishment low.

## Exit Rules

- Target the opposite side of the failed breakout range.
- Take partial at VWAP or midpoint.
- Exit if price accepts beyond the reloaded liquidity.

## Filters

- Requires live depth and print confirmation.
- Avoid thin names where reloads are unreliable.
- Best after a crowded obvious breakout.

## Risk Management

Risk 0.5%. Keep stops tight because valid breakouts should not return into the range.

---
*Category: Order Flow / Failed Breakout | Timeframe: Intraday | Market: VN30F / Liquid HSX Stocks*
