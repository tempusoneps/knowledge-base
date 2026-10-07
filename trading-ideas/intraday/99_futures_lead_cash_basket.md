# 99 — Futures Lead, Cash Basket Follow

## Overview

Trade liquid VN30 components when futures move first and the cash basket begins to confirm. This is useful during risk-on/risk-off bursts where index futures reveal direction before slower stocks respond.

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 1-min and 5-min |
| Markets | Liquid VN30 components |
| Lead Instrument | VN30F |

### Long Entry
1. VN30F breaks HOD or a major intraday resistance.
2. Basis remains stable or positive.
3. Target stock is above VWAP but still below its own breakout level.
4. Enter stock long when it breaks its 5-min range high.
5. Stop below stock range low or VWAP.

### Short / Sell Entry
1. VN30F breaks LOD or major support.
2. Basis remains stable or negative.
3. Target stock is below VWAP but has not yet broken down.
4. Enter short where available, or sell/avoid, when stock breaks support.
5. Stop above stock range high or VWAP.

## Exit Rules

- Target stock HOD/LOD or 1.5R-2R.
- Exit if VN30F reverses into the old range.
- Take partials when cash basket catches up.

## Filters

- Prefer high index-weight stocks.
- Avoid stocks with independent corporate news against the futures signal.
- Require enough stock liquidity for clean execution.

## Risk Management

Do not use futures stop levels for stock trades. Manage risk on the traded stock.

---
*Category: Futures-Cash Lead-Lag | Timeframe: Intraday | Market: VN30 Stocks*
