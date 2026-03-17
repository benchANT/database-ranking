# Tuning Details

This document describes the tuning parameters applied to the DBMS and cloud infrastructure configuration for this evaluation scenario.
For the vanilla (baseline) configuration, refer to the [Time Series: DevOps Ranking README](../../README.md).

## DBMS Server Tuning

| Parameter | Tuned Value |
|-----------|-------------|
| `configNodeConsensusProtocolClass` | `SimpleConsensus` |
| `dataRegionConsensusProtocolClass` | `SimpleConsensus` |
| `dataRegionGroupExtensionPolicy` | `CUSTOM` |
| `defaultDataRegionGroupNumPerDatabase` | `1` |
| `degreeOfQueryParallelism` | `1` |
| `dnMetricLevel` | `OFF` |
| `enableAutoRepairCompaction` | `false` |
| `enableCrossSpaceCompaction` | `false` |
| `enableLastCache` | `false` |
| `enableSeqSpaceCompaction` | `false` |
| `enableUnseqSpaceCompaction` | `false` |
| `heapNewsizeConfig` | `1G` |
| `heapNewsizeData` | `2G` |
| `iotdbJmxOpts` | `UseParallelGC` |
| `maxHeapSizeConfig` | `1G` |
| `maxHeapSizeData` | `12G` |
| `maxNumberOfPointsInPage` | `360` |
| `maxTsblockLineNumber` | `360` |
| `maxWalNodesNum` | `9` |
| `schemaRegionConsensusProtocolClass` | `SimpleConsensus` |
| `walAsyncModeFsyncDelayInMs` | `3000` |
| `walBufferQueueCapacity` | `5000` |
| `walMode` | `ASYNC` |

## DBMS Client Tuning

| Parameter | Tuned Value |
|-----------|-------------|
| `useGroupBy` | `true` |
| `channelCapacity` | `50` |
| `alignedTimeSeries` | `false` |
| `tabletSize` | `5000` |
| `flowControl` | `false` |
| `sessionPoolSize` | `40` |
| `warmupPhases` | `4` |

## Benchmark Tuning

| Parameter | Tuned Value |
|-----------|-------------|
| `hashWorkers` | `true` |
