# 119 — Liquidity Gap Fill

## Overview

Trade the fill of an intraday liquidity gap created by a fast directional move through thin volume. Once momentum fails, price often revisits the low-liquidity path because few trades occurred there.

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 5-min chart |
| Markets | VN30F, liquid stocks |
| Reference | Fast move with low traded volume between two zones |

### Short Entry
1. Price spikes upward through a thin-volume zone.
2. Spike fails to continue and forms a lower high.
3. Price breaks below the spike base or 9-EMA.
4. Enter short targeting the thin zone fill.
5. Stop above failed high.

### Long Entry
1. Price drops through a thin-volume zone.
2. Breakdown fails to continue and forms a higher low.
3. Price reclaims the drop base or 9-EMA.
4. Enter long targeting the thin zone fill.
5. Stop below failed low.

## Exit Rules

- Target midpoint of liquidity gap first.
- Target full fill second.
- Exit if price rejects strongly inside the gap.

## Filters

- Avoid if the original move was backed by confirmed major news.
- Better when volume profile shows clear low-volume path.
- Require reversal trigger before entering.

## Risk Management

Risk 0.5%-0.75%. Thin zones can move fast both ways, so avoid late entries.

---
*Category: Liquidity Gap / Mean Reversion | Timeframe: Intraday | Market: VN30F / HSX Stocks*
