# Lesson 098: Logging and tracing - log, tracing, structured logging

## Section 19: Ecosystem & Tooling

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Use the `log` crate facade with `env_logger` backend to add leveled logging (error, warn, info, debug, trace) to a Rust application, and configure log levels via `RUST_LOG`
- [ ] Understand the `tracing` crate and how it improves on `log` with structured fields, spans for context, and async-awareness
- [ ] Add spans with `#[instrument]` and manual `span!`/`enter()` to create hierarchical context that shows the call chain in log output
- [ ] Configure log filtering by module path (e.g., `RUST_LOG=my_app=debug,hyper=warn`) and understand how filtering works with both `log` and `tracing`
- [ ] Use `tracing_appender` for file-based log output, composing it as a layer in `tracing-subscriber`
- [ ] Set up `tracing-subscriber` with a JSON formatter for production-style structured logging that can be consumed by log aggregation tools

## Exercises
- [ ] **Exercise 1 -- log + env_logger basics**: Create a multi-module application (modules: `auth`, `db`, `api`) where each module uses `log::{info, warn, error, debug}`. Initialize `env_logger` in `main()`. Run with `RUST_LOG=info`, `RUST_LOG=debug`, `RUST_LOG=my_app::db=debug,my_app::api=warn` and observe how filtering changes the output. Document the difference between `log` (facade) and `env_logger` (implementation).
- [ ] **Exercise 2 -- tracing spans and events**: Rewrite the application from Exercise 1 using `tracing` instead of `log`. Add `#[instrument]` to key functions. Use `tracing::info!(user_id = %id, action = "login", "User logged in")` with structured fields. Set up `tracing_subscriber::fmt()` and observe how spans appear in the output showing the call hierarchy.
- [ ] **Exercise 3 -- Filtering and layering**: Configure `tracing-subscriber` with an `EnvFilter` that reads from `RUST_LOG`. Add a filter that logs `auth` module at debug level, `db` at info, and everything else at warn. Add a second layer that writes error-level events to a separate file using `tracing_appender`. Demonstrate how layers compose.
- [ ] **Exercise 4 [STRETCH] -- JSON structured logging**: Set up `tracing-subscriber` with `fmt::layer().json()` to output JSON-formatted log lines. Each line should include timestamp, level, target, span context, and structured fields. Write a function that processes a batch of items with a span per item, and show that the JSON output includes the span's item ID. Compare this output to what Go's `slog` or `zap` would produce.

## Notes
_Lesson not yet started._
