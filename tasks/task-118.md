# Lesson 118: Project 3 Part C: Benchmarking and Optimization

## Section 21: Capstone Projects

## Status: pending

## Prerequisites
- Lesson 117 (Capstone Project 3 - Completion and Polish)
- Lessons 094/095 (Benchmarking - criterion, profiling, flamegraphs)

## Added
- Split from lesson 118 (v7 pacing review)

## Objectives
- [ ] Set up `criterion` benchmarks for all performance-critical operations in your capstone 3 project, establishing a baseline for optimization
- [ ] Benchmark at least 3 operations at different input sizes (small, medium, large) and compare at least one against a standard library equivalent
- [ ] Profile the project using `cargo flamegraph` or `perf` to identify hot paths and bottlenecks
- [ ] Apply at least one targeted optimization based on profiling results (e.g., reducing allocations, improving cache locality, avoiding unnecessary clones)
- [ ] Re-benchmark after optimization and document before/after measurements

## Exercises
- [ ] **Exercise 1 -- Criterion benchmarks**: Add `criterion` benchmarks for your project: benchmark at least 3 operations at different input sizes (small, medium, large). For the executor: benchmark task throughput. For the parser: benchmark parsing speed on varying expression complexity. For the B-tree: benchmark insert/get/remove at different tree sizes. Compare at least one operation against a standard library equivalent (e.g., `BTreeMap` vs your B-tree, `std` parser vs yours).
- [ ] **Exercise 2 -- Flamegraph and optimization**: Generate a flamegraph of a realistic workload using `cargo flamegraph` (requires `perf` on Linux or `dtrace` on macOS). Identify the top 3 hottest functions. Implement at least one optimization targeting a hot path (e.g., reducing allocations, caching results, replacing `clone()` with references, using `Vec::with_capacity`). Re-run benchmarks and document: what you changed, why, and the before/after measurements.

## Notes

> **Benchmark comparison targets by option:**
> - Option A (executor): Compare your `spawn` + `block_on` throughput against `tokio::spawn`
> - Option B (parser): Compare your parser against the `nom` crate on the same input
> - Option C (data structure): Compare your implementation against `std::collections::BTreeMap` (or `BinaryHeap`)

_Lesson not yet started._
_Split from original lesson 118 which was assessed as >2 hrs because benchmarking, profiling, and unsafe auditing are each time-consuming activities._
_This part focuses exclusively on performance: establishing benchmarks, profiling, optimizing, and measuring improvement._
_`cargo flamegraph` depends on platform tooling (Linux `perf`, macOS `dtrace`). If unavailable, use criterion benchmarks and platform-native profilers as a fallback._

> **Profiling setup by platform:**
> - **Linux**: install `perf` (for example: `sudo apt install linux-tools-generic linux-tools-$(uname -r)`), then install flamegraph tool: `cargo install flamegraph`
> - **macOS**: install flamegraph tool (`cargo install flamegraph`) and use `dtrace`/Instruments (may require elevated permissions; SIP can limit some traces)
> - **Windows**: `cargo flamegraph` is typically done via WSL/Linux VM; native fallback is criterion + Windows profilers (WPA/Visual Studio)
> - If changing `kernel.perf_event_paranoid` is not allowed in your environment, continue with criterion-only measurements and document the limitation.
