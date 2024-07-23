# 📈 Analyzing Time Series Data for Tesla 📈

## 📋 Overview

This project focuses on analyzing time series data to extract meaningful statistics and identify trends using real-world stock market data.

### Introduction

**Purpose**: The primary aim of this project is to analyze stock market data over the past month to identify trends and significant changes in price and volume.
![overview](https://github.com/user-attachments/assets/1a096bc3-7bfb-45d0-98dc-6688ea90260d)

### Summary of Rules

  1.Load stock data for Tesla for the past month using yfinance.
  
  2. Calculate daily percentage changes in stock price and volume using the natural logarithm.
     
  3. Add rolling window calculations for total volume over the previous two days and the next day's volume.
     
  4. Filter the data to identify significant price changes, defined as changes greater than 5% in absolute 

**Scope**: The project involves:
- Loading Tesla stock market data using the `yfinance` library.
- Calculating daily percentage changes in stock price and volume.
- Applying rolling window calculations to analyze trends over time.
- Filtering data to identify days with significant price changes.

### Sample Output:
Running this script will display the analysis of significant changes over a particular stock over the past month:
![data](https://github.com/user-attachments/assets/f5e7f20b-f559-48f9-9d53-be47afefa761)

**Insights**:
- **Daily Percentage Changes**: Calculating the daily percentage changes in stock price and volume helps in identifying short-term trends and volatility.
- **Rolling Window Calculations**: Analyzing the total volume over the previous two days and predicting the next day's volume provides insights into trading patterns.
- **Significant Price Changes**: Filtering for significant price changes helps in identifying key events or trading days that had a major impact on the stock price.

### Data Source
```python
print("Loading stock market data for Tesla...")
# Load stock market data for Tesla for the past month
ticker = 'TSLA'
tkr = yf.Ticker(ticker)
df = tkr.history(period='1mo')
print("Data loaded.")
```
The data for this project comes from Yahoo Finance, accessed using the `yfinance` Python library. This allows us to work with real-time and historical stock market data, providing a realistic context for our analysis.

### 🔍 Key Components
*Filtering for Significant Changes:
The code filters the data to identify days with significant price changes. A "significant" change is defined as an absolute daily percentage change in price greater than 5% (0.05). This is completly adjustable based on modification for flexability and use case.

![changepercentage](https://github.com/user-attachments/assets/74d9bd89-6f1a-4f61-bd22-660e6be7cb1a)

### Bigger Scope and Applications

The techniques used in this exercise can be applied to various real-world scenarios beyond analyzing Tesla's stock data. By understanding trends and significant changes in time series data, businesses can make informed decisions in areas such as:

- **Stock Market Analysis**: Identifying trends and making investment decisions based on historical data.
- **Sales Forecasting**: Predicting future sales based on past performance to optimize inventory and marketing strategies.
- **Financial Planning**: Analyzing income and expenses over time to create effective budgeting plans.
- **Economic Indicators**: Studying trends in economic data to forecast future economic conditions.

By using real-time data and sophisticated analysis techniques, this project demonstrates the practical applications of time series analysis in various business contexts.
