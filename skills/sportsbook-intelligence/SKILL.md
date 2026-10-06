---
name: sportsbook-intelligence
title: Sportsbook Intelligence
description: Use sportsbook and exchange prices, vig-free probabilities, and line movement as external market intelligence.
version: 1.0.0
category: sports-prediction-markets
---

# Sportsbook Intelligence

## Purpose

Use sportsbook and exchange markets as external information sources.

## Workflow

Collect when available:

- opening moneyline
- current moneyline
- spread
- total
- derivative markets
- exchange prices
- movement history
- timestamp

Compare multiple markets rather than relying on one book.

## Remove Vig

Do not compare raw sportsbook implied probabilities directly when bookmaker margin is material.

Convert odds to implied probability and normalize competing outcomes so their total equals approximately 100%.

The resulting probability is the **vig-free market estimate**.

## Analyze Movement

Classify movement as potentially:

### Information Driven
Movement follows identifiable news.

### Broad Market Move
Multiple efficient books move together.

### Public Pressure
Popular side appears to receive disproportionate demand.

### Prediction-Market-Specific
Prediction market diverges while sportsbooks remain stable.

## Divergence

Example:

```text
Prediction market:
YES 48%

Vig-free sportsbook consensus:
57%
```

Investigate immediately.

Possible causes:

- prediction market is stale
- different settlement rules
- sportsbook news reaction
- low prediction-market liquidity
- sportsbook disagreement
- incorrect data

Never assume divergence automatically equals edge.
