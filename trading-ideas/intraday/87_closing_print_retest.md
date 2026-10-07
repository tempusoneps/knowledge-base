# 87 — Closing Print Retest

## Overview

Use the previous session's closing auction price as an intraday reference. Large closing prints can become support/resistance the next day because many funds benchmark or rebalance around that level.

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 5-min chart |
| Markets | Liquid HSX stocks |
| Reference | Previous ATC/closing print |

### Long Entry
1. Previous close had unusually high ATC volume.
2. Today price pulls back to the closing print zone.
3. Sellers fail to push price below the zone for 2 candles.
4. Enter long on reclaim of the zone high.
5. Stop below the retest low.

### Short Entry
1. Previous close had unusually high ATC volume.
2. Today price rallies into the closing print zone from below.
3. Buyers fail to reclaim the zone.
4. Enter short on rejection candle or failed retest.
5. Stop above the retest high.

## Exit Rules

- Target VWAP, PDC extension level, or next intraday swing.
- Exit if price accepts through the closing print for 2 candles.

## Filters

- Stronger if the closing print was much larger than normal volume.
- Avoid if today's open gaps far beyond the level and never retests.
- Combine with market direction.

## Risk Management

Treat the closing print as a zone, not an exact tick. Stops should allow normal noise.

---
*Category: Auction Reference / Support Resistance | Timeframe: Intraday | Market: HSX Stocks*
