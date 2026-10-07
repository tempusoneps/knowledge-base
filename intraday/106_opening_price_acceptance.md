# 106 — Opening Price Acceptance

## Overview

Trade in the direction of the open only after the market proves it accepts the opening price. This avoids both blind gap fading and blind gap chasing.

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 5-min chart |
| Markets | VN30F, liquid stocks |
| Context | First 30-45 minutes |

### Long Entry
1. Market opens above PDC.
2. First 30 minutes hold above the opening price and VWAP.
3. Pullback into the opening price is rejected.
4. Enter long when price breaks the rejection candle high.
5. Stop below opening price acceptance zone.

### Short Entry
1. Market opens below PDC.
2. First 30 minutes stay below the opening price and VWAP.
3. Bounce into the opening price is rejected.
4. Enter short when price breaks the rejection candle low.
5. Stop above opening price acceptance zone.

## Exit Rules

- Target morning high/low, then 2R.
- Exit if price crosses and accepts on the other side of the opening price.
- Time stop before lunch if no follow-through.

## Filters

- Avoid tiny opens where the opening price has no information.
- Best when opening volume is above average.
- Confirm with index direction for single stocks.

## Risk Management

Define the opening acceptance zone before entry. Do not move it after price tests it.

---
*Category: Opening Structure / Acceptance | Timeframe: Intraday | Market: VN30F / HSX Stocks*
