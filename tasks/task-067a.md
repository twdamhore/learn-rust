# Lesson 067a: Advanced Async - Part A: The Future Trait and Cancellation

## Section 14: Async Rust

## Status: pending

## Added
- Split from lesson 067 (v6 pacing review)

## Objectives
- [ ] Understand the `Future` trait: `poll`, `Context`, `Poll::Ready` vs `Poll::Pending`
- [ ] Implement a simple Future by hand (e.g., a Delay/Countdown future)
- [ ] Understand async cancellation and drop semantics -- what happens when a future is dropped before completion
- [ ] Compare to Java `CompletableFuture` and Go context cancellation

## Exercises
- [ ] **Countdown future**: Implement a `Countdown` future that starts at a given number and returns `Poll::Pending` until it has been polled enough times, then returns `Poll::Ready(())`. This is the simplest possible hand-written `Future` -- no threads, no sleeping, just counting polls. Test it with `block_on` or `tokio::runtime`.
- [ ] **TimerFuture**: Implement a `TimerFuture` that resolves after a duration using `thread::sleep` + `Waker`; test it with `tokio::runtime`
- [ ] **Timeout combinator [STRETCH]**: Build a `Timeout` combinator that wraps a future and returns an error if it takes too long; implement `Future` for `Timeout<F>` manually. This exercise uses `Pin<Box<F>>` and `Pin<&mut Self>` -- concepts covered in lesson 067b. Attempt it after completing 067b if you want practice combining Future implementation with Pin.

  **Skeleton** -- Start with this struct and trait impl. Your job is to fill in the fields and the `poll` logic.

  ```rust
  use std::pin::Pin;
  use std::task::{Context, Poll};
  use std::future::Future;

  struct Timeout<F> {
      future: Pin<Box<F>>,
      // What else do you need to track the deadline?
  }

  impl<F: Future> Future for Timeout<F> {
      type Output = Result<F::Output, &'static str>;

      fn poll(self: Pin<&mut Self>, cx: &mut Context<'_>) -> Poll<Self::Output> {
          // 1. Check if the inner future is ready
          // 2. Check if the deadline has passed
          // 3. If neither, register the waker and return Pending
          todo!()
      }
  }
  ```
- [ ] **Cancellation observation**: Write code demonstrating cancellation -- drop a future mid-execution and observe cleanup via a `Drop` impl on a guard struct; use `select!` with a timeout to trigger the drop

## Notes
_Lesson not yet started._
