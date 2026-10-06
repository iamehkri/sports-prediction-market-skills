---
name: market-analysis
title: Market Analysis
description: Analyze pregame, futures, playoff, championship, award, and other sports prediction markets to estimate fair probability and edge.
version: 1.0.0
category: sports-prediction-markets
---

# Market Analysis

## Purpose

Analyze a sports prediction market before an event or when the event state itself is not the primary variable.

## Use When

Use this skill for:

- game winner markets
- series markets
- tournament markets
- season markets
- playoff markets
- championship markets
- player awards
- qualification markets
- sports-related event contracts

## Workflow

### 1. Understand the Contract

Determine:

- exact question
- resolution criteria
- event date
- deadline
- overtime rules
- cancellation rules
- official settlement source

Flag ambiguity before relying on normal sports assumptions.

### 2. Capture Current Market

Collect when available:

```text
YES bid
YES ask
NO bid
NO ask
last trade
volume
liquidity
timestamp
```

Use executable prices when evaluating edge.

### 3. Establish Baseline Strength

Use sport-appropriate metrics.

Examples:

NFL:
- EPA/play
- success rate
- quarterback efficiency
- pressure rate
- explosive-play rate

NBA:
- offensive rating
- defensive rating
- net rating
- pace
- lineup performance

MLB:
- starting pitcher projection
- bullpen availability
- wRC+
- platoon splits
- park factors

NHL:
- expected goals
- high-danger chances
- goalie quality
- special teams

Soccer:
- xG
- xGA
- shot quality
- field tilt
- set pieces

### 4. Adjust for Context

Evaluate:

- injuries
- suspensions
- starters
- expected rotation
- rest
- travel
- home advantage
- weather
- tactical matchup
- motivation when measurably relevant

### 5. Establish Independent Probability

Generate:

```text
Base probability:
Context-adjusted probability:
Market-informed probability:
Final fair range:
Central estimate:
```

Do not blindly average models when they materially disagree.

Investigate why.

### 6. Compare Against Market

Calculate:

```text
Edge = Fair Probability - Executable Probability
```

Classify:

```text
<2 points     insignificant
2–4 points   weak
4–7 points   interesting
7–10 points  strong
10+ points   investigate aggressively
```

Large apparent edges require additional skepticism.

### 7. Attack the Thesis

Ask:

- Are we missing an injury?
- Did another market already move?
- Is liquidity poor?
- Are settlement rules unusual?
- Does our model rely on stale information?
- Is an important player status unresolved?

### 8. Output

Return:

```text
MARKET
CURRENT PRICE
FAIR VALUE
FAIR RANGE
EDGE
CONFIDENCE

THESIS

SUPPORTING EVIDENCE

RISKS

UPCOMING CATALYSTS

VERDICT
```

Possible verdicts:

```text
NO EDGE
WATCH
LEAN YES
LEAN NO
STRONG YES DISCREPANCY
STRONG NO DISCREPANCY
```

The verdict describes market discrepancy, not certainty.
