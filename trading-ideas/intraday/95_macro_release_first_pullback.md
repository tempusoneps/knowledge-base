# 95 — Macro Release First Pullback

## Overview

Trade the first controlled pullback after a scheduled macro release creates a clear directional repricing. The strategy avoids the first violent candle and joins only after spreads and direction stabilize.

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 1-min and 5-min |
| Markets | VN30F, index-sensitive stocks |
| Context | CPI, rates, FX, policy, or other scheduled macro event |

### Long Entry
1. Release triggers a strong upside impulse.
2. Wait at least 3-5 minutes for spreads to normalize.
3. Price pulls back 30%-50% of the impulse without losing VWAP.
4. Enter long when pullback high breaks.
5. Stop below pullback low.

### Short Entry
1. Release triggers a strong downside impulse.
2. Wait for the initial volatility burst to settle.
3. Price bounces 30%-50% without reclaiming VWAP.
4. Enter short when bounce low breaks.
5. Stop above bounce high.

## Exit Rules

- Target retest of post-release extreme.
- Target 2: measured move if the extreme breaks.
- Exit if price fully retraces the release impulse.

## Filters

- Only use scheduled, known-time events.
- Avoid guessing before the release.
- Require liquidity normalization before entry.

## Risk Management

Use half normal size. Macro candles can slip through stops.

---
*Category: Macro Event / Momentum | Timeframe: Intraday | Market: VN30F / Index Stocks*
