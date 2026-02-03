# Trader Behavior vs Market Sentiment (Fear & Greed Analysis)

## Overview
This project analyzes how trader performance and behavior change under different market sentiment regimes (Fear vs Greed).  
We combine historical trade-level data with the Crypto Fear & Greed Index to study performance, behavioral shifts, and actionable trading insights.

---

## Datasets
1. **historical_data.csv**
   - Trade-level data including trader account, PnL, trade size, position size, direction, and timestamps.

2. **fear_greed_index.csv**
   - Daily market sentiment classified as Fear or Greed with a numerical sentiment score.

---

## Methodology

### 1. Data Preparation
- Loaded and validated both datasets (missing values, duplicates).
- Converted timestamps (milliseconds → datetime).
- Aggregated trades at a **daily per-trader** level.
- Engineered key metrics:
  - Daily PnL
  - Win rate
  - Trade frequency
  - Average position size (leverage proxy)
  - Long/Short ratio

### 2. Data Alignment
- Merged trader-day metrics with daily sentiment data.
- Analysis performed at the daily granularity.

---

## Analysis Performed
- Performance comparison between Fear and Greed regimes.
- Behavioral changes based on sentiment.
- Trader segmentation:
  - High vs low leverage
  - Frequent vs infrequent traders
  - Consistent vs inconsistent performers

---

## Key Findings
- Traders perform better on average during Greed regimes.
- Fear regimes increase downside risk, especially for high-leverage traders.
- Trading behavior (frequency, leverage, directional bias) changes significantly with sentiment.

---

## Actionable Insights
- Reduce leverage during Fear periods, especially for aggressive traders.
- Increase trade frequency selectively during Greed regimes for experienced traders.

---

## Repository Structure
