---
name: calibration-postmortem
title: Calibration and Postmortem
description: Track forecast quality over time using calibration, Brier score, log loss, closing-market movement, and postmortems.
version: 1.0.0
category: sports-prediction-markets
---

# Calibration and Postmortem

## Purpose

Measure whether forecasts are actually good over time.

## Record Every Forecast

Store:

```text
market
timestamp
market price
fair probability
fair range
confidence
thesis
information used
eventual closing price
outcome
```

Do not overwrite the original forecast.

## Calibration

Group forecasts into probability buckets:

```text
50–55
55–60
60–65
65–70
70–80
80–90
90+
```

Compare predicted probability with actual frequency.

Example:

If 100 forecasts were approximately 70%, roughly 70 should eventually occur.

## Metrics

Track:

- Brier score
- log loss
- calibration error
- mean absolute probability error
- closing-line movement
- average estimated edge
- actual results

## Closing-Price Analysis

Example:

```text
Original market:
53%

Our fair estimate:
61%

Closing market:
62%
```

The outcome may still lose.

The movement toward the forecast nevertheless provides evidence that the original price may have been inefficient.

Do not confuse outcome variance with forecasting quality.

## Postmortem Questions

After resolution ask:

1. Was the probability reasonable?
2. Was information missing?
3. Did the market eventually move toward the forecast?
4. Did unexpected information appear?
5. Was the model overconfident?
6. Was a variable incorrectly weighted?
7. Was the process correct despite the outcome?
8. Should the model change?

## Rule

Never alter old forecasts to make historical performance look better.
