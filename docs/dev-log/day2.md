1. Research common quantitative indicators.
2. Study how trading strategies are typically structured.
3. Begin designing example QuantDSL programs.
4. Identify the minimum feature set required for Version 1.

# Day 2 Development Log: Research

## Common quantitative indicators

### Indicators Investigated

- **Moving Average (MA):** Smooths price data to identify the overall market trend by averaging prices over a chosen period.
- **Exponential Moving Average (EMA):** Similar to an MA but gives greater weight to recent prices, making it more responsive to market changes.
- **Stochastic Oscillator:** Measures momentum by comparing the closing price to its recent trading range, heslping identify overbought and oversold conditions.
- **MACD (Moving Average Convergence Divergence):** Measures momentum by comparing two moving averages and highlights potential trend changes through line crossovers.
- **Bollinger Bands:** Uses a moving average with upper and lower bands to measure market volatility and identify unusually high or low prices.
- **Relative Strength Index (RSI):** Measures the strength and speed of price movements, commonly used to identify overbought and oversold markets.
- **Fibonacci Retracement:** Uses Fibonacci ratios to identify potential support and resistance levels during price pullbacks.
- **Ichimoku Cloud:** A comprehensive indicator that combines trend direction, momentum, and support/resistance into a single chart.
- **Standard Deviation:** Measures market volatility by showing how much prices deviate from their average.
- **Average Directional Index (ADX):** Measures the strength of a trend regardless of its direction, helping traders determine whether a market is trending or ranging.

### Key Takeaways

- No single indicator guarantees accurate trading signals.
- Indicators are most effective when used together rather than in isolation.
- Different indicators specialise in analysing trends, momentum, volatility, or support and resistance.
- Choosing the right indicator depends on the trading strategy and market conditions.

## General trading stategies

# Trading Strategy Structure

### 1. Market

Define what will be traded.

- Forex
- Stocks
- Cryptocurrency
- Indices
- Commodities

### 2. Timeframe

Specify the chart timeframe.

- 1 minute (M1)
- 5 minute (M5)
- 15 minute (M15)
- 1 hour (H1)
- 4 hour (H4)
- Daily (D1)

### 3. Trend Identification

Determine the current market direction.

Examples:

- Price above the 200 EMA = Uptrend
- Price below the 200 EMA = Downtrend
- Higher highs and higher lows

### 4. Setup

Describe the conditions that must exist before considering a trade.

Example:

- Uptrend confirmed
- RSI below 40
- Price pulls back to the 21 EMA

### 5. Entry Rules

Specify the exact trigger for entering.

Example:

- Bullish engulfing candle
- MACD crossover
- Break and retest of resistance
- Close above previous high

### 6. Stop Loss

Define where the trade becomes invalid.

Examples:

- Below the previous swing low
- 20 pips below entry
- Below support

### 7. Take Profit

Specify the exit target.

Examples:

- Next resistance level
- 2:1 Risk-to-Reward ratio
- Fibonacci extension

### 8. Trade Management

Explain how the trade will be managed.

Examples:

- Move stop loss to break-even after 1R
- Trail stop using the 21 EMA
- Close half the position at 2R

### 9. Exit Rules

Define when to close the trade early.

Examples:

- Opposite MACD crossover
- Strong reversal candle
- Trend breaks

### 10. Risk Management

Control losses.

Examples:

- Risk 1% of account per trade
- Maximum 3 trades per day
- Stop trading after 3 consecutive losses

### 11. Backtesting

Test the strategy using historical data.

Record:

- Win rate
- Average reward-to-risk ratio
- Profit factor
- Maximum drawdown
- Number of trades

### 12. Trading Journal

After each trade record:

- Date
- Instrument
- Entry
- Exit
- Profit/Loss
- Screenshot
- Mistakes
- Lessons learned

__Example__

Market: EUR/USD

Timeframe: 15 Minutes

Trend:

• Price above 200 EMA

Setup:

• Pullback to the 21 EMA

• RSI below 40

Entry:

• Bullish engulfing candle closes above the 21 EMA

Stop Loss:

• Below the recent swing low

Take Profit:

• 2:1 Risk-to-Reward

Management:

• Move stop to break-even at 1R

• Take 50% profit at 2R

• Let the remaining position run

Risk:

• Risk 1% of account

• Maximum 2 trades per day