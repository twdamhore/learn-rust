# Lesson 063: Threads - std::thread, move, join, scoped threads

## Section 13: Concurrency

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Spawn OS threads with `std::thread::spawn` and understand that the closure must be `'static` (own all its data) unless using scoped threads
- [ ] Use `move` closures with threads to transfer ownership of data into the spawned thread
- [ ] Join threads with `JoinHandle::join()` and handle the `Result` it returns (which carries panics from the child thread)
- [ ] Use `std::thread::scope` to spawn scoped threads that can borrow data from the parent stack without `'static` requirements
- [ ] Compare Rust threads with Java's `Thread`/`Runnable` and Go's goroutines (lightweight vs OS threads, compile-time safety vs runtime race detection)

## Exercises
- [ ] **Basic thread spawning**: Spawn 5 threads, each printing its index and thread ID (`std::thread::current().id()`). Join all threads and print "all done" from the main thread. Observe that print order is non-deterministic.
- [ ] **Move and ownership**: Create a `Vec<String>` of names. Spawn a thread with `move` that sorts and prints the names. After joining, verify the original variable is no longer accessible. Then refactor to clone the data so both threads can use it.
- [ ] **Scoped threads for borrowing**: Use `std::thread::scope` to spawn threads that borrow slices of a shared `&[i32]` array. Each thread computes the sum of its slice. Collect the partial sums and compute the total. Explain why this doesn't need `move` or `Arc`.
- [ ] **Parallel computation [STRETCH]**: Implement a parallel `map` function: given a `Vec<i32>` and a function `fn(i32) -> i32`, split the vector into N chunks (one per available CPU via `std::thread::available_parallelism()`), process each chunk in a scoped thread, and combine results into a single `Vec<i32>`. Test with a computationally expensive closure (e.g., checking primality).

## Notes
_Lesson not yet started._
