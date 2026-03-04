# Lesson 064: Tokio basics - tasks, spawn, select!, join!

## Section 14: Async Rust

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Set up a tokio runtime using `#[tokio::main]` and understand the difference between `current_thread` and `multi_thread` flavors
- [ ] Spawn concurrent tasks with `tokio::spawn` and understand that spawned tasks require `'static + Send` bounds
- [ ] Use `tokio::select!` to race multiple futures and handle whichever completes first
- [ ] Use `tokio::join!` (and `tokio::try_join!`) to run multiple futures concurrently and wait for all of them
- [ ] Explain the difference between a tokio task and an OS thread, including the cooperative scheduling model

## Exercises
- [ ] **Concurrent tasks**: Spawn 5 tasks with `tokio::spawn`, each sleeping for a random duration (100-500ms) and printing its ID; use `JoinHandle` to await all of them and collect their results
- [ ] **Select racing**: Use `tokio::select!` to race two `tokio::time::sleep` futures (200ms vs 500ms); print which branch won; add a third branch that receives from an `mpsc` channel

  > **Note:** `tokio::sync::mpsc` is the async equivalent of `std::sync::mpsc` from lesson 059. The API is similar but `send()` and `recv()` are async (you `.await` them).
- [ ] **Join all**: Simulate 4 concurrent "API calls" using `async fn`s that sleep for different durations; use `tokio::join!` to run them all concurrently and print the total elapsed wall-clock time (should be close to the longest sleep, not the sum)
- [ ] **Task vs thread comparison**: Write the same workload (spawn 1000 units of work that each sleep 10ms) once with `tokio::spawn` and once with `std::thread::spawn`; compare wall-clock time (primary metric) and optionally memory usage

  > **Tip:** Compare wall-clock time first (this alone is dramatic at 1000 units). For optional memory comparison on Linux: `cat /proc/self/status | grep VmRSS` from within the program, or observe with `htop` in another terminal.

## Notes
_Lesson not yet started._
