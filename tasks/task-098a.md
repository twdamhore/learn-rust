# Lesson 098a: Project 2 Part C: Async Patterns and Observability

## Section 21: Capstone Projects

## Status: pending

## Added
- Split from original lesson 098 (v7 pacing review)

## Objectives
- [ ] Implement a concurrent stats endpoint using `tokio::join!` to run multiple database queries in parallel, understanding when concurrency helps (independent I/O-bound operations) vs when it adds unnecessary overhead
- [ ] Add structured logging and tracing with the `tracing` crate: configure `tracing-subscriber` with `fmt` layer and `EnvFilter` for runtime log-level control via `RUST_LOG`
- [ ] Instrument handler and repository functions with `#[tracing::instrument]`, understanding what fields are automatically captured and how to skip or rename parameters
- [ ] Implement a request logging middleware layer that logs method, path, status code, and latency for every request, using `tracing::Span` to correlate logs within a single request

## Exercises
- [ ] **Concurrent stats endpoint**: Implement a `GET /notes/stats` endpoint that concurrently fetches total note count, count by date range (last 7 days), and average body length using `tokio::join!` to run all three queries in parallel. First implement a sequential version, then refactor to concurrent. Add a response header `X-Query-Time-Ms` to both versions and compare the response times in your tests. Verify that the concurrent version is faster when the database has simulated latency.
  > **Hint**: To make the sequential vs concurrent difference visible, add `tokio::time::sleep(Duration::from_millis(50)).await` to your repository functions to simulate database latency.
- [ ] **Add tracing**: Set up `tracing-subscriber` and add `#[tracing::instrument]` to your handler functions. Configure `tracing-subscriber` with a `fmt` layer and `EnvFilter` so that running `RUST_LOG=info cargo run` shows info-level logs and `RUST_LOG=my_api=debug` shows debug-level logs for your crate only. Add `#[tracing::instrument]` to all handler functions (skipping large parameters like request bodies with `skip`) and all repository functions. Verify spans appear in logs.
- [ ] **Add tower-http middleware**: Add `tower-http`'s `TraceLayer` middleware to your router for automatic request/response logging. (tower-http provides HTTP-specific middleware for tower-based frameworks like axum, including request/response logging, CORS, compression, and tracing integration.) Verify that each request generates a span with method, path, and status code.

## Notes
_Lesson not yet started._
