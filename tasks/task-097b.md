# Lesson 097b: Capstone Project 2 - Part B: Database and Authentication

## Section 21: Capstone Projects

## Status: pending

## Prerequisites
- Lesson 097a (Axum Web API Basics)
- Lesson 090 (sqlx - for database operations)

## Added
- Split from lesson 097 (v6 pacing review)

## Objectives
- [ ] Replace in-memory storage with SQLite via `sqlx`: set up a connection pool, create migrations for the notes table, pass the pool to handlers via axum's `State` extractor
- [ ] Add JWT authentication using the `jsonwebtoken` crate: issue tokens on login, validate tokens in requests
- [ ] Add authentication middleware: create an `AuthUser` extractor that verifies the JWT from the `Authorization: Bearer <token>` header, and protect write endpoints while leaving read endpoints public

## Exercises

> **Additional Cargo.toml dependencies for this lesson** (add to the 097a dependencies):
> ```toml
> [dependencies]
> sqlx = { version = "0.8", features = ["runtime-tokio", "sqlite"] }
> jsonwebtoken = "9"
> ```

> **Time check**: If you reach 90 minutes before starting Exercise 3 (auth middleware), defer it to a follow-up session. Exercises 1-2 (sqlx integration) are the core learning goals.

> **Time management**: If Exercise 1 (sqlx migration) takes longer than 60 minutes, consider deferring Exercise 2 (JWT) to a separate session.

- [ ] **Exercise 1 -- SQLite persistence**: Set up SQLite with `sqlx`. Create a migration for a `notes` table (id, title, body, created_at, updated_at). Migrate the CRUD handlers from in-memory Vec to database queries using `sqlx`. Pass `SqlitePool` via `State`. Verify end-to-end with `curl`.
- [ ] **Exercise 2 -- JWT authentication**: Add a `POST /auth/login` endpoint that accepts a username/password JSON body and returns a JWT token (use hardcoded credentials for simplicity, or add a users table). Use the `jsonwebtoken` crate to create and verify tokens with a shared secret.
> **JWT (JSON Web Token) primer**: A JWT is a signed JSON payload with three parts: header.payload.signature. The server creates a token on login (encoding user ID + expiry), and the client sends it in the `Authorization: Bearer <token>` header. The server verifies the signature on each request. The `jsonwebtoken` crate handles encoding/decoding.

- [ ] **Exercise 3 [STRETCH] -- Auth middleware and protected routes**: Create an `AuthUser` extractor that reads the `Authorization: Bearer <token>` header, validates the JWT, and extracts the user info. Protect write endpoints (POST/PUT/DELETE) with this extractor while leaving read endpoints (GET) public. Return 401 for missing/invalid tokens.

## Notes
_Lesson not yet started._
_Split from original lesson 097 which was rated OVERLOADED (~3-4 hr). This part adds database persistence and authentication to the API built in 097a._
