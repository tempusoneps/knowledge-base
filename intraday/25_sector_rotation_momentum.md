# 25 — Sector Rotation Momentum (Laggard Catch-Up)

## Overview

When one sector leads the market with a strong morning surge, the stocks within that sector that **haven't moved yet (laggards)** tend to catch up within the same session. Institutional sector allocation and retail momentum following both drive this rotation effect. The strategy is to identify the leading sector, find the lagging stocks within it, and buy them as rotation flows in.

---

## Concept

```
Sector Rotation Logic:
  1. Sector Leader runs +2% in first hour (e.g., VCB +2%, BID +1.8%)
  2. Sector Laggard hasn't moved yet (e.g., CTG +0.2%)
  3. Rotate: Buy CTG expecting it to catch up to VCB/BID level

Why it works:
  - Fund managers buy the entire sector basket, just delayed
  - Retail traders notice the hot sector and buy laggards
  - Index rebalancing creates systematic sector-wide pressure
```

**Correlation framework:**
```
Banking Sector: VCB, BID, CTG, TCB, MBB, VPB, STB, HDB
Real Estate:    VHM, VIC, NVL, DXG, KDH, BCM
Steel/Material: HPG, HSG, NKG
Tech:           FPT, CMG, VGI
Retail:         MWG, PNJ
```

---

## Setup & Entry Rules

| Parameter    | Value                                             |
|--------------|---------------------------------------------------|
| Timeframe    | 5-min for entry; 1-min for scan                   |
| Markets      | VN30 stocks and mid-cap HSX stocks in same sector |
| Session      | 09:30 – 12:00 (rotation happens in morning)       |
| Lead/Lag Gap | Leader up >1.5%, Laggard up <0.5%                |

### Entry Process
1. By 09:45, identify the **leading sector** (best-performing sector, check 2-3 stocks).
2. Within that sector, find stocks that are up <0.5% while leaders are up >1.5%.
3. Confirm the laggard stock is above its VWAP and EMA50.
4. Laggard must be liquid enough (>500K shares traded so far).
5. Enter Long on the laggard at market or just above the ask.
6. Stop Loss: Below the laggard's session low or below VWAP.

### Exit Rules
- **Target:** Laggard catches up to the percentage move of the sector leader (e.g., if leader at +2%, target laggard reaching +1.5–2%).
- **Time Limit:** Most rotation happens before 11:30 — exit by 12:00.
- **Sector Fade:** If sector leader starts pulling back, exit laggard immediately.
- **Trail:** Trail stop below each 5-min higher low.

---

## Sector Momentum Scorecard (Morning, 09:45)

| Sector      | Leader Stocks         | Laggard Candidates    | Threshold  |
|-------------|----------------------|----------------------|------------|
| Banking     | VCB, BID, CTG        | TCB, MBB, VPB        | Leader >1% |
| Real Estate | VHM, VIC             | NVL, KDH, DXG        | Leader >1.5%|
| Steel       | HPG                  | HSG, NKG             | Leader >2% |
| Tech        | FPT                  | CMG, VGI             | Leader >1% |
| Retail      | MWG                  | PNJ                  | Leader >1% |

---

## Filters

- [ ] Sector move must be broad (at least 2 leaders up) — not just 1 stock news.
- [ ] Laggard must have positive pre-market sentiment (no negative news).
- [ ] Check if laggard has its own upcoming news (can decouple from sector).
- [ ] Avoid if the overall VN-Index is flat or negative (weak rotation environment).
- [ ] Skip laggards that already moved >50% of the leader's gain (too late to rotate).

---

## Risk Management

| Rule              | Guideline                             |
|-------------------|---------------------------------------|
| Max Risk/Trade    | 0.75% per laggard stock               |
| Max Laggards      | 2–3 simultaneously (diversify sector) |
| Stop Placement    | Below session low or VWAP             |
| Time Exit         | 12:00 hard exit for rotation trades   |
| Daily Loss Limit  | −2%                                   |

---

## Edge & Statistics

- Win rate: **60–70%** when sector move is broad and genuine.
- Average gain: **+0.5–1.5%** on the laggard catch-up.
- Best on: Sector-specific catalyst days (NHNN rate cut → banks, infrastructure news → real estate).
- Worst on: Stock-specific news driving one name — won't rotate to the whole sector.

---

## Example Trade Log

```
Date:         2026-06-22
Sector:       Banking (NHNN signals rate hold — positive for banks)
Leaders:      VCB +2.1% by 09:45, BID +1.8%
Laggard:      TCB +0.3% (same sector, not moved)
VWAP:         TCB above VWAP ✓
Volume:       TCB starting to pick up volume ✓
Entry:        42,500 (Long TCB at 09:50)
Stop:         41,800 (below session low, −1.65%)
Target:       Leader average = +2% → TCB target +1.5% = 43,138
T1:           43,000 (+500, +1.18%) ← 70% at 10:20
T2:           43,300 (+800, +1.88%) ← 30% at 11:00
Result:       +WIN (TCB caught up to sector)
```

---

## Notes & Improvements

- Automate a **sector dashboard**: real-time P&L of each sector and each stock within it, sorted by gain.
- Build a **rotation alert**: fires when leader stock is up >1.5% but 2+ sector peers are still flat.
- Track **rotation speed**: how quickly does the average laggard catch up on strong sector days? (Usually 1–3 hours).
- Combine with **T+0**: sector rotation laggard buys are ideal T+0 candidates — buy, sell same day on the catch-up.

---

*Category: Sector Momentum | Timeframe: Intraday (5-min) | Market: HSX Stocks (Sector Baskets)*
