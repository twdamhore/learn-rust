# Lesson 070: Async I/O Part A: Files and Timeouts

## Section 14: Async Rust

## Status: pending

## Added
- Split from original lesson 070 (v7 pacing review)

## Objectives
- [ ] Read and write files asynchronously using `tokio::fs` (`read_to_string`, `write`, `File::open`) and understand when async file I/O helps vs. standard `std::fs`
- [ ] Use `tokio::time::timeout` to add deadlines to async operations and handle `Elapsed` errors gracefully
- [ ] Combine `tokio::join!` and `tokio::fs` to perform concurrent file I/O, understanding that async file I/O on most OSes uses a thread pool internally but the calling code remains non-blocking

## Exercises
- [ ] **Async file reader**: Write a program that reads 3 text files concurrently using `tokio::fs::read_to_string` and `tokio::join!`; print each file's line count; compare wall-clock time with sequential reads using `tokio::time::Instant`
- [ ] **Timeout wrapper**: Wrap a slow async operation (a 5-second `tokio::time::sleep`) in `tokio::time::timeout(Duration::from_secs(2), ...)` and handle the timeout error gracefully; print whether the operation completed or timed out; then try with a 10-second timeout to see the success path
- [ ] **[OPTIONAL] Concurrent file processor**: Given a directory of text files, write a program that uses `tokio::fs::read_dir` to list files, reads all of them concurrently, counts the total number of words across all files, and prints the result. Use `futures::future::join_all` or `tokio::task::JoinSet` to manage the concurrent reads

## Notes
_Lesson not yet started._
