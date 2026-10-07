# 24 — T+0 Intraday Momentum Scalp (Vietnam-Specific)

## Overview

Vietnam's HOSE market operates on **T+2 settlement**, but since 2021, qualified investors can use **T+0 same-day selling** for stocks they bought on the same day using margin (or in certain broker schemes). This creates a unique intraday opportunity: buy a stock during morning momentum, sell the same day for profit — without needing to wait for T+2. Momentum scalps on highly liquid VN30 stocks using this framework are the most active intraday trading style in Vietnam.

---

## Concept

```
T+0 Mechanism (Vietnam):
  Buy stock at 09:20 → Can sell same day at 13:00 → Net P&L realized
  Available on: Stocks with T+0 eligibility at supported brokers
  Brokers offering T+0: SSI, VNDS, MBS, FPTS, Entrade (DNSE), etc.

Key Advantage:
  No overnight risk → purely intraday
  Leverage effect → more capital efficiency
  Best suited to: Strong momentum moves in first 2 hours of session
```

---

## Setup & Entry Rules

| Parameter    | Value                                                   |
|--------------|---------------------------------------------------------|
| Timeframe    | 1-min and 5-min chart                                   |
| Markets      | VN30 constituents only (most liquid, tight spread)      |
| Preferred    | VCB, BID, VHM, HPG, FPT, MWG, MSN (top 10 liquidity)  |
| Session      | Buy: 09:15–10:30 | Sell: 09:30–14:00                    |
| T+0 Window   | Buy in morning session, sell before 14:15               |

### Long Entry (T+0 Momentum Buy)
1. Stock gaps up >0.5% or shows strong buying at open (ATO higher than prior close).
2. First 5-min candle is bullish with above-average volume.
3. Price is above VWAP and above EMA9.
4. No major resistance within 1% of entry price.
5. VN30 index is positive (broad market support).
6. Enter Long at market or limit just above ask.
7. Stop Loss: Below the first 5-min candle low or below VWAP.

### Sell Strategy
- **Scalp Target:** +0.5% → close 60% of position quickly.
- **Momentum Ride:** Hold 40% with trailing stop for additional +0.5–1%.
- **Hard Exit:** All shares sold by 14:20 (avoid ATC uncertainty).

---

## Stock Selection Criteria (Daily Pre-Market Scan)

Run this scan before 09:00:

```python
filters = {
    "T0_eligible": True,           # Must be T+0 eligible at your broker
    "avg_volume_10d": "> 2M shares",  # Minimum liquidity
    "price_range": "10,000 – 200,000 VND",  # Reasonable price range
    "pre_session_signal": "gap up > 0.3% OR foreign buying > 5B VND yesterday",
    "sector_momentum": "sector trending up on D1"
}
```

---

## Exit Rules

- **T1 (Scalp):** +0.5% from entry → sell 60% immediately.
- **T2 (Momentum):** +1.0% → sell additional 30%.
- **T3 (Runner):** Trailing stop on final 10% until 14:00.
- **Stop Loss:** −0.5% from entry → sell all immediately (discipline critical).
- **Time Force Exit:** Sell ALL holdings by 14:20 no exceptions.
- **Daily max loss:** Stop trading if down −1.5% on T+0 trades.

---

## Cost Consideration (Vietnam-Specific)

```
Transaction costs (approximate):
  Buy fee:   0.15–0.25% of trade value
  Sell fee:  0.15–0.25% of trade value
  Total:     0.30–0.50% round-trip cost

Minimum move needed to profit: > 0.5%
Optimal target: 0.7–1.5% move
Avoid T+0 on stocks with < 0.5% average daily range!
```

---

## Filters

- [ ] Only trade T+0-eligible stocks at your specific broker.
- [ ] Check bid-ask spread: skip if spread > 0.3% (slippage erodes profit).
- [ ] Skip if VN-Index futures (VN30F) are in negative territory (headwind).
- [ ] Skip if stock has an ex-dividend date today or tomorrow.
- [ ] Do not T+0 trade stocks with unusual news (takeover, disclosure) — price can spike both ways.

---

## Risk Management

| Rule              | Guideline                              |
|-------------------|----------------------------------------|
| Max Position Size | 20% of account per T+0 trade           |
| Stop Loss         | Hard −0.5% from entry                  |
| Max T+0 Trades/Day| 5 stocks simultaneously (diversify)    |
| Max Daily Loss    | −1.5% of account → stop T+0 for day   |
| All-Exit Deadline | 14:20 hard cutoff                      |

---

## Edge & Statistics

- Win rate: **60–70%** on strong momentum morning setups.
- Typical profit per win: **+0.5–1.5%** before fees.
- After fees (~0.4% round trip): net ~+0.1–1.1%.
- Best on: Days when VN-Index opens up >0.5% with broad participation.
- Worst on: Reversal days where early momentum fails after open.

---

## Example Trade Log

```
Date:      2026-06-24
Symbol:    FPT (HSX)
T+0:       Eligible at DNSE broker ✓
Pre-market: Foreign bought 12B VND yesterday, sector trending ✓
ATO Price: 125,500 (prior close 124,000, gap +1.2%)
First 5-min: High 126,000 / Low 125,200, bullish, volume 2× ✓
VWAP:      124,800, price above ✓
Entry:     125,800 (Long T+0 at 09:25)
Stop:      124,900 (below first candle low, −0.71%)
T1:        126,800 (+1,000, +0.79%) ← 60% sold at 09:45
T2:        127,500 (+1,700, +1.35%) ← 30% sold at 10:15
Trail:     10% runner, stopped at 127,200 at 11:00
Result:    +WIN, total gain ~+0.9% after fees
```

---

## Notes & Improvements

- Use **broker API** (DNSE/Entrade API) to automate T+0 scalp entries and exits.
- **Risk of not being able to sell T+0**: if broker system is slow or T+0 quota is full, you are stuck holding T+2 — always confirm T+0 eligibility before each trade.
- Track per-stock win rates for T+0 — some stocks (FPT, HPG) respond better than others (VRE, PLX).
- **Best monthly periods**: Beginning of month (institutional rebalancing) and VN30 rebalancing quarters.

---

*Category: T+0 Momentum | Timeframe: Intraday (1-min / 5-min) | Market: HSX Stocks (VN30 Constituents)*
