#  Bitcoin Market Sentiment vs Trader Performance Analysis

## Assignment Overview

This project analyzes the relationship between **Bitcoin Market Sentiment (Fear & Greed Index)** and **trader performance** using historical trading data from Hyperliquid.

The objective is to determine whether market sentiment has a measurable impact on trader profitability, trading behavior, and overall market performance. The analysis combines exploratory data analysis, statistical hypothesis testing, and business insights to identify patterns that can support smarter trading decisions.

---

# Dataset Information

## 1. Historical Trader Dataset

Contains historical trading records with features including:

- Account
- Coin
- Execution Price
- Size Tokens
- Size USD
- Side (BUY/SELL)
- Direction
- Closed PnL
- Fee
- Timestamp
- Trade ID
- Order ID
- Transaction Hash

---

## 2. Bitcoin Fear & Greed Index

Contains daily market sentiment information.

Columns include:

- Date
- Fear & Greed Value
- Market Classification

Sentiment Categories:

- Extreme Fear
- Fear
- Neutral
- Greed
- Extreme Greed

---

# Project Objectives

The primary objectives of this analysis are:

- Understand trader behavior under different market sentiments.
- Measure the impact of market sentiment on profitability.
- Compare trader performance across sentiment categories.
- Identify profitable traders and cryptocurrencies.
- Perform statistical validation of observed patterns.
- Generate actionable business recommendations.

---

# Data Preprocessing

The following preprocessing steps were performed:

- Loaded both datasets using Pandas.
- Converted timestamps into datetime format.
- Extracted trading dates.
- Merged trader data with the Fear & Greed Index.
- Removed missing sentiment values.
- Converted numerical columns into appropriate data types.
- Engineered additional features for analysis.

---

# Feature Engineering

The following features were created:

- IsWin
- IsLoss
- Absolute PnL
- Trade Value
- PnL Percentage
- Daily Trading Date

These engineered features improve the quality of downstream analysis.

---

# Exploratory Data Analysis (EDA)

The following analyses were performed.

## Market Analysis

- Distribution of Market Sentiments
- Average Closed PnL by Sentiment
- Total Closed PnL by Sentiment
- Win Rate by Sentiment
- Daily Profit Trend

---

## Trading Behaviour

- BUY vs SELL Performance
- Direction Analysis
- Trade Volume Analysis
- Average Trade Size
- Fee Analysis

---

## Trader Analysis

- Top Performing Traders
- Worst Performing Traders
- Win Rate Analysis
- Average Profit per Trader
- Trading Activity Analysis

---

## Cryptocurrency Analysis

- Most Profitable Coins
- Coin Performance Across Market Sentiments
- Coin-wise Profitability Comparison

---

## Correlation Analysis

Correlation Heatmap between:

- Execution Price
- Size Tokens
- Size USD
- Fee
- Fear & Greed Value
- Closed PnL

---

# Statistical Analysis

## One-Way ANOVA

A One-Way ANOVA test was performed to determine whether trader profitability differs across different market sentiment categories.

### Result

- F-statistic = 9.062
- p-value < 0.001

### Conclusion

The null hypothesis was rejected, indicating that average trader profitability differs significantly across market sentiment categories.

---

## Tukey HSD Post-Hoc Test

Since the ANOVA test identified significant differences, a Tukey HSD test was conducted to determine which market sentiment pairs differed significantly.

Significant differences were observed between selected sentiment categories, confirming that trader performance varies under specific market conditions rather than uniformly across all sentiments.

---

# Visualizations

The notebook includes the following visualizations:

- Market Sentiment Distribution
- Average Profit by Sentiment
- Total Profit by Sentiment
- Win Rate Analysis
- BUY vs SELL Analysis
- Direction Analysis
- Top Traders
- Worst Traders
- Coin Performance
- Correlation Heatmap
- Daily Profit Trend
- Profit Distribution
- Fee vs Profit
- Trade Size vs Profit
- Trader Performance Overview
- Coin Sentiment Heatmap
- Statistical Summary Heatmap

---

# Key Findings

The analysis produced the following major findings:

- Market sentiment has a statistically significant effect on trader profitability.
- Average profitability differs across sentiment categories.
- Only selected sentiment pairs exhibit statistically significant differences according to Tukey HSD analysis.
- Trading performance varies considerably between traders.
- A small number of traders contribute a disproportionately large share of total profits.
- Cryptocurrency selection influences overall profitability.
- Trade size and transaction fees are positively correlated.
- Market sentiment alone does not completely explain profitability; trader behavior also plays an important role.

---

# Business Recommendations

Based on the analysis, the following recommendations are proposed:

### 1. Sentiment-Based Risk Management

Reduce leverage and tighten risk management during Fear and Extreme Fear market conditions.

---

### 2. Dynamic Trading Strategy

Adjust trading strategies according to prevailing market sentiment rather than using a fixed approach.

---

### 3. Trader Benchmarking

Analyze the trading patterns of consistently profitable traders to identify best practices.

---

### 4. Asset Selection

Prioritize cryptocurrencies that demonstrate consistent profitability across multiple market sentiment conditions.

---

### 5. Portfolio Monitoring

Combine market sentiment indicators with trader performance metrics to improve portfolio allocation decisions.

---

# Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Statsmodels
- Jupyter Notebook

---

# Project Structure

```
Assignment/
│
├── dataset/
│   ├── historical_data.csv
│   └── fear_greed_index.csv
│
├── analysis.ipynb
├── README.md
├── requirements.txt
│
└── outputs/
    ├── figures/
    ├── tables/
    └── reports/
```

---

# Statistical Methods Used

- Descriptive Statistics
- Correlation Analysis
- Feature Engineering
- Exploratory Data Analysis
- One-Way ANOVA
- Tukey HSD Multiple Comparison Test

---

# Conclusion

This project demonstrates how market sentiment can be integrated with historical trading data to better understand trader behavior and profitability.

The combination of exploratory analysis and statistical hypothesis testing confirms that market sentiment is associated with meaningful differences in trading outcomes. While sentiment is an important market indicator, trader-specific behavior, asset selection, and risk management also contribute significantly to overall performance.

The findings from this analysis can be used to support the development of more adaptive trading strategies and improved risk management frameworks.

---

## Author

**Ayush Khatri**

Data Science Assignment – PrimeTrade.ai Hiring Process