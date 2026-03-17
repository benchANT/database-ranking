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
| `dnMetricLevel` | `DO_NOTHING` |
| `enableLastCache` | `false` |
| `heapNewsizeConfig` | `1G` |
| `heapNewsizeData` | `12G` |
| `iotdbJmxOpts` | `UseParallelGC` |
| `maxDirectMemorySizeConfig` | `1G` |
| `maxDirectMemorySizeData` | `2G` |
| `maxHeapSizeConfig` | `1G` |
| `maxHeapSizeData` | `12G` |
| `maxInnerCompactionCandidateFileNum` | `2` |
| `maxNumberOfPointsInPage` | `1080` |
| `maxWalNodesNum` | `9` |
| `minCrossCompactionUnseqFileLevel` | `0` |
| `schemaRegionConsensusProtocolClass` | `SimpleConsensus` |
| `timePartitionInterval` | `60480000000` |
| `walAsyncModeFsyncDelayInMs` | `3000` |
| `walBufferQueueCapacity` | `5000` |
| `walMode` | `ASYNC` |

## DBMS Client Tuning

| Parameter | Tuned Value |
|-----------|-------------|
| `compactionGracePeriod` | `300` |
| `useGroupBy` | `true` |


