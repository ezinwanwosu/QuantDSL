# QuantDSL Language Specification (v0.1)

## Overview

QuantDSL is a domain-specific language for expressing quantitative trading strategies.

A strategy consists of one or more trading rules that define actions and the conditions under which those actions should occur.

---

# Keywords

The following keywords are reserved:

```text
BUY
SELL
WHEN
AND
OR
```

Keywords are case-sensitive.

---

# Trading Actions

A trading action specifies whether an asset should be bought or sold.

## Syntax

```text
BUY <SYMBOL>

SELL <SYMBOL>
```

## Examples

```text
BUY AAPL

SELL MSFT
```

---

# Conditions

Conditions determine when a trading action should be executed.

## Syntax

```text
WHEN <expression>
```

## Example

```text
WHEN SMA(20) > SMA(50)
```

---

# Indicators

## SMA

Simple Moving Average.

### Syntax

```text
SMA(<period>)
```

### Example

```text
SMA(20)
```

---

## EMA

Exponential Moving Average.

### Syntax

```text
EMA(<period>)
```

### Example

```text
EMA(50)
```

---

## RSI

Relative Strength Index.

### Syntax

```text
RSI
```

### Example

```text
RSI > 70
```

---

# Comparison Operators

Supported comparison operators:

```text
>
<
>=
<=
==
```

## Examples

```text
SMA(20) > SMA(50)

RSI < 30
```

---

# Logical Operators

Multiple conditions may be combined.

## Syntax

```text
<condition> AND <condition>

<condition> OR <condition>
```

## Example

```text
SMA(20) > SMA(50)
AND RSI < 70
```

---

# Example Program

```text
BUY AAPL
WHEN SMA(20) > SMA(50)

SELL AAPL
WHEN RSI > 70
```

---

# Execution Model

1. Load historical market data.
2. Calculate required indicators.
3. Evaluate strategy conditions.
4. Execute simulated trades.
5. Record portfolio performance.
6. Generate performance metrics.

---

# Future Extensions

Potential future features include:

* Stop losses
* Take profits
* Multiple assets
* Portfolio management
* Additional indicators