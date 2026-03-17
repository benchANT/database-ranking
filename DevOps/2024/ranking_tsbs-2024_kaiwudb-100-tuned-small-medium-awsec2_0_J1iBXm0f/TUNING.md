# Tuning Details

This document describes the tuning parameters applied to the DBMS and cloud infrastructure configuration for this evaluation scenario.
For the vanilla (baseline) configuration, refer to the [Time Series: DevOps Ranking README](../../README.md).

## DBMS Client Tuning

| Parameter | Tuned Value |
|-----------|-------------|
| `queryMode` | `PREPARED` |
| `warmupPhases` | `2` |

## Benchmark Tuning

| Parameter | Tuned Value |
|-----------|-------------|
| `hashWorkers` | `true` |
