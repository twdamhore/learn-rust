# Lesson 066: Streams, async iterators, async channels

## Section 14: Async Rust

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Understand the `Stream` trait as the async equivalent of `Iterator` (yields items over time via `poll_next`)
- [ ] Use `tokio-stream` crate utilities to create, transform, and consume streams (`StreamExt::map`, `filter`, `take`, `next`)
- [ ] Use `tokio::sync::mpsc` channels to build async producer-consumer patterns and convert the receiver into a stream
- [ ] Understand backpressure in async systems -- how bounded channels naturally apply it when the buffer is full

## Exercises

**Setup**: Add `tokio-stream` to your dependencies: `cargo add tokio-stream --features sync`. This crate provides stream adaptors and wrappers for tokio channels.

- [ ] **Channel to stream**: Create a `tokio::sync::mpsc::channel(10)`, spawn a producer that sends numbers 1-20 with small delays, and consume the receiver as a stream using `tokio_stream::wrappers::ReceiverStream`; print each item as it arrives
- [ ] **Stream processing pipeline**: Create a stream of integers 1-100, use `filter` to keep only even numbers, `map` to square them, and `take(10)` to limit results; collect into a `Vec` and print it
  Hint: Use `tokio_stream::iter(1..=100)` to create the initial stream of integers.
- [ ] **Rate-limited consumer**: Create a producer that sends items as fast as possible into a bounded channel (capacity 5); in the consumer, add a 100ms delay per item; observe how the producer blocks when the channel is full (backpressure)
- [ ] **Async producer-consumer [STRETCH]**: Build a system with 3 producer tasks each sending tagged messages into a single `mpsc` channel, and 1 consumer task that processes them; use the stream API to merge and process messages; print statistics (count per producer) at the end

## Notes
_Lesson not yet started._
