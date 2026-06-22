# Day 1 Development Log: Defining the Scope

**Date:** 2026-06-22

## Goals

Today's goal was to define the overall direction and scope of the project before beginning implementation.

Rather than immediately writing code, I wanted to understand:

* What problem the language solves
* Who the intended user is
* What features should be included
* What features should be intentionally excluded

This would help prevent scope creep and provide a clear roadmap for future development.

---

## Project Definition

The project will be a Haskell-based domain-specific language called **QuantDSL**.

The language will allow users to express trading strategies using a simple syntax rather than writing a full program.

Example:

```text
BUY AAPL
WHEN SMA(20) > SMA(50)
```

The strategy will be parsed, converted into an internal representation, and eventually evaluated against historical market data.

---

## Initial Research

I spent time thinking about how quantitative strategies are commonly expressed.

Most strategies consist of:

* An action (buy or sell)
* A condition
* Market indicators
* Risk management rules

This observation suggests that the language grammar can be kept relatively small while still supporting useful strategies.

---

## Key Decisions

### Use Haskell

I chose Haskell because the project naturally aligns with:

* Algebraic data types
* Pattern matching
* Parser combinators
* Functional design principles

The project also provides an opportunity to improve my Haskell skills through a larger practical application.

### Focus on Language Design First

The first milestone will be language design rather than market simulation.

The language itself is the core of the project, so understanding the syntax and semantics is more important than immediately implementing trading functionality.

### Prioritise Documentation

I want this project to demonstrate not only technical implementation but also engineering process.

Development logs and design documents will be maintained throughout the project to record decisions, challenges, and lessons learned.

---

## Challenges

One challenge is balancing simplicity with expressiveness.

A language that is too simple may not support interesting strategies, while a language that is too complex could become difficult to implement and maintain.

This trade-off will likely influence many future design decisions.

---

## Lessons Learned

Before writing code, it is important to clearly define:

* Project objectives
* Scope
* Constraints
* Success criteria

Investing time in planning should reduce rework later in the project.

---

## What Problem Does the Language Solve?

Quantitative trading strategies are often implemented directly in general-purpose programming languages such as Python. While powerful, these languages require users to focus on programming details rather than the trading logic itself.

QuantDSL aims to provide a simple, human-readable way to express trading strategies. Instead of writing code to calculate indicators, manage conditions, and execute trades, users can describe their strategy using a specialised language focused solely on trading concepts.

For example:

```text
BUY AAPL
WHEN SMA(20) > SMA(50)

SELL AAPL
WHEN RSI > 70
```

The goal is to separate **what the strategy does** from **how it is executed**.

---

## Who Is the Intended User?

The primary user is:

* Students interested in quantitative finance
* Developers learning functional programming
* Developers interested in programming language design
* Hobbyist traders who want to experiment with systematic strategies

The project is primarily educational rather than commercial. The intended user is someone who wants to define and test trading strategies without building an entire trading system from scratch.

---

## What Features Should Be Included?

### Core Language Features

* BUY and SELL actions
* Trading symbols (e.g. AAPL, MSFT)
* Conditional expressions
* Comparison operators (`>`, `<`, `>=`, `<=`, `==`)
* Logical operators (`AND`, `OR`)

### Technical Indicators

* Simple Moving Average (SMA)
* Exponential Moving Average (EMA)
* Relative Strength Index (RSI)

### Language Infrastructure

* Lexer
* Parser
* Abstract Syntax Tree (AST)
* Interpreter

### Backtesting Features

* Historical market data processing
* Simulated trade execution
* Portfolio tracking
* Performance metrics

### Reporting

* Total return
* Number of trades
* Win rate
* Maximum drawdown
* Sharpe ratio

---

## What Features Should Be Intentionally Excluded?

To keep the project focused and achievable, the following features are out of scope for Version 1:

### Trading Infrastructure

* Live trading
* Broker integrations
* Order routing
* Real-time market data

### Advanced Quantitative Features

* Machine learning models
* Portfolio optimisation
* Options and derivatives pricing
* Statistical arbitrage systems

### Enterprise Features

* User accounts
* Web applications
* Cloud deployment
* Multi-user support

### High-Frequency Trading

* Tick-level processing
* Low-latency execution
* Market microstructure modelling

The purpose of QuantDSL is to explore language design, functional programming, and backtesting rather than to build a production trading platform.

---

## Next Steps

Tomorrow's goals are:

1. Research common quantitative indicators.
2. Study how trading strategies are typically structured.
3. Begin designing example QuantDSL programs.
4. Identify the minimum feature set required for Version 1.

---

## Current Status

* Repository created ✅
* Project proposal written ✅
* Initial scope defined ✅
* Development journal started ✅
* Ready to begin domain research ✅