# Sports Prediction Market Skills

A modular skills repository for a sports prediction-market analyst.

The permanent agent identity and non-negotiable behavior live in `SOUL.md`.
Task-specific workflows live under `skills/<skill-name>/SKILL.md`.

## Repository structure

```text
sports-prediction-market-skills/
├── SOUL.md
├── README.md
├── skills.json
└── skills/
    ├── market-analysis/
    │   └── SKILL.md
    ├── live-event-analysis/
    │   └── SKILL.md
    ├── pricing-edge/
    │   └── SKILL.md
    ├── sportsbook-intelligence/
    │   └── SKILL.md
    ├── news-and-research/
    │   └── SKILL.md
    ├── correlated-markets/
    │   └── SKILL.md
    ├── slate-scanner/
    │   └── SKILL.md
    ├── calibration-postmortem/
    │   └── SKILL.md
    └── risk-and-exposure/
        └── SKILL.md
```

## Loading model

Always load:

```text
SOUL.md
```

Then load only the skill or skills required for the current task.

Examples:

### Pregame market analysis

```text
SOUL.md
skills/market-analysis/SKILL.md
skills/pricing-edge/SKILL.md
skills/sportsbook-intelligence/SKILL.md
skills/news-and-research/SKILL.md
```

### Live game

```text
SOUL.md
skills/live-event-analysis/SKILL.md
skills/pricing-edge/SKILL.md
skills/news-and-research/SKILL.md
skills/sportsbook-intelligence/SKILL.md
```

### Scan an entire slate

```text
SOUL.md
skills/slate-scanner/SKILL.md
skills/market-analysis/SKILL.md
skills/pricing-edge/SKILL.md
skills/news-and-research/SKILL.md
skills/sportsbook-intelligence/SKILL.md
```

### Cross-market inconsistency

```text
SOUL.md
skills/correlated-markets/SKILL.md
skills/pricing-edge/SKILL.md
```

## Skill discovery

`skills.json` provides a machine-readable registry containing each skill's path,
description, and common triggers.

An agent can:

1. Read `SOUL.md` at startup.
2. Read `skills.json`.
3. Match the user task to one or more skill triggers.
4. Load the matching `SKILL.md` files.
5. Execute the workflow without loading unrelated skills.

## Live-data requirement

This repository defines analytical behavior but does not itself provide live data.

For live analysis, the host agent should have access to reliable sources for:

- live scores and play-by-play
- sportsbook or exchange prices
- prediction-market prices and order books
- injuries and starting lineups
- weather where relevant
- official league/team announcements

The agent must never invent live state or current prices when a live source is unavailable.

## Import

You can import the whole repository into any agent framework that supports file-based context or skills.

If the framework expects a conventional skill file named `SKILL.md`, each skill is already structured that way.

If the framework uses a registry, point it at `skills.json`.

If the framework loads a persistent system/context file, use `SOUL.md` for that layer.
