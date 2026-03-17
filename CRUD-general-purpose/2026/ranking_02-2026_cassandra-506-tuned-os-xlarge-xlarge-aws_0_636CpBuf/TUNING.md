# Tuning Details

This document describes the tuning parameters applied to the DBMS and cloud infrastructure configuration for this evaluation scenario.
For the vanilla (baseline) configuration, refer to the [CRUD General Purpose Ranking README](../../../README.md).

## DBMS Tuning

| Parameter            | Vanilla Value     | Tuned Value               |
|----------------------|-------------------|---------------------------|
| Compaction Strategy  | STCS              | UnifiedCompactionStrategy |
| SSTable Format       | big               | bti                       |
| Memtable             | default           | TrieMemtable              |
| Java Version         | 11                | 17                        |
| Garbage Collector    | G1GC              | ZGC                       |


