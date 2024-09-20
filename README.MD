# **Stock Data Analysis and Risk Management Project**

## **Introduction**

This project involves analyzing stock data using Python and the `yfinance` library. We perform several tasks, including stock data analysis, strategy development with a simple moving average crossover, and risk management through maximum drawdown calculations and a stop-loss mechanism.

## **Project Overview**

### **Tasks**

- **Task 1: Stock Data Analysis**
  - Fetch historical stock data for 5 stocks from the Nifty 50 index over the last 6 months.
  - Perform analysis such as calculating daily percentage changes and moving averages.
  - Plot the closing prices and daily percentage changes for the selected stocks.

- **Task 2: Strategy Development**
  - Develop a simple moving average crossover strategy for one of the 5 stocks.
  - Backtest the strategy and identify buy and sell signals based on the moving averages.
  - Compare the strategy's performance with a simple buy-and-hold approach.

- **Task 3: Risk Management**
  - Calculate the maximum drawdown for each stock over the 6-month period.
  - Implement a stop-loss mechanism (5% stop-loss) for the stock selected in Task 2.
  - Re-run the strategy with the stop-loss and compare its performance to the original strategy.

---

## **Approach and Explanation**

### **Task 1: Stock Data Analysis**

1. **Fetching Data**: 
   We use the `yfinance` library to fetch the stock data for 5 Nifty 50 stocks (`RELIANCE.NS`, `TCS.NS`, `INFY.NS`, `HDFC.NS`, `ICICIBANK.NS`) over the past 6 months. The `auto_adjust=True` option ensures that stock prices are adjusted for corporate actions such as dividends and stock splits.

2. **Daily Percentage Change**:
   The daily percentage change is calculated using the `pct_change()` function on the stock prices, which gives us insight into the day-to-day performance of each stock.

3. **Moving Average Calculation**:
   A 20-day moving average is calculated to smooth out price fluctuations and highlight the stock's trend. This is plotted alongside the closing prices to visualize trends.

4. **Plotting**:
   We plot the closing prices, daily percentage changes, and moving averages to visualize the stock performance.

### **Task 2: Strategy Development**

1. **Simple Moving Average Crossover Strategy**:
   We develop a strategy based on two moving averages (20-day and 50-day SMAs). The strategy is:
   - **Buy** when the 20-day SMA crosses above the 50-day SMA (bullish signal).
   - **Sell** when the 20-day SMA crosses below the 50-day SMA (bearish signal).
   
2. **Backtesting**:
   The strategy is backtested by calculating returns based on buy/sell signals. The performance is compared with a simple buy-and-hold strategy.

3. **Buy and Sell Signals**:
   The buy and sell signals are plotted on the stock price chart to show where the strategy would have triggered buying or selling.

### **Task 3: Risk Management**

1. **Maximum Drawdown Calculation**:
   The maximum drawdown is calculated for each stock. The maximum drawdown is the largest peak-to-trough decline in stock price over the 6-month period.

2. **Stop-Loss Mechanism**:
   For the stock selected in Task 2 (`RELIANCE.NS`), a stop-loss mechanism is implemented to limit losses. If the stock price drops by 5% from the entry price, the position is sold to prevent further losses.

3. **Comparing Performance**:
   The strategy with stop-loss is compared with the original strategy (without stop-loss) and the buy-and-hold approach. The cumulative returns for each strategy are plotted for comparison.

---

## **Code Structure**

### **1. Stock Data Analysis**

- **Fetching Stock Data**:
   We use `yfinance` to download stock data for multiple stocks and calculate daily percentage changes.

- **Moving Average Calculation**:
   We calculate 20-day and 50-day moving averages for each stock.

- **Visualization**:
   We plot closing prices, daily percentage changes, and moving averages.

### **2. Strategy Development**

- **Simple Moving Average Crossover Strategy**:
   The strategy uses 20-day and 50-day SMAs to generate buy/sell signals. We calculate returns based on these signals and compare them to a buy-and-hold approach.

- **Plotting Buy/Sell Signals**:
   The buy and sell signals are plotted on the stock price chart for visual representation.

### **3. Risk Management**

- **Maximum Drawdown Calculation**:
   The maximum drawdown for each stock is calculated to measure the risk.

- **Stop-Loss Implementation**:
   A stop-loss of 5% is implemented to limit losses in the strategy.

- **Comparison**:
   The cumulative returns of the stop-loss strategy are compared with the original strategy and a simple buy-and-hold strategy.

---

## **How to Run the Code**

1. Install the required dependencies:
   ```
   bash
   pip install yfinance matplotlib pandas
   ```
2. Run the Python script or Jupyter Notebook in your preferred environment.

3. The results, including plots and performance comparisons, will be displayed.

## Conclusion

In this project, we successfully analyzed stock data, developed a simple moving average crossover strategy, and implemented risk management techniques like maximum drawdown calculation and a stop-loss mechanism. The project demonstrates the use of Python in stock market analysis and strategy development.

## Requirements
`Python` 3.x
`yfinance` library
`pandas` library
`matplotlib` library



