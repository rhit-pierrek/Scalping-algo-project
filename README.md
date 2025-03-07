# Forex Scalping Strategy - EUR/USD Analysis

## Project Overview

This project implements a **scalping strategy** for the **EUR/USD Forex market**, leveraging key technical indicators to identify buy and sell signals. The primary objective was to explore **international financial markets** by developing a backtested algorithm that can be applied to real-world trading scenarios. 

### **Why This Project?**
This scalping strategy was designed to:
- **Analyze international forex trends** using historical EUR/USD price data.
- **Backtest technical indicators** to assess strategy effectiveness.
- **Develop algorithmic trading strategies** for potential automation in international financial markets.
- **Adapt trading signals for different market conditions** and time zones.

By working on this project, I learned about **quantitative finance, backtesting methodologies, and market behavior**, while also improving my skills in **data processing and algorithm development**.

---

## Strategy Explanation

The strategy utilizes the following **technical indicators**:
- **Exponential Moving Averages (EMA)**
  - Fast EMA: 30-period
  - Slow EMA: 50-period
- **Relative Strength Index (RSI)**
  - 7-period RSI to measure market momentum
- **Bollinger Bands (BBANDS)**
  - 15-period bands with 1.5 standard deviations to identify price deviations
- **Average True Range (ATR)**
  - 7-period ATR to measure volatility

### **Buy and Sell Signals**
- **Buy Signal (Long Position)**:
  - Fast EMA crosses **above** Slow EMA
  - Price is near **lower Bollinger Band**
- **Sell Signal (Short Position)**:
  - Fast EMA crosses **below** Slow EMA
  - Price is near **upper Bollinger Band**

### **Risk Management: Stop Loss & Take Profit**
This strategy includes a built-in risk management system:
- **Stop Loss (SL):**
  - Set **1.1 times the ATR** below (for long trades) or above (for short trades) the entry price.
- **Take Profit (TP):**
  - Set at **1.5 times the SL distance** to ensure a favorable risk-reward ratio (1:1.5).
- **Trade Execution:**
  - A trade is executed only if there are no open trades (`len(self.trades) == 0`).
  - If a **buy signal** is triggered, the bot buys with a defined SL and TP.
  - If a **sell signal** is triggered, the bot sells with a defined SL and TP.

This ensures **controlled risk exposure** to minimize losses.

---

## Installation & Setup

### 1. Clone the Repository
```sh
git clone https://github.com/your-username/forex-scalping-strategy.git
cd forex-scalping-strategy
```

### 2. Install Dependencies
Make sure you have **Python 3.8+** installed. Then, install the required libraries:
```sh
pip install pandas numpy matplotlib pandas-ta tqdm
```

### 3. Load the Data
The dataset used is a historical **EUR/USD** candlestick dataset with 5-minute intervals.
```sh
EURUSD_Candlestick_5_M_ASK_30.09.2019-30.09.2022.csv
```
Ensure the dataset is in the same directory as the notebook.

### 4. Run the Strategy
Open the Jupyter Notebook and execute all cells to generate trading signals.
```sh
jupyter notebook 01_Strategy_Scalping_Modified_I.ipynb
```

---

## Key Insights from the Strategy

- **International Forex Markets Are Volatile**: Learned how the EUR/USD pair reacts VERYYYY differently to economic events.
- **Technical Indicators Can Improve Trading**: EMA crossovers and Bollinger Bands effectively helped me identify entry and exit points.
- **Algorithmic Trading Feasibility**: The model shows potential for automation in forex trading strategies. And I can see myself in the future improving it and adding it to my portoflio. 
- **Risk Management Works**: The built-in **stop loss and take profit** system ensures controlled risk exposure, and takes all the emotion out of trading. Doesn't allow me to jump into any trades arbitrarily.
- Also showed me how much I love backtesting for scenarios such as these. 

---

## Future Improvements
- **Explore Machine Learning** to optimize signal generation.
- **Expand strategy testing** to other currency pairs.
- **Integrate with live trading APIs** (e.g., Binance, OANDA) for real-world deployment.




