# 120 — Market-on-Close Drift

## Overview

Trade directional drift into the close when expected market-on-close demand or supply is confirmed by price, volume, and sector behavior. The setup follows real late-day flow instead of predicting the auction blindly.

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 1-min and 5-min |
| Markets | Liquid HSX stocks, VN30 components |
| Context | Final 45 minutes before ATC |

### Long Entry
1. Stock holds above VWAP into the final hour.
2. Volume pace increases after 13:45.
3. Pullbacks become shallow and closing-range lows hold.
4. Sector or basket remains strong.
5. Enter long on final-hour range breakout.

### Short / Sell Entry
1. Stock holds below VWAP into the final hour.
2. Volume pace increases on down moves.
3. Bounces fail below closing-range highs.
4. Sector or basket remains weak.
5. Enter short where available, or sell/avoid, on final-hour breakdown.

## Exit Rules

- Take partials before ATC if price reaches extension target.
- Close before auction if auction imbalance is unknown.
- If explicitly trading ATC, predefine max auction slippage.

## Filters

- Avoid if late volume is just one block print without follow-through.
- Stronger during rebalance, month-end, or index event sessions.
- Require broad confirmation, not one candle.

## Risk Management

Late-day trades need smaller size and strict time stops. Do not let an intraday drift idea become an overnight position by accident.

---
*Category: Closing Flow / Momentum | Timeframe: Intraday | Market: HSX Stocks / VN30 Components*
