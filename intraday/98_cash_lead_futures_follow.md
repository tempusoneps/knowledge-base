# 98 — Cash Lead, Futures Follow

## Overview

Trade VN30F when the cash basket clearly leads but futures lag for a few minutes. The setup works when multiple heavyweight cash components move together before futures fully reprices.

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 1-min and 5-min |
| Markets | VN30F |
| Inputs | VN30 cash index, top weighted VN30 components |

### Long Entry
1. VN30 cash index breaks a 5-min resistance.
2. At least 60% of top-weight components are above VWAP.
3. VN30F remains below its equivalent trigger but holds higher lows.
4. Enter long VN30F when it breaks the lagging trigger.
5. Stop below the futures higher low.

### Short Entry
1. VN30 cash index breaks support.
2. Majority of top-weight components are below VWAP.
3. VN30F lags but forms lower highs.
4. Enter short when VN30F breaks its lagging support.
5. Stop above the futures lower high.

## Exit Rules

- Target futures catch-up to cash-implied level.
- Exit if cash breakout fails.
- Trail after futures reaches parity with cash move.

## Filters

- Avoid if cash index data is delayed.
- Best during broad basket moves, not single-component spikes.
- Skip near ATC unless auction flow is part of the plan.

## Risk Management

Use tight stops because the lead-lag window can close quickly.

---
*Category: Cash-Futures Lead-Lag | Timeframe: Intraday | Market: VN30F*
