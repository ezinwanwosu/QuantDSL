# QuantDSL

> A Haskell-based domain-specific language (DSL) for expressing and backtesting quantitative trading strategies.

⚠️ **Project Status: Early Development**

QuantDSL is currently in the design and planning stage. The language specification, architecture, and project documentation are being developed before implementation begins.

The goal of this project is to explore the intersection of:

* Functional Programming
* Programming Language Design
* Quantitative Finance
* Software Engineering

---

## Overview

QuantDSL is a custom domain-specific language designed to express trading strategies in a concise and human-readable format.

Instead of implementing strategies directly in a general-purpose programming language, users define trading rules using a dedicated syntax focused on financial concepts.

Example:

```text
BUY AAPL
WHEN SMA(20) > SMA(50)

SELL AAPL
WHEN RSI > 70
```

The long-term vision is to allow strategies to be parsed, interpreted, and evaluated against historical market data through a backtesting engine.

---

## Project Goals

The primary goals of this project are:

* Design a custom trading strategy language
* Implement a parser and interpreter in Haskell
* Explore Abstract Syntax Trees (ASTs)
* Learn practical language implementation techniques
* Build a historical backtesting engine
* Generate performance metrics and reports
* Document the entire development process

---

## Planned Features

### Language Features

* Buy and sell actions
* Conditional expressions
* Logical operators (`AND`, `OR`)
* Technical indicators
* Custom strategy definitions

### Supported Indicators (Planned)

* Simple Moving Average (SMA)
* Exponential Moving Average (EMA)
* Relative Strength Index (RSI)

### Backtesting Features

* Historical market data analysis
* Simulated trade execution
* Portfolio tracking
* Performance evaluation

### Reporting

* Total return
* Win rate
* Maximum drawdown
* Sharpe ratio
* Trade history

---

## Current Development Roadmap

### Phase 1 — Research & Design

- [x] Repository creation
- [x] Project proposal
- [x] Development journal
- [ ] Quantitative finance research
- [ ] Language specification
- [ ] System architecture design

### Phase 2 — Language Implementation

- [ ] Define grammar
- [ ] Build parser
- [ ] Construct AST
- [ ] Implement interpreter
- [ ] Add error handling

### Phase 3 — Backtesting Engine

- [ ] Historical data processing
- [ ] Indicator calculations
- [ ] Trade execution simulation
- [ ] Portfolio management

### Phase 4 — Reporting & Analysis

- [ ] Performance metrics
- [ ] Strategy evaluation
- [ ] Visualisations
- [ ] Final documentation

---

## Project Structure

```text
QuantDSL/
│
├── README.md
│
├── docs/
│   ├── proposal.md
│   ├── language-spec.md
│   ├── architecture.md
│   └── dev-log/
│
├── examples/
│
├── src/
│
└── tests/
```

---

## Example Workflow

The planned execution pipeline is:

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

---

## Why Haskell?

This project is being implemented in Haskell because it provides excellent support for:

* Algebraic Data Types
* Pattern Matching
* Functional Design
* Parser Combinators
* Type Safety

These features make Haskell particularly well-suited for implementing programming languages and interpreters.

---

## Documentation

This repository will document the entire development process, including:

* Design decisions
* Research notes
* Architecture discussions
* Development logs
* Lessons learned

The intention is to treat the project as both a software engineering exercise and a learning journey.

---

## Current Status

QuantDSL is under active development.

The current focus is on defining the language, researching quantitative trading concepts, and designing the architecture before implementation begins.

Implementation updates will be added as development progresses.

---

## License

This project is released under the MIT License.