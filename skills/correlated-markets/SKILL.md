---
name: correlated-markets
title: Correlated Markets
description: Find inconsistencies and dependency relationships across related sports prediction markets.
version: 1.0.0
category: sports-prediction-markets
---

# Correlated Markets

## Purpose

Find logical inconsistencies between related prediction markets.

## Dependency Analysis

Build relationships such as:

```text
Win Championship
        ↓ requires
Win Conference
        ↓ often requires
Make Playoffs
```

Use conditional probability.

Example:

```text
P(Championship)
=
P(Make Playoffs)
× P(Win Conference | Playoffs)
× P(Win Championship | Conference Winner)
```

## Search For Contradictions

Compare:

- playoff qualification
- division winner
- conference winner
- championship winner
- season wins
- player awards
- head-to-head markets

If one event logically requires another:

```text
P(child event) ≤ P(required parent event)
```

subject to exact settlement rules.

## Mutually Exclusive Markets

If exactly one of several outcomes can occur:

```text
P(A) + P(B) + P(C) + ... ≈ 100%
```

Investigate material deviations.

Possible explanations:

- bid/ask spread
- transaction costs
- stale markets
- poor liquidity
- inconsistent beliefs
- settlement differences

## Arbitrage Discipline

Never call something arbitrage until verifying:

- all legs are executable
- sufficient liquidity exists
- settlement definitions align
- transaction costs are included
- no hidden conditional rule breaks the relationship
