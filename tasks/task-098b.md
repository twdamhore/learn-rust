# Lesson 098b: Project 2 Part D: Testing and Deployment

## Section 21: Capstone Projects

## Status: pending

## Added
- Split from original lesson 098 (v7 pacing review)

## Objectives
- [ ] Write integration tests for API endpoints by spinning up the server with a fresh in-memory SQLite database, making real HTTP requests with `reqwest`, and verifying responses including status codes, headers, and JSON bodies
- [ ] Test the full authentication flow end-to-end: register/login to get a JWT, use the token for authenticated requests, verify rejection of invalid/expired/missing tokens
- [ ] Test CRUD operations end-to-end and error cases: not found (404), validation failure (400/422), unauthorized (401), ensuring the API behaves correctly under all conditions
- [ ] Create a production-ready deployment configuration: multi-stage Dockerfile, externalized configuration via environment variables with sensible defaults, and a health check endpoint that verifies database connectivity

## Exercises
- [ ] **Integration test suite**: Create a `tests/api.rs` file with a helper function that starts the server on a random available port with a fresh in-memory SQLite database and returns the base URL. Write the following tests using `#[tokio::test]`:
  - [ ] **(Required) CRUD happy-path test**: Create a note, read it back, update it, list all notes (verify the updated content appears), delete it, and verify it returns 404 afterward.
  - [ ] **[STRETCH] Auth flow test**: Register a user, login, receive a valid JWT, use the JWT to access a protected endpoint, and verify that an invalid token returns 401.
  - [ ] **[STRETCH] Error cases test**: Request a non-existent note (404), send an invalid JSON body (400/422), access a protected endpoint without a token (401).
> **Docker**: If Docker is not installed, write the Dockerfile and docker-compose.yml without building. The file contents are the learning goal. To verify later: `docker build -t my-api .`

- [ ] **Dockerfile and deployment config**: **Note**: This exercise has two distinct parts: (1) implementing the `GET /health` endpoint in Rust code, and (2) writing the Dockerfile for deployment. Consider tackling them as separate sub-tasks. Create a multi-stage `Dockerfile` using `rust:slim-bookworm` as the builder stage and `debian:bookworm-slim` as the runtime stage. Externalize all configuration (database URL, JWT secret, port, log level) via environment variables with sensible defaults using a config struct that reads from `std::env`. Add a `GET /health` endpoint that checks database connectivity by running a simple query (`SELECT 1`) and returns 200 with `{"status": "ok"}` on success or 503 with `{"status": "degraded", "error": "..."}` on failure. Document the build and run commands in comments at the top of the Dockerfile.

## Notes
_Lesson not yet started._
