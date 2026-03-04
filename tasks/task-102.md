# Lesson 102: Database Part B - CRUD, Testing, and Repository Pattern

## Section 19: Ecosystem & Tooling

## Status: pending

## Added
- Split from task-101 (v13 pacing review, 2026-03-04)

## Objectives
- [ ] Set up and use connection pools with `SqlitePool`, understanding pool sizing, connection reuse, and why pooling matters for async applications
- [ ] Implement complete async CRUD operations using `sqlx` within a Tokio runtime, handling database errors with proper error types
- [ ] Write database integration tests using temporary in-memory SQLite databases

## Exercises
- [ ] **Exercise 1 - Complete CRUD Module**: Extend the query functions from 101 into a full CRUD module: add `update_task(pool, id, title, description, completed)` and `delete_task(pool, id)`. Each function takes a `&SqlitePool` and returns `Result<_, sqlx::Error>`. Test the full create-read-update-delete cycle
- [ ] **Exercise 2 - Integration Tests**: Write an integration test that creates a temporary in-memory SQLite database, runs migrations, performs all CRUD operations, and asserts correctness -- use `#[sqlx::test]` if available, or set up the pool manually in a `#[tokio::test]`
- [ ] **Exercise 3 - Repository Pattern [STRETCH]**: Implement a repository pattern: define a `TaskRepository` trait with async CRUD methods, implement it for `SqliteTaskRepository` that holds a `SqlitePool`, and write a service layer using one of these two paths:
  - **Path A (recommended)**: use `async-trait` and dynamic dispatch (`&dyn TaskRepository`)
  - **Path B (advanced)**: no `async-trait`; keep the service generic (`R: TaskRepository`) using return-position `impl Trait` in trait methods
  > **Important**: `&dyn TaskRepository` and async trait methods are only straightforward with `async-trait`. Without it, prefer generic service functions over trait objects.

## Notes
- ~1-1.5 hours estimated
- Prerequisite: 101 (SQLite setup and queries)
- If you choose Path A in Exercise 3, add `async-trait = "0.1"` to dependencies.
