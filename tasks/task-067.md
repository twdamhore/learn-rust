# Lesson 067: Advanced async - Pin/Unpin in depth, writing a mini executor, cancellation

## Section 14: Async Rust

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Understand what `Pin<T>` guarantees (the pointed-to value will not be moved in memory) and why async futures need it
- [ ] Explain the `Unpin` marker trait -- most types are `Unpin` and can be freely moved even when pinned
- [ ] Understand why self-referential futures (created by `async fn` with references across `.await` points) require pinning
- [ ] Understand async cancellation: what happens when a future is dropped before completion, and how to handle cleanup
- [ ] Trace through a minimal executor loop conceptually: `poll` -> `Pending` -> `Waker::wake` -> `poll` -> `Ready`

## Exercises
- [ ] **Implement a Future by hand**: Create a struct `Countdown { remaining: u32 }` that implements `Future` manually; each `poll` call decrements the counter; when it reaches 0, return `Poll::Ready("done!")`; test it with `tokio::runtime`
- [ ] **Cancellation observation**: Spawn an async task that prints "started", sleeps for 5 seconds, then prints "finished"; drop the `JoinHandle` (or use `select!` with a timeout) after 1 second and observe that "finished" never prints; add a `Drop` impl on a guard struct to print "cancelled"
- [ ] **Basic poll loop**: Write a function that creates a `Countdown` future, wraps it in `Box::pin`, and manually calls `poll` in a loop using a no-op waker from `std::task::Wake`; print the poll results until `Ready`
- [ ] **Pin exploration**: Demonstrate that a `Vec<u8>` (which is `Unpin`) can be moved after pinning with `Pin::new`, but a `!Unpin` type created with `pin!()` macro cannot; write code that would fail to compile if you tried to move a pinned `!Unpin` value, and comment out the failing line with an explanation

## Notes
_**SUPERSEDED**: This lesson has been split into [Lesson 67a](task-067a.md) and [Lesson 67b](task-067b.md). Use those files instead._

_Lesson not yet started._
