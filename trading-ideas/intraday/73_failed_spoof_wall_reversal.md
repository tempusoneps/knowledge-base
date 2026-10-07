# 73 — Failed Spoof Wall Reversal

## Overview

Trade against a visible order-book wall when the wall disappears or fails to attract real continuation. The idea is practical only when the trader can observe depth-of-market behavior and confirm with prints.

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 1-min chart plus DOM |
| Markets | VN30F, liquid large-cap stocks |
| Context | Near an intraday high/low or round number |

### Long Entry
1. A large sell wall appears above price and stalls buyers.
2. Price refuses to sell off despite the visible wall.
3. The wall is cancelled or lifted, and price closes above it.
4. Enter long on the first retest of the former wall price.
5. Stop below the reclaim candle.

### Short Entry
1. A large buy wall appears below price and attracts buyers.
2. Price cannot bounce meaningfully from the wall.
3. The wall is cancelled or sold through.
4. Enter short on the first failed retest from below.
5. Stop above the breakdown candle.

## Exit Rules

- Target the next liquidity pocket or prior swing.
- Exit half at 1R and trail the rest behind micro swings.
- Abort if the same wall reappears and holds.

## Filters

- Do not assume spoofing from size alone; require cancellation/failure plus price response.
- Avoid slow midday periods unless the level is very clear.
- Best after a trapped breakout or breakdown.

## Risk Management

Risk 0.5% per trade. Use hard stops because order-book signals can reverse instantly.

---
*Category: Market Microstructure / Reversal | Timeframe: Intraday | Market: VN30F / Liquid HSX Stocks*
