# 88 — Large Lot Wall Break

## Overview

Trade continuation when a well-observed large resting order is genuinely consumed and price accepts beyond it. Unlike a spoof-wall reversal, this setup follows real absorption by aggressors.

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 1-min execution |
| Markets | VN30F, liquid stocks |
| Context | Visible wall near round number or intraday high/low |

### Long Entry
1. Large sell wall caps price for at least 5 minutes.
2. Trades repeatedly print into the wall.
3. The wall is consumed, not simply cancelled.
4. Price closes above the wall and holds the level on retest.
5. Enter long on the retest hold.

### Short Entry
1. Large buy wall supports price for at least 5 minutes.
2. Trades repeatedly hit the wall.
3. The wall is consumed by sellers.
4. Price closes below and fails on retest.
5. Enter short on continuation.

## Exit Rules

- Target the next visible liquidity cluster.
- Trail behind 1-min swings if momentum expands.
- Exit if price falls back through the consumed wall.

## Filters

- Require print confirmation; quoted size alone is not enough.
- Avoid lunch lull unless volume is abnormal.
- Prefer when broader market confirms.

## Risk Management

Risk 0.5%. Slippage can occur when liquidity disappears after the wall breaks.

---
*Category: Order Book / Breakout | Timeframe: Intraday | Market: VN30F / Liquid HSX Stocks*
