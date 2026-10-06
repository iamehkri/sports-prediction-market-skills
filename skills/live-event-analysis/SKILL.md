---
name: live-event-analysis
title: Live Event Analysis
description: Analyze sports prediction markets while an event is actively happening using verified live game state and rapidly updating probabilities.
version: 1.0.0
category: sports-prediction-markets
---

# Live Event Analysis

## Purpose

Analyze sporting events and prediction markets **while the event is actively occurring**.

Live analysis should continuously update fair probability as the event state changes.

## Core Principle

The correct probability is conditional on the current state.

```text
P(outcome | current game state)
```

Pregame probability becomes only a prior.

## Required Live State

Collect as much as available:

```text
sport
teams / players
score
period / quarter / inning
clock
possession
field position
timeouts
down and distance
outs
bases occupied
foul situation
cards
serve
recent substitutions
injuries
weather
current market prices
timestamp
```

Only use fields relevant to the sport.

## Step 1 — Verify State

Never assume the event state.

Confirm using the freshest reliable feed available.

Record:

```text
LIVE STATE VERIFIED:
timestamp
```

## Step 2 — Establish Prior

Determine the approximate probability immediately before the current state.

This may come from:

- pregame model
- previous live estimate
- efficient sportsbook market
- previous prediction-market state

## Step 3 — Update Using Game State

Evaluate how the new state changes expected outcome.

Examples:

NFL:
- score differential
- possession
- field position
- clock
- timeouts
- down/distance
- quarterback availability

NBA:
- score differential
- clock
- possession
- foul trouble
- lineup
- pace
- timeout situation

MLB:
- inning
- score
- outs
- runners
- current pitcher
- bullpen availability
- batting order position

NHL:
- score
- time remaining
- power play
- goalie status
- expected-goal flow

Soccer:
- score
- minute
- red cards
- substitutions
- xG
- tactical state
- stoppage expectations

Tennis:
- set score
- game score
- serve
- break state
- injury signals

## Step 4 — Identify Material Events

Do not overreact to noise.

Material events include things like:

- scoring
- turnovers
- red cards
- injuries
- pitcher changes
- major substitutions
- foul-outs
- break of serve
- weather disruption

Recalculate after material events.

## Step 5 — Compare With Live Market

Capture:

```text
Prediction market bid/ask:
Sportsbook live probability:
Updated model probability:
```

Determine whether one market reacted faster than another.

## Step 6 — Detect Stale Markets

Potential stale-market indicators:

- sportsbook moved but prediction market did not
- major event occurred but quote remains unchanged
- injury confirmed but market has not repriced
- game resumed after suspension with outdated orders
- thin order book reflects old state

Be alert to data latency.

A quote that appears attractive may simply be stale and unexecutable.

## Step 7 — Live Output

Use:

```text
LIVE STATE
Team A 24
Team B 20
Q4 — 6:14
Team B ball

LAST MATERIAL EVENT
...

CURRENT MARKET
YES 46–49¢

UPDATED FAIR VALUE
55%

FAIR RANGE
52–58%

LIVE EDGE
+6 points at 49¢

CONFIDENCE
Medium

WHY IT CHANGED
...

NEXT HIGH-IMPACT STATE
...
```

## Rule

Never pretend to have live information that has not actually been retrieved or verified.
