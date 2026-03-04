# Lesson 098: Project 2 - continued (async patterns, deployment)

## Section 21: Capstone Projects

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Implement async patterns in the API: concurrent database queries with `tokio::join!`, background tasks with `tokio::spawn`, and graceful shutdown with `tokio::signal`
- [ ] Add structured logging and tracing with the `tracing` crate: instrument handlers with `#[tracing::instrument]`, add a request ID middleware, and configure log levels via environment variables
- [ ] Write integration tests for API endpoints using `axum::test` helpers or by spawning the server and making HTTP requests with `reqwest`, including tests for auth flows
- [ ] Add pagination (limit/offset) and search/filtering to the list endpoint using query parameters
- [ ] Configure the application for deployment: externalize config (database URL, JWT secret, port) via environment variables or a config file using `dotenvy` and a config struct

## Exercises
- [ ] Implement a `GET /notes/stats` endpoint that concurrently fetches total count, count by date range, and average body length using `tokio::join!` to run all three queries in parallel -- compare the response time with sequential execution
- [ ] Add `tracing` to the project: configure `tracing-subscriber` with `fmt` and `EnvFilter`, add `#[tracing::instrument]` to all handler and repository functions, implement a middleware layer that logs request method, path, status code, and latency for every request
- [ ] Write integration tests: create a `tests/api.rs` file that spins up the server with a fresh in-memory database, tests the full auth flow (login, use token, reject invalid token), tests CRUD operations end-to-end, and tests error cases (not found, validation failure, unauthorized)
- [ ] Add deployment configuration: create a `Dockerfile` (multi-stage build with `rust:slim` builder and `debian:slim` runtime), externalize all configuration via environment variables with sensible defaults, add a health check endpoint `GET /health` that verifies the database connection, and document how to build and run the container

## Notes
_**SUPERSEDED**: This lesson has been split into [Lesson 98a](task-098a.md) and [Lesson 98b](task-098b.md). Use those files instead._

_Lesson not yet started._
