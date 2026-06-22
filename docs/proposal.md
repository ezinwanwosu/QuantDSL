# QuantDSL Project Proposal

## Overview

QuantDSL is a domain-specific language (DSL) written in Haskell for defining and evaluating quantitative trading strategies. The language aims to provide a concise, human-readable way to express trading rules while exploring concepts from functional programming, language design, and quantitative finance.

The project will include a parser, abstract syntax tree (AST), interpreter, and backtesting engine capable of evaluating strategies against historical market data.

---

## Motivation

This project was created to combine several areas of computer science that I am interested in:

* Functional Programming
* Programming Language Design
* Quantitative Finance
* Software Engineering

Many quantitative trading platforms require strategies to be written in general-purpose programming languages. QuantDSL explores how a specialised language can be designed to make strategy development more intuitive while also serving as a vehicle for learning about parsers, interpreters, and language implementation.

---

## Example Strategy

The language should allow strategies to be expressed in a readable format:

```text
BUY AAPL
WHEN SMA(20) > SMA(50)

SELL AAPL
WHEN RSI > 70
```

Rather than writing implementation details, users focus on the trading logic itself.

---

## Objectives

The primary objectives of this project are:

1. Design a custom domain-specific language for trading strategies.
2. Implement a parser in Haskell.
3. Build an Abstract Syntax Tree (AST) representation.
4. Develop an interpreter capable of evaluating trading rules.
5. Implement a backtesting engine using historical market data.
6. Generate performance metrics for evaluated strategies.
7. Document the entire design and development process.

---

## Scope

### Included in Version 1

* Buy and sell rules
* Technical indicators (SMA, EMA, RSI)
* Conditional expressions
* Parsing and syntax validation
* Historical backtesting
* Basic performance metrics

### Not Included in Version 1

* Live trading
* Broker integration
* Machine learning models
* Derivatives pricing
* High-frequency trading
* Portfolio optimisation

The goal of Version 1 is to create a complete and well-documented language and execution pipeline rather than a production trading system.

---

## Technical Challenges

The project will explore several computer science concepts:

* Lexical analysis
* Parsing
* Abstract Syntax Trees
* Functional program design
* State modelling
* Data processing
* Financial modelling

---

## Expected Outcomes

By the completion of the project I expect to have:

* A functioning DSL implementation
* A backtesting engine
* Example trading strategies
* Technical documentation
* Development logs documenting decisions and lessons learned

The final result should demonstrate the application of functional programming techniques to a real-world problem domain while providing practical experience in language implementation.