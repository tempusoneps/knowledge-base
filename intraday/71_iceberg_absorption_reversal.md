# 71 — Iceberg Absorption Reversal

## Overview

Trade a reversal when aggressive orders repeatedly hit one price level but price refuses to move through it. The hidden resting liquidity is absorbing flow, and once the aggressors stop, price often snaps the other way.

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 1-min or 5-min chart |
| Markets | VN30F, highly liquid HSX stocks |
| Context | Near HOD/LOD, VWAP, PDC, or a visible intraday level |

### Long Entry
1. Price tests support 3 or more times within 10-20 minutes.
2. Selling volume is high, but candles stop closing lower.
3. The final push below support is immediately reclaimed.
4. Enter long on the reclaim close or first pullback above the level.
5. Stop below the absorption low.

### Short Entry
1. Price repeatedly attacks resistance with high buy volume.
2. Break attempts fail to close above the level.
3. A failed breakout candle closes back below resistance.
4. Enter short on the rejection or first retest from below.
5. Stop above the absorption high.

## Exit Rules

- Target 1: VWAP or nearest intraday volume node.
- Target 2: opposite side of the local range.
- Exit immediately if price accepts beyond the absorbed level for 2 candles.

## Filters

- Avoid thin stocks where prints are too sparse to infer absorption.
- Prefer levels that are obvious to many traders.
- Do not fade fresh news-driven breakouts.

## Risk Management

Risk 0.5%-0.75% per trade. This setup needs a tight stop; skip if the stop is wider than the first target.

---
*Category: Order Flow / Reversal | Timeframe: Intraday | Market: VN30F / Liquid HSX Stocks*
