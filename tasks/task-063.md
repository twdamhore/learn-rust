# Lesson 063: Futures, async fn, .await, what the runtime does

## Section 14: Async Rust

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Understand the `Future` trait and its `poll`-based execution model (`Poll::Ready` vs `Poll::Pending`)
- [ ] Write `async fn` functions and chain them with `.await`, understanding that each `.await` is a yield point
- [ ] Explain what an async runtime does (executor polls futures, reactor watches I/O) and why Rust has no built-in runtime
- [ ] Compare Rust's async model with Java's `CompletableFuture` (callback-based) and Go's goroutines (preemptive green threads)
- [ ] Demonstrate that Rust futures are lazy -- they do nothing until polled by an executor

## Exercises
- [ ] **Lazy futures demo**: Write an `async fn` that prints a message and returns a value; call the function without `.await` and observe that nothing prints; then `.await` it and confirm the output appears
- [ ] **Chaining awaits**: Write three `async fn`s that simulate stages of a pipeline (fetch, transform, store) with `println!` markers; chain them with `.await` in a fourth `async fn` and verify the execution order
- [ ] **Tokio hello world**: Add `tokio` as a dependency, annotate `main` with `#[tokio::main]`, and run an async function that sleeps for 1 second using `tokio::time::sleep` then prints a greeting
- [ ] **Future trait exploration**: Read the signature of `std::future::Future` in the docs; write a short summary in comments explaining what `type Output`, `fn poll`, `Context`, and `Waker` each do

## Notes
_Lesson not yet started._
