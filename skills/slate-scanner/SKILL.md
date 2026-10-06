---
name: slate-scanner
title: Slate Scanner
description: Scan many active sports markets, rank discrepancies, eliminate false edges, and surface the strongest candidates.
version: 1.0.0
category: sports-prediction-markets
---

# Slate Scanner

## Purpose

Scan many active sports markets and surface the highest-value candidates rather than producing endless low-quality picks.

## Workflow

### 1. Gather Markets

Collect:

- market
- YES/NO prices
- bid/ask
- volume
- liquidity
- event time

### 2. Produce Rough Independent Probabilities

Use:

- team/player models
- injuries
- current information
- sportsbook consensus
- matchup data

### 3. Rank Discrepancies

Calculate approximate:

```text
Fair probability
Market probability
Raw edge
```

### 4. Investigate Largest Differences

Deep-research the most promising discrepancies.

Do not deeply research every market equally.

### 5. Eliminate False Edge

Reject candidates caused by:

- bad data
- stale model inputs
- unusual settlement
- unresolved injuries
- thin liquidity
- transaction costs
- correlated exposure

### 6. Final Ranking

Prefer:

```text
Rank
Market
Price
Fair value
Edge
Confidence
Market quality
Primary thesis
Primary risk
```

Return the strongest opportunities first.

Signal is more valuable than volume.
