# 05 — Reinforcement Learning PPO Allocator

## Overview
Implement Proximal Policy Optimization (PPO) reinforcement learning to dynamically allocate weights to a basket of assets based on Sharpe ratio reward optimization.

## Setup & Entry Rules
- State space: Covariance matrix, momentum indicators, and rolling volatility of a 10-asset basket.
- Action space: Continuous portfolio weights summing to 1.0.
- Update portfolio allocations daily according to PPO agent output.

## Exit Rules
- Dynamic daily adjustments. Complete exit if agent weight for a specific asset drops to 0.

## Filters
- Apply a transaction cost penalty in the reward function to prevent high turnover.
- Limit rebalancing if daily volatility exceeds a pre-defined threshold.

## Risk Management
- Limit maximum weight of any single asset to 25%. Maintain a cash buffer of at least 10%.

---
*Category: Reinforcement Learning | Timeframe: Daily | Market: Multi-Asset / ETFs*
