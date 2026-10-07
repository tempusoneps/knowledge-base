# 28 — VN30F vs VN30 Cash Index Arbitrage

## Overview

The **VN30F futures contract** should theoretically trade at a **fair value premium** over the VN30 cash index, calculated by the cost of carry (interest rate minus dividends). When the actual premium deviates significantly from fair value — either into excessive premium or discount — a mean-reversion arbitrage opportunity exists. This strategy exploits the convergence of futures price back to fair value, particularly powerful near contract expiry.

---

## Concept

```
Fair Value Formula:
  FV = VN30_Cash × (1 + r × t/365) − Dividends
  r  = risk-free rate (Vietnamese government bond ~4.5%)
  t  = calendar days to contract expiry

Actual Premium = VN30F_Price − VN30_Cash_Index
Fair Value Premium = VN30_Cash × r × t/365

Basis = Actual Premium − Fair Value Premium

If Basis > +0.5%: Futures OVERPRICED → Short Futures, (Hedge with basket long)
If Basis < −0.5%: Futures UNDERPRICED → Long Futures, (Hedge with basket short)
```

---

## Setup & Entry Rules

| Parameter      | Value                                              |
|----------------|----------------------------------------------------|
| Instrument     | VN30F (monthly contract on HNX)                    |
| Reference      | VN30 Index cash (tracked on HOSE)                  |
| Timeframe      | 5-min or real-time monitoring                      |
| Session        | 09:00 – 14:30                                      |
| Min Deviation  | Basis > ±0.5% from fair value                      |

### Long Futures (Underpriced Futures)
1. Calculate fair value premium at current time of day.
2. Actual futures price is below fair value by >0.5%.
3. Futures are "cheap" relative to cash.
4. Enter Long VN30F.
5. (Optional hedge: Short VN30 ETF/basket for pure arb).
6. Stop: If basis widens further to −1.0% (trend may be driving it, not noise).
7. Target: Basis converges back to fair value (0% or slight positive).

### Short Futures (Overpriced Futures)
1. Futures trading at excessive premium (basis > +0.5% above fair value).
2. Enter Short VN30F.
3. Stop: Basis widens to +1.0%.
4. Target: Premium converges to fair value.

---

## Contract Expiry Calendar

```
VN30F Contract Codes (HOSE):
  VN30F2607 = July 2026 expiry (3rd Thursday of month)
  VN30F2608 = August 2026 expiry
  Final Settlement = Average VN30 index last 30 minutes of expiry day

Near expiry (< 5 days):
  - Basis converges STRONGLY to zero
  - Any discount = strong long opportunity
  - Any premium = strong short opportunity
```

---

## Exit Rules

- **Target:** Basis returns to 0% to fair value range.
- **Time Target:** Near expiry, convergence is guaranteed (hold until settlement if needed).
- **Stop:** Basis widens to ±1.5% (systematic buying/selling may be directional, not arb).
- **Best Exit:** Morning session when liquidity is highest for unwinding.

---

## Filters

- [ ] Calculate fair value fresh each morning (r and t change daily).
- [ ] Near expiry week (last 5 days): bias = any discount is a strong long.
- [ ] Heavy foreign net buying day: premium may persist longer.
- [ ] On major macro news days: basis can gap wildly — avoid pure arb.
- [ ] Check if VN30F has sufficient open interest (thin contracts = wide spread arb).

---

## Risk Management

| Rule              | Guideline                                      |
|-------------------|------------------------------------------------|
| Max Risk/Trade    | 1% of account equity                          |
| Stop: Basis widens| Exit if basis moves 0.5% further against you  |
| Max Contracts     | Size based on margin requirement               |
| Leverage          | VN30F leverage ~10–15× — size carefully       |
| Near Expiry       | Higher confidence → can size up               |

---

## Edge & Statistics

- Win rate: **70–80%** for pure basis mean reversion (highly mechanical).
- Pure arb (futures + basket hedge) is near risk-free but requires significant capital.
- Semi-arb (only the futures side): win rate ~65% with small, defined risk.
- **Expiry week**: highest edge — basis MUST converge by settlement.

---

## Example Trade Log

```
Date:         2026-06-25 (expiry week for VN30F2606)
VN30 Cash:    1,274.5
Days to Expiry: 3
Fair Value:   1,274.5 × (1 + 0.045 × 3/365) = 1,274.97
VN30F Price:  1,272.0 (trading at DISCOUNT of 2.97 pts = −0.23% actual, FV at +0.04%)
Basis:        −0.27% vs fair value → Futures underpriced
Entry:        Long VN30F at 1,272.0
Stop:         1,268.5 (if basis widens to −0.55%)
Target:       1,275+ (fair value convergence)
Result:       +WIN, settled at 1,276.1 on expiry day
```

---

## Notes & Improvements

- Build a **real-time basis calculator** in Python using VN30F price from HNX data feed and VN30 index from SSI/VNDIRECT API.
- Track the **basis intraday pattern**: basis often starts negative at open (sellers of futures at ATO) and converges by close.
- **Basket hedge**: buy the 30 VN30 constituent stocks proportionally to hedge the cash leg (requires significant capital — ~5B VND minimum).
- Near expiry, this is closer to a **risk-free trade** — a genuine arbitrage, not just a mean reversion trade.

---

*Category: Arbitrage / Mean Reversion | Timeframe: Intraday | Market: VN30F Futures vs VN30 Cash Index*
