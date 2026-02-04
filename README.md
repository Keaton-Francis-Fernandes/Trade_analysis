# Market Sentiment vs Trader Behavior on Hyperliquid
## Objective

This project analyzes how market sentiment (Fear vs Greed) influences trader behavior and performance on the Hyperliquid platform.
The goal is to uncover actionable patterns that can inform smarter trading decisions, risk management, and capital allocation.

Rather than focusing purely on prediction accuracy, the emphasis is on:

behavioral shifts under different sentiment regimes

performance differences across trader segments

translating insights into practical trading rules

## Data Overview

The project uses two primary datasets:

Hyperliquid trading data

Trades, positions, PnL, leverage, and account-level activity

Market sentiment data

Daily Fear/Greed sentiment index

All analysis is performed at a daily aggregation level to ensure consistent alignment across datasets.

### Part A — Data Preparation

The following preprocessing steps are performed:

Loaded and inspected both datasets

documented number of rows and columns

checked for missing values and duplicates

Converted timestamps and aligned both datasets by date

Created key daily metrics, including:

daily PnL per account

win rate

average position size

trade intensity (number of trades per day)

long/short ratio

sentiment lag features

volatility proxies

These steps ensure the data is clean, comparable, and suitable for behavioral analysis.

### Part B — Analysis
1. Performance vs Sentiment

We compare trader performance across Fear and Greed days using:

daily PnL

win rate

volatility / instability proxies

This highlights how outcomes differ depending on market psychology.

2. Behavioral Changes Under Sentiment

We analyze how traders adapt their behavior under different sentiment regimes:

changes in trade frequency

position sizing and exposure

long/short bias

lagged sentiment effects on next-day behavior

3. Trader Segmentation

To uncover non-uniform effects, traders/days are segmented into groups such as:

high vs low trade intensity

larger vs smaller average positions

more consistent vs volatile outcomes

Comparisons across these segments reveal which behaviors are more robust under Fear or Greed.

4. Key Insights

The analysis produces multiple evidence-backed insights supported by charts and tables, for example:

sentiment effects are stronger with a one-day lag than same-day sentiment

high activity during Fear days amplifies downside risk

selective participation outperforms constant trading during volatile sentiment regimes

### Part C — Actionable Output

Instead of stopping at analysis, the project translates insights into decision-support outputs.

A probabilistic framework is used to estimate:

Probability of a good trading day

Recommended trade action:

Trade

Reduced Trade

Skip

Risk-aware capital allocation

Estimated maximum loss

## Output File

The final output is a CSV file containing:

Date

Probability of a good trading day

Trade decision

Recommended investment amount

Estimated maximum loss

This makes the results directly usable in a real trading workflow.

## Modeling Approach (Bonus)

A lightweight predictive approach is explored using:

sentiment features

lagged behavior metrics

volatility proxies

Given the small sample size and class imbalance, the focus is on probability scoring and risk management, not overfitting complex models.
This design choice prioritizes robustness and interpretability.

## Project Strengths

Clear alignment between sentiment, behavior, and performance

Emphasis on actionable insights, not just visualization

Risk-aware recommendations instead of binary predictions

Reproducible workflow with clean preprocessing steps

## How to Run

Clone the repository

Open the notebook (.ipynb) in Jupyter or Google Colab

Run cells sequentially (data loading → analysis → output generation)

Review generated charts and the final CSV output

## Summary

This project demonstrates how market sentiment can be systematically linked to trader behavior and outcomes, and how those insights can be converted into practical trading rules.
The result is not just analysis, but a decision-support framework grounded in data.
