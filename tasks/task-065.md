# Lesson 065: Shared state - Mutex<T>, RwLock, Arc<Mutex<T>>

## Section 13: Concurrency

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Use `Mutex<T>` for mutual exclusion: `lock()` returns a `MutexGuard` that auto-unlocks when dropped, ensuring data access is always synchronized
- [ ] Combine `Arc<Mutex<T>>` to share mutable state across multiple threads (Arc for shared ownership, Mutex for synchronized mutation)
- [ ] Use `RwLock<T>` for read-heavy workloads where multiple concurrent readers are allowed but writers get exclusive access
- [ ] Handle lock poisoning: understand that a `Mutex` becomes poisoned if a thread panics while holding the lock, and how to recover with `into_inner()` or `PoisonError`
- [ ] Compare Rust's `Mutex<T>` (protects data, not code) with Java's `synchronized` (protects code blocks) and Go's `sync.Mutex` (protects code, not data)

## Exercises
- [ ] **Shared counter**: Create an `Arc<Mutex<i32>>` counter. Spawn 10 threads, each incrementing the counter 1000 times. Join all threads and verify the final count is exactly 10000. Explain why this would be a data race without the Mutex.
- [ ] **Thread-safe cache**: Build a `Cache` struct wrapping an `Arc<RwLock<HashMap<String, String>>>`. Implement `get(&self, key: &str) -> Option<String>` (uses `read()`) and `insert(&self, key: String, value: String)` (uses `write()`). Spawn reader and writer threads concurrently and verify correctness.
- [ ] **Mutex vs RwLock comparison [STRETCH]**: Create a shared `Vec<i32>` behind both a `Mutex` and an `RwLock`. Spawn 8 reader threads and 2 writer threads for each. Time both approaches using `std::time::Instant` and compare throughput. Print results showing when `RwLock` wins.
- [ ] **Poisoned lock recovery**: Spawn a thread that locks a `Mutex<Vec<String>>`, pushes a value, then panics. In the main thread, attempt to lock the mutex, observe the `PoisonError`, recover the inner data with `into_inner()`, and print the partially-modified data. Explain when you'd want to recover vs propagate the error.

## Notes
_Lesson not yet started._
