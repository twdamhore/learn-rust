# Lesson 059: Message passing - channels, mpsc, patterns

## Section 13: Concurrency

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Use `std::sync::mpsc::channel()` to create an unbounded channel with a `Sender` (tx) and `Receiver` (rx) for message passing between threads
- [ ] Send various data types through channels, understanding that `send()` transfers ownership of the value to the receiver
- [ ] Clone the `Sender` to enable multiple producer threads sending to a single consumer (the "mpsc" pattern: multiple producer, single consumer)
- [ ] Use `sync_channel` for bounded/synchronous channels where the sender blocks when the buffer is full
- [ ] Compare Rust channels with Go channels: both transfer ownership, but Go channels are multi-producer multi-consumer while Rust's `mpsc` is multi-producer single-consumer; Rust has no `select!` in std (but `crossbeam` does)

## Exercises
- [ ] **Basic producer-consumer**: Spawn a producer thread that sends the numbers 1..=10 through a channel. The main thread receives and prints each value. Use both `rx.recv()` (blocking) and iteration over `rx` (which ends when all senders are dropped).
- [ ] **Sending structs**: Define a `LogEntry { level: String, message: String, timestamp: u64 }` struct. Spawn a thread that creates and sends 5 log entries through a channel. The receiver collects them into a `Vec` and prints a formatted summary. Demonstrate that the sender no longer owns the entries after sending.
- [ ] **Multiple producers**: Clone the sender 3 times, giving each clone to a different thread. Each thread sends its thread ID and a sequence of messages. The single receiver prints all messages in arrival order. Observe interleaving. Count total messages received to verify none were lost.
- [ ] **Bounded channel task queue**: Use `sync_channel(2)` to create a bounded channel. Spawn a "slow" consumer that sleeps briefly between processing items. Spawn a fast producer that sends 10 items. Observe that the producer blocks when the buffer is full. Print timestamps to demonstrate the backpressure behavior.

## Notes
_Lesson not yet started._
