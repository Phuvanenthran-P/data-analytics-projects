# 📈 Stock Market Analysis: SMA & EMA Trend Tracker

A Python notebook that pulls intraday stock data from Yahoo Finance and analyzes price trends with 50-period Simple (SMA) and Exponential (EMA) moving averages, shown in static and interactive charts.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Phuvanenthran-P/data-analytics-projects/blob/main/stock-market-analysis/stock_market_analysis.ipynb)

## What It Does

- Fetches 1-minute interval data for a chosen ticker (default: AAPL) using `yfinance`
- Cleans the data (missing-value check and removal)
- Calculates 50-period SMA and EMA on the closing price
- Detects bullish and bearish EMA/SMA crossovers
- Plots price vs SMA vs EMA with Matplotlib (static) and Plotly (interactive)
- Refreshes the data on a timed interval to simulate live updates

## Tech Stack

Python · Pandas · yfinance · Matplotlib · Plotly · Google Colab

## How to Read the Chart

- Price above both averages suggests short-term upward momentum.
- EMA reacts faster than SMA because it weights recent prices more.
- An EMA/SMA crossover is a common trend-change signal.

## Run It

Click the Colab badge above, or locally:

```bash
pip install yfinance pandas matplotlib plotly
jupyter notebook stock_market_analysis.ipynb
```

## Limitations

- Yahoo Finance data can be delayed and rate-limited.
- Intraday data is only available around market hours.
- Moving averages lag price and are not predictive.

## Future Improvements

- Multi-stock comparison
- RSI and MACD indicators
- Streamlit deployment

## Disclaimer

Educational project. Not financial advice.
