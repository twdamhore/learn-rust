# Lesson 097: Project 2 - Web API (axum, sqlx, auth, middleware)

## Section 21: Capstone Projects

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Set up an `axum` web server with a Tokio runtime, defining routes with the Router, extractors (Path, Query, Json), and response types
- [ ] Design a REST API for a resource (e.g., "notes" or "bookmarks"): GET list, GET by ID, POST create, PUT update, DELETE -- following REST conventions
- [ ] Integrate `sqlx` with SQLite for persistence: set up a connection pool, pass it to handlers via axum's State extractor, run migrations at startup
- [ ] Implement authentication middleware: issue and validate JWT tokens using `jsonwebtoken`, protect routes with an extractor that verifies the Authorization header
- [ ] Structure the project with clean separation: handlers (HTTP concerns), services (business logic), and repositories (database access) in separate modules

## Exercises
- [ ] Create a new project `notesapi` with axum: define routes for a "notes" resource (`GET /notes`, `GET /notes/:id`, `POST /notes`, `PUT /notes/:id`, `DELETE /notes/:id`), initially returning hardcoded JSON responses, and verify with `curl` or a REST client
- [ ] Add SQLite persistence: create a migration for a `notes` table (id, title, body, created_at, updated_at), implement a `NotesRepository` with async CRUD methods using `sqlx`, wire the pool into handlers via `State<SqlitePool>`, and verify end-to-end with curl
- [ ] Implement JWT authentication: add a `POST /auth/login` endpoint that accepts username/password and returns a JWT, create an `AuthUser` extractor that validates the JWT from the `Authorization: Bearer <token>` header, and protect the write endpoints (POST/PUT/DELETE) while leaving read endpoints public
- [ ] Add request validation and error handling: use a custom `ApiError` type that implements `IntoResponse` to return proper HTTP status codes and JSON error bodies (`{ "error": "message" }`), validate that note titles are non-empty and body length is under 10,000 characters, and return 400/401/404/500 as appropriate

## Notes
_**SUPERSEDED**: This lesson has been split into [Lesson 97a](task-097a.md) and [Lesson 97b](task-097b.md). Use those files instead._

_Lesson not yet started._
