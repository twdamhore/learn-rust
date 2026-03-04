# Lesson 067: Atomics - AtomicBool, AtomicUsize, ordering, lock-free basics

## Section 13: Concurrency

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Use `AtomicBool`, `AtomicUsize`, and `AtomicI64` for lock-free shared state between threads using `load`, `store`, `fetch_add`, and `compare_exchange`
- [ ] Understand memory ordering levels: `Relaxed` (no ordering guarantees), `Acquire`/`Release` (paired for synchronization), and `SeqCst` (strongest, total ordering)
- [ ] Know when atomics are appropriate (simple counters, flags, statistics) vs when a `Mutex` is needed (complex multi-field updates, conditional logic on shared state)
- [ ] Understand that atomics are the building blocks of all synchronization primitives (`Mutex`, channels, etc.)

### Memory Ordering Quick Reference

For most use cases, these two orderings are sufficient:

| Ordering | When to use |
|----------|-------------|
| `Relaxed` | Simple counters, statistics -- when you don't need ordering guarantees between threads |
| `SeqCst` | Everything else -- when in doubt, use this (it's the strongest/safest) |

> **Rule of thumb**: Start with `SeqCst`. Only switch to weaker orderings (`Acquire`/`Release`, `Relaxed`) when you understand why and have measured a performance need.

## Exercises
- [ ] **Atomic counter**: Create an `AtomicUsize` shared across 10 threads (each incrementing 10,000 times using `fetch_add(1, Ordering::Relaxed)`). Verify the final count is exactly 100,000. Compare the code simplicity and performance against the `Arc<Mutex<usize>>` version from lesson 065.
- [ ] **Shutdown flag**: Use an `AtomicBool` as a shutdown signal. Spawn a worker thread that loops and checks the flag each iteration using `load(Ordering::Acquire)`. The main thread sleeps for 100ms, then sets the flag to `true` using `store(true, Ordering::Release)`. Verify the worker stops. Explain why `Acquire`/`Release` ordering is used here.
- [ ] **Atomic vs Mutex benchmark**: Implement a shared counter using (a) `AtomicUsize` with `fetch_add`, (b) `Arc<Mutex<usize>>`, and (c) `Arc<RwLock<usize>>`. Run each with 8 threads doing 1,000,000 increments. Time each approach and print a comparison table. Discuss when the performance difference matters.

  **Starter code** -- Use this timing harness. Your job is to fill in each closure with the threaded counter implementation.

  ```rust
  use std::time::Instant;

  fn bench(label: &str, f: impl Fn()) {
      let start = Instant::now();
      f();
      println!("{}: {:?}", label, start.elapsed());
  }

  fn main() {
      let iterations = 1_000_000;
      let threads = 8;

      bench("AtomicUsize", || { /* your atomic implementation */ });
      bench("Mutex<usize>", || { /* your Mutex implementation */ });
      bench("RwLock<usize>", || { /* your RwLock implementation */ });
  }
  ```
- [ ] **Simple spin lock [STRETCH]**: Implement a basic `SpinLock` struct using `AtomicBool`. The `lock()` method loops calling `compare_exchange(false, true, Ordering::Acquire, Ordering::Relaxed)` until it succeeds. The `unlock()` method calls `store(false, Ordering::Release)`. Test it with multiple threads protecting a shared `Vec`. Discuss why real code uses `Mutex` instead of spin locks.

## Notes
_Lesson not yet started._
