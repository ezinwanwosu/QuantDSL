# How QuantDSL Works

QuantDSL is a Haskell-based domain-specific language (DSL) for defining and evaluating quantitative trading strategies.

Users write trading rules in a simple, human-readable format:

```text
BUY AAPL
WHEN SMA(20) > SMA(50)

SELL AAPL
WHEN SMA(20) < SMA(50)
```

The system processes these strategies through several stages:

```text
Strategy File
    ↓
Parser
    ↓
Abstract Syntax Tree (AST)
    ↓
Interpreter
    ↓
Backtesting Engine
    ↓
Performance Report
```

## Example Workflow

### 1. Define a Strategy

A user creates a strategy file:

```text
BUY AAPL
WHEN SMA(20) > SMA(50)

SELL AAPL
WHEN SMA(20) < SMA(50)
```

### 2. Parse the Strategy

The parser converts the text into an internal representation (AST) that the system can understand and evaluate.

### 3. Run a Backtest

The system loads historical market data and:

* Calculates indicators
* Evaluates strategy conditions
* Executes simulated trades
* Tracks portfolio performance

### 4. Generate Results

Example output:

```text
Strategy: sma-crossover.qdsl

Initial Capital: $10,000
Final Capital:   $16,842

Total Return:    68.42%
Trades:          24
Win Rate:        62.5%
Max Drawdown:    -12.3%
Sharpe Ratio:    1.41
```

## Project Goals

This project combines concepts from:

* Functional Programming
* Programming Language Design
* Parsing and Interpreters
* Software Engineering
* Quantitative Finance

The aim is to explore how a specialised language can be used to express trading strategies while learning about language implementation and financial modelling.