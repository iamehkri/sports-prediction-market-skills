---
name: pricing-edge
title: Pricing and Edge
description: Convert market prices and fair probabilities into edge, expected value, net edge, and market-quality assessments.
version: 1.0.0
category: sports-prediction-markets
---

# Pricing and Edge

## Purpose

Convert probabilities and market prices into fair value, edge, expected value, and market-quality assessments.

## Binary Contract

For a contract paying $1 if YES occurs:

```text
Market probability ≈ contract price
```

Example:

```text
YES = 0.58
Implied probability ≈ 58%
```

Use actual executable ask when evaluating buying YES.

## Edge

```text
Edge = Fair Probability - Purchase Price
```

Example:

```text
Fair probability = 0.67
YES ask = 0.58

Edge = 0.09
```

Report:

```text
+9 percentage points
```

## Expected Value

For one YES contract paying $1:

```text
EV = Fair Probability - Contract Cost
```

Example:

```text
0.67 - 0.58 = $0.09 EV per contract
```

Expected return on capital:

```text
EV ROI = EV / Contract Cost
```

Example:

```text
0.09 / 0.58 = 15.5%
```

This is model-based expected value.

It is not guaranteed return.

## NO Contracts

For a mutually exclusive binary market:

```text
Fair NO probability = 1 - Fair YES probability
```

Evaluate NO against its own executable price.

Do not assume quoted YES and NO prices sum perfectly to $1 because:

- spread
- fees
- liquidity
- platform design

may prevent this.

## Market Quality

Classify:

### High Quality
- tight spreads
- strong volume
- deep order book
- active price discovery

### Medium Quality
- moderate liquidity
- manageable spread

### Low Quality
- thin order book
- wide spread
- stale trades
- unstable quotes

Reduce confidence in apparent edge as market quality declines.

## Transaction Costs

Consider:

- fees
- spread
- slippage
- fill probability

Edge must survive transaction costs.

## Fair-Value Output

```text
MARKET ASK
58¢

FAIR VALUE
67¢

RAW EDGE
+9 points

FEES / FRICTION
...

NET ESTIMATED EDGE
...

MODEL EV
...

MARKET QUALITY
...
```
