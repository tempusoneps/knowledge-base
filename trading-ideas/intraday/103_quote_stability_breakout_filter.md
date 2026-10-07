# 103 — Quote Stability Breakout Filter

## Overview

Trade breakouts only when quotes remain stable before the trigger. A breakout from chaotic quoting often fails; a breakout from stable two-sided liquidity is more likely to attract follow-through.

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 1-min and 5-min |
| Markets | VN30F, liquid stocks |
| Metric | Spread stability and quote refresh behavior |

### Long Entry
1. Price consolidates below resistance for at least 15 minutes.
2. Spread stays near normal and quotes refresh consistently.
3. Price closes above resistance with volume expansion.
4. Enter long on the breakout or first stable retest.
5. Stop below resistance or the retest low.

### Short Entry
1. Price consolidates above support.
2. Spread and quote behavior remain stable.
3. Price closes below support with volume expansion.
4. Enter short on breakdown or first stable retest.
5. Stop above support or retest high.

## Exit Rules

- Target 1x-2x range height.
- Exit if quote stability collapses after entry.
- Trail behind 5-min structure if trend develops.

## Filters

- Avoid breakouts where spread widens before the trigger.
- Prefer liquid names with consistent order flow.
- Useful as a filter on other breakout setups.

## Risk Management

Do not increase size just because quotes are stable. Stability improves execution, not certainty.

---
*Category: Execution Quality / Breakout | Timeframe: Intraday | Market: VN30F / HSX Stocks*
