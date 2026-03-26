# AI Coding Principles

A collection of Claude Code skills for coding discipline and system design knowledge.

[中文文档](./README.zh-CN.md)

## Skills

### [ai-coding-discipline](./ai-coding-discipline/SKILL.md)

Mandatory rules loaded during all code writing tasks that prevent common AI coding anti-patterns.

| # | Rule | Summary |
|---|------|---------|
| 1 | No Silent Fallbacks | Don't use `??` / `||` to mask values that should never be missing |
| 2 | No Catch-All try/catch | Business logic lets errors propagate; catch only at API boundaries |
| 3 | Tests Must Fail When Code Breaks | Verify specific outcomes, not just existence |
| 4 | No Hardcoded Lookup Tables | Implement real logic, not test-case-fitting shims |
| 5 | Red-Green Testing (TDD) | Write failing test first, then fix |
| 6 | Don't Remove Debug Logs During Fix | Logs stay until human confirms the fix works |

### [ddia-principles](./ddia-principles/SKILL.md)

Distilled reference guide based on Martin Kleppmann's *Designing Data-Intensive Applications*. Loaded when designing database schemas, choosing storage engines, implementing replication/partitioning, handling distributed transactions, or building batch/stream processing pipelines.

| Part | Topics |
|------|--------|
| I: Foundations | Reliability, Scalability, Maintainability; Data Models & Query Languages; Storage & Retrieval (B-tree vs LSM-tree, OLTP vs OLAP); Encoding & Evolution |
| II: Distributed Data | Replication (single/multi-leader, leaderless); Partitioning (key-range, hash, compound); Transactions & Isolation Levels; Distributed System Challenges; Consistency & Consensus |
| III: Derived Data | Batch Processing (MapReduce, Spark, Flink); Stream Processing (Kafka, CDC, Event Sourcing); Data Integration Patterns |

## Installation

```bash
npx skills add luoling8192/ai-coding-principles
```

## License

[MIT](./LICENSE)
