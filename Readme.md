# Gavekal Framework Analysis: Equities vs Gold

This project implements the Gavekal research framework to analyze the structural relationship between equity markets and gold prices. The analysis visualizes when equities are in a "Structural Bear" regime relative to gold, which often indicates periods of monetary illusion or inflationary stress.

## 📊 Analysis Overview

The Gavekal framework suggests that the ratio of an equity index to the local price of gold serves as a long-term indicator of market structure. When the ratio falls below its 7-year moving average, it signals a "Structural Bear Market" where monetary illusion is breaking down.

This implementation calculates and visualizes this relationship for three major markets:
- **United States**: S&P 500 Index (^GSPC) vs Gold (GC=F)
- **Singapore**: Straits Times Index (^STI) vs Gold converted to SGD (USDSGD=X)
- **Hong Kong**: Hang Seng Index (^HSI) vs Gold converted to HKD (USDHKD=X)

## 🚀 Features

- Automated data retrieval using Yahoo Finance API
- Calculation of equity/gold ratios in local currency terms
- 7-year (1,764 trading days) moving average computation
- Professional visualization with structural bear regime shading
- Log-scale plotting for long-term trend analysis
- Robust error handling for data alignment and missing values

## 📈 Methodology

For each market, the analysis:
1. Fetches daily price data from 1990-01-01
2. Calculates local gold price (Gold × FX rate for non-US markets)
3. Computes the ratio: Equity Index / Local Gold
4. Applies a 7-year rolling average as the structural threshold
5. Shades periods where the ratio falls below this threshold

## 🛠️ Installation

```bash
pip install yfinance pandas numpy matplotlib seaborn