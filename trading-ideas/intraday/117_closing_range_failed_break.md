# 117 — Closing Range Failed Break

## Overview

Fade a failed break from the final hour range. Late in the session, failed moves often unwind quickly because traders have limited time to hold losing positions.

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 1-min and 5-min |
| Markets | VN30F, liquid stocks |
| Context | Final 60 minutes before ATC |

### Short Entry
1. Final-hour range forms for at least 20 minutes.
2. Price breaks above range high.
3. Break fails within 1-3 candles and closes back inside range.
4. Enter short on failed retest of range high.
5. Stop above failed breakout high.

### Long Entry
1. Final-hour range forms.
2. Price breaks below range low.
3. Breakdown fails and price closes back inside range.
4. Enter long on successful retest of range low.
5. Stop below failed breakdown low.

## Exit Rules

- Target range midpoint first.
- Target opposite side of closing range second.
- Exit before ATC unless auction risk is intentional.

## Filters

- Avoid if confirmed closing imbalance supports the break.
- Best on balanced days.
- Require enough time before close for target to be reached.

## Risk Management

Risk 0.5%. Do not re-enter repeatedly in the final minutes.

---
*Category: Closing Range / Failed Break | Timeframe: Intraday | Market: VN30F / HSX Stocks*
