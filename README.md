# Personal Trading Performance Analysis

## Overview
End-to-end analysis of my real MT4 forex trading history across EURUSD and GBPUSD (May–June 2026). Built to identify performance patterns, quantify edge, and uncover behavioural weaknesses using data.

## Live Dashboard
[View on Tableau Public](https://public.tableau.com/views/trading-analysis/PersonalTradingPerformanceDashboard)

## Dataset
- 65 closed trades extracted from MT4 platform
- Fields: entry/exit price, direction, P&L, commission, volume, exit reason, duration
- Raw data: 135 rows (paired In/Out legs per trade)

## Notebooks
- `01_trading_analysis.ipynb` — data engineering, EDA, equity curve, performance by direction/exit/duration
- `02_trading_sql.ipynb` — SQLite database setup and 5 SQL queries (day of week, position size, streaks, top trades, weekly P&L)

## Key Findings
- **Net P&L: +$300.19** across 65 trades after $93.81 commission
- **Win rate: 33.8%** with a 2.55 R:R ratio — strategy is asymmetric by design
- **Sell trades generated $578** vs Buy trades losing $278 — clear directional edge
- **Manual exits destroy value** — mobile closes average -$3.71 vs +$2.92 for stop loss exits
- **Trade duration is the strongest predictor of outcome** — trades under 30 mins lose $440 net; trades over 8 hrs are 100% profitable
- **Thursday and Wednesday** are the most profitable trading days

## Tools
Python, pandas, matplotlib, seaborn, SQLite, Tableau Public