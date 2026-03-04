# Lesson 065: Async I/O - files, networking, timers

## Section 14: Async Rust

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Read and write files asynchronously using `tokio::fs` (`read_to_string`, `write`, `File::open`)
- [ ] Build an async TCP client and server using `tokio::net::TcpListener` and `TcpStream`
- [ ] Use `tokio::time::timeout` to add deadlines to async operations and handle `Elapsed` errors
- [ ] Understand why async I/O is more efficient than spawning a thread per connection (event-driven, non-blocking)

## Exercises
- [ ] **Async file reader**: Write a program that reads 3 text files concurrently using `tokio::fs::read_to_string` and `tokio::join!`; print each file's line count; compare wall-clock time with sequential reads
- [ ] **Echo TCP server**: Build an async TCP echo server that accepts multiple connections concurrently; for each connection spawn a task that reads lines and echoes them back; test with `telnet` or a simple async client
- [ ] **Timeout wrapper**: Wrap a slow async operation (a 5-second sleep) in `tokio::time::timeout(Duration::from_secs(2), ...)` and handle the timeout error gracefully; print whether the operation completed or timed out
- [ ] **Concurrent file processor**: Given a directory of text files, write a program that reads all files concurrently, counts the total number of words across all files, and prints the result; use `tokio::fs::read_dir` to list files

## Notes
_**SUPERSEDED**: This lesson has been split into [Lesson 65a](task-065a.md) and [Lesson 65b](task-065b.md). Use those files instead._

_Lesson not yet started._
