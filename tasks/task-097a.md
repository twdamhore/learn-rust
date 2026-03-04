# Lesson 097a: Capstone Project 2 - Part A: Axum Web API Basics

## Section 21: Capstone Projects

## Status: pending

## Prerequisites
- Lesson 060 (Shared state — `Mutex`, `Arc<Mutex<T>>`)
- Lesson 063-064 (async/await, Tokio basics)
- Lesson 086 (serde - for JSON serialization)

## Added
- Split from lesson 097 (v6 pacing review)

## Objectives
- [ ] Introduction to `axum`: understand Router, handler functions, extractors (Path, Query, Json), State, and response types -- this provides the axum introduction that was missing from the curriculum
- [ ] Set up a basic REST API with axum and Tokio: create routes, handle JSON request/response bodies, and run the server
- [ ] Implement CRUD routes with in-memory storage (`Arc<Mutex<Vec<Note>>>` or `Arc<Mutex<HashMap>>`): create, read, update, and delete operations
- [ ] Return structured JSON responses with appropriate HTTP status codes using `axum::Json` and `StatusCode`

## Exercises

> **Axum version**: Use `axum = "0.8"` -- the latest stable version. API details may differ from older tutorials.

> **Cargo.toml dependencies for this lesson:**
> ```toml
> [dependencies]
> axum = "0.8"
> tokio = { version = "1", features = ["full"] }
> serde = { version = "1", features = ["derive"] }
> serde_json = "1"
> ```

- [ ] **Exercise 1 -- Axum basics**: Set up a new `notesapi` project with axum and tokio. Create three routes: `GET /health` (returns `{"status": "ok"}`), `GET /notes` (returns a JSON array from an in-memory `Vec<Note>` stored in `State`), and `POST /notes` (accepts a JSON body, adds to the Vec, returns the created note with 201 status). Test with `curl`. (This pattern — `Arc<Mutex<Vec<T>>>` for shared mutable state — was covered in lesson 060.)
- [ ] **Exercise 2 -- Full CRUD**: Add the remaining CRUD routes: `GET /notes/:id` (return 404 if not found), `PUT /notes/:id` (update title/body, return 404 if not found), `DELETE /notes/:id` (remove and return 204, or 404 if not found). Use `Path` extractor for the ID parameter.
- [ ] **Exercise 3 -- Error responses**: Create a custom `ApiError` enum with variants like `NotFound`, `BadRequest(String)`. Implement `IntoResponse` for it to return proper HTTP status codes and JSON error bodies (`{ "error": "Note not found" }`). Validate that note titles are non-empty on POST/PUT. Test all error cases with `curl`.

## Notes
_Lesson not yet started._
_Split from original lesson 097 which was rated OVERLOADED (~3-4 hr). This part uses in-memory storage only. SQLite and auth are in Part B (097b). This provides the axum introduction that was missing from the curriculum._
