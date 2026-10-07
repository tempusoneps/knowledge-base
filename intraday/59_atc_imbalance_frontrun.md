# 59 — End of Day (ATC) Imbalance Front-Run

## Overview

In the Vietnamese market, the **ATC (At The Close)** session (14:30 - 14:45) is a batch auction that determines the closing price. Often, massive institutional orders (especially during ETF rebalancing days or options expiry) are placed into the ATC, causing significant price imbalances. The **ATC Imbalance Front-Run** strategy seeks to anticipate the direction of the ATC auction by analyzing the aggressive order flow leading into it (14:15 - 14:30) and entering a position *before* the auction begins, holding it into the close.

---

## Concept

```
The Logic:
  If a major fund needs to buy 5 million shares of VNM at the close, they cannot just dump it all into the ATC without causing a massive price spike.
  They will begin quietly buying aggressively in the continuous session leading up to the ATC (14:15 - 14:30) to secure inventory.
  This creates a "pre-ATC momentum curve."
  By identifying this late-day urgency, you can front-run the final ATC spike.
```

**Trade Logic:** You are betting that the late-day continuous momentum is a precursor to a massive imbalance in the ATC auction.

---

## Indicators Required

| Indicator      | Setting                      | Purpose                                  |
| -------------- | ---------------------------- | ---------------------------------------- |
| Time & Sales   | Real-time tape               | Spot institutional urgency               |
| Volume         | 1-min chart                  | Confirm rising volume into the close     |
| Market Context | ETF Rebalance / Expiry Dates | High probability days for this setup     |

---

## Setup & Entry Rules

| Parameter | Value                                          |
| --------- | ---------------------------------------------- |
| Timeframe | 1-min chart                                    |
| Markets   | VN30 Constituents (ETF heavy stocks)           |
| Context   | The window between 14:15 and 14:29             |

### Long Entry (Front-Running ATC Buy Imbalance)
1. **The Time:** It is after 14:15.
2. **The Tell:** A specific VN30 stock begins a relentless, steady climb on a 1-min chart. Volume is steadily increasing with every minute.
3. **The Tape:** Time & Sales shows continuous "sweeping" of the Ask (buying market orders).
4. **Trigger:** The stock breaks its afternoon intraday high between 14:20 and 14:28.
5. **Entry:** Go Long at market before 14:29 (before continuous trading stops).
6. **Stop Loss:** Just below the VWAP of this late-day move.

### Short Entry (Front-Running ATC Sell Imbalance)
1. **The Time:** After 14:15.
2. **The Tell:** Stock begins heavy, relentless selling. 1-min candles are stacking red.
3. **Trigger:** Breaks the afternoon low on increasing volume.
4. **Entry:** Go Short (via VN30F or T+0) before 14:29.
5. **Stop Loss:** Above the high of the late-day move.

---

## Exit Rules

- **The Exit:** You do not exit during the continuous session. You hold the position *into* the ATC auction (14:30 - 14:45).
- **Execution:** Place an ATC order to close your position. Your order will be matched at the final closing price determined by the auction.
- **The Bet:** You are betting the final ATC price will be significantly higher (for a Long) than your entry price at 14:28 due to the institutional imbalance clearing.

---

## Filters

- [ ] **Crucial:** This strategy has the highest probability on **VN30F Expiry Days** (3rd Thursday of the month) and **ETF Rebalancing Days** (usually a Friday near the end of a quarter).
- [ ] If the stock is just chopping sideways between 14:15 and 14:28 on low volume, do not guess the ATC direction. Stay out.
- [ ] Ensure you actually enter the closing ATC order before 14:45, otherwise you will be stuck holding overnight.

---

## Risk Management

| Rule             | Guideline                          |
| ---------------- | ---------------------------------- |
| Max Risk/Trade   | 0.5% of account equity (Can gap against you in ATC) |
| Stop Placement   | Hard stop during continuous; Uncontrollable during ATC |
| Min R:R          | Variable (Depends on the size of the ATC imbalance) |

---

## Edge & Statistics

- **Win rate:** 65-75% *specifically* on ETF rebalance days. Much lower on normal days.
- **Edge:** Exploiting the mechanical necessity of passive funds that MUST trade at the closing price, regardless of how much it moves the market.

---

## Example Trade Log

```
Date:      2026-06-19 (ETF Rebalance Friday)
Symbol:    MSN (HSX)
Context:   MSN has been flat all day at 75,000.
The Tell:  At 14:20, massive volume starts hitting the Ask. Price climbs to 75,500 by 14:25.
Entry:     75,800 (Long, bought at market at 14:28)
Exit Plan: Entered ATC sell order at 14:35.
The Auction: A massive 2-million share buy order hits the ATC tape.
Result:    ATC matching price closes at 76,900. Trade closed automatically. +WIN (+1,100 pts in 15 mins).
```

---

## Notes & Improvements
- Track historical ATC behavior for specific stocks. Some stocks (like SAB or VIC) are notorious for wild ATC swings.
- This is an advanced strategy because once the ATC starts, you cannot exit if the price goes against you until the auction clears. Size down accordingly.

---
*Category: Market Microstructure / Auction Fade | Timeframe: 14:15 - 14:45 | Market: VN30 Stocks*
