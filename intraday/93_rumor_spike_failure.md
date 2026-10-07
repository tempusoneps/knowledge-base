# 93 — Rumor Spike Failure

## Overview

Fade a rumor-driven spike when price surges on vague information but fails to hold above the impulse base. This setup is practical in markets where unofficial news can move liquid names intraday.

## Setup & Entry Rules

| Parameter | Value |
| --- | --- |
| Timeframe | 1-min and 5-min |
| Markets | Liquid HSX stocks |
| Context | Sudden spike without confirmed disclosure |

### Short / Sell Entry
1. Price spikes more than normal 30-minute ATR on abnormal volume.
2. The catalyst is vague, unconfirmed, or already circulated.
3. Price fails to make a second higher high.
4. Enter short where available, or sell/avoid, when price breaks the spike base.
5. Stop above the failed second high.

### Long Reclaim Entry
1. A downside rumor causes a panic drop.
2. Price stops making new lows and reclaims the drop base.
3. Volume normalizes and bid support returns.
4. Enter long on reclaim retest.
5. Stop below the panic low.

## Exit Rules

- Target VWAP or pre-rumor price.
- Take partials quickly because rumor moves can re-spike.
- Exit if official confirmation validates the rumor.

## Filters

- Do not trade unverified information as fact.
- Require price failure, not just personal skepticism.
- Avoid illiquid names with wide spreads.

## Risk Management

Risk 0.5% maximum. Event invalidation can happen instantly.

---
*Category: Event-Driven / Reversal | Timeframe: Intraday | Market: HSX Stocks*
