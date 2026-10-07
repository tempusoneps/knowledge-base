# 118 — Basket Confirmation Breakout

## Overview

Trade a single stock breakout only when a custom basket of related stocks confirms. This reduces false signals caused by one stock's isolated noise.

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 5-min chart |
| Markets | Sector baskets or VN30 component groups |
| Basket | 5-10 liquid related stocks |

### Long Entry
1. Candidate stock forms a clear intraday resistance.
2. At least 60% of basket members are above VWAP.
3. Basket equal-weight index makes a new intraday high.
4. Candidate closes above resistance.
5. Enter long on close or first retest.

### Short / Sell Entry
1. Candidate stock forms clear support.
2. At least 60% of basket members are below VWAP.
3. Basket equal-weight index makes a new intraday low.
4. Candidate closes below support.
5. Enter short where available, or sell/avoid, on breakdown.

## Exit Rules

- Target measured move from candidate range.
- Exit if basket confirmation reverses.
- Take partials at candidate HOD/LOD.

## Filters

- Basket should be built before the session, not changed after signal.
- Avoid if one stock dominates basket movement.
- Use liquid, correlated members.

## Risk Management

Limit trades from the same basket to avoid duplicated exposure.

---
*Category: Basket Confirmation / Breakout | Timeframe: Intraday | Market: HSX Stocks*
