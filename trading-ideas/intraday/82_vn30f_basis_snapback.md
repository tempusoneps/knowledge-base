# 82 — VN30F Basis Snapback

## Overview

Trade mean reversion when VN30 futures basis stretches too far from the cash index without a matching change in cash basket momentum. This is different from pure arbitrage because it waits for basis exhaustion and confirmation.

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 1-min or 5-min |
| Markets | VN30F vs VN30 cash index |
| Metric | Futures basis = VN30F - VN30 cash |

### Short Futures Entry
1. Basis expands above its intraday 90th percentile.
2. VN30 cash index stops making higher highs.
3. VN30F fails to extend and breaks a 1-min higher-low structure.
4. Enter short VN30F.
5. Stop above the futures exhaustion high.

### Long Futures Entry
1. Basis compresses below its intraday 10th percentile.
2. VN30 cash index stops making lower lows.
3. VN30F reclaims a micro resistance level.
4. Enter long VN30F.
5. Stop below the futures exhaustion low.

## Exit Rules

- Target basis returning to intraday median.
- Exit if cash index starts confirming the futures move.
- Time stop after 20-30 minutes if basis does not normalize.

## Filters

- Avoid opening minutes when basis can be unstable.
- Be careful near expiry and major index rebalancing.
- Use only liquid front-month contracts.

## Risk Management

Position size from VN30F stop distance. Do not assume convergence is guaranteed.

---
*Category: Futures Basis / Mean Reversion | Timeframe: Intraday | Market: VN30F*
