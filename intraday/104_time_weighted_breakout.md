# 104 — Time-Weighted Breakout

## Overview

This strategy gives more weight to how long price holds near a level before breaking. A level tested and accepted for a long time often has cleaner continuation than a sudden one-candle spike.

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 5-min chart |
| Markets | VN30F, liquid HSX stocks |
| Context | Price pressing against support/resistance |

### Long Entry
1. Price spends at least 45 minutes in the upper third of an intraday range.
2. Pullbacks from resistance become smaller.
3. Volume does not collapse during the pressure period.
4. Enter on 5-min close above resistance.
5. Stop below the final higher low inside the range.

### Short Entry
1. Price spends at least 45 minutes in the lower third of a range.
2. Bounces from support become smaller.
3. Volume remains active.
4. Enter on 5-min close below support.
5. Stop above the final lower high.

## Exit Rules

- Target range height projected from breakout.
- Exit if price returns into the middle of the old range.
- Take partials at 1R.

## Filters

- Avoid if the range forms during a dead lunch period with no volume.
- Stronger when VWAP sits near the breakout side.
- Confirm with market direction.

## Risk Management

The stop is structural, not arbitrary. Skip if the final swing makes risk too wide.

---
*Category: Breakout / Price Acceptance | Timeframe: Intraday | Market: VN30F / HSX Stocks*
