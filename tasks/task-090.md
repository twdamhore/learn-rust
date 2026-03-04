# Lesson 090: Database - sqlx, connection pools, migrations

## Section 19: Ecosystem & Tooling

## Status: pending

## Added
- Initial curriculum design

### Prerequisites
```bash
# Install sqlx-cli
cargo install sqlx-cli --no-default-features --features sqlite
# Set database URL
export DATABASE_URL="sqlite:./dev.db"
```

> **Setup time warning**: Setting up sqlx compile-time query checking (DATABASE_URL, `sqlx prepare`) can take 20-30 minutes on first encounter. Budget extra time for setup.

## Objectives
- [ ] Set up `sqlx` with SQLite (no external database server needed), understanding the difference between compile-time checked queries (`sqlx::query!`) and runtime queries (`sqlx::query`)
- [ ] Use `sqlx::query!` and `sqlx::query_as!` macros for compile-time verified SQL, mapping rows to Rust structs with `FromRow`
- [ ] Create and run database migrations using `sqlx migrate` CLI commands and embedded migrations with `sqlx::migrate!()`
- [ ] Set up and use connection pools with `SqlitePool`, understanding pool sizing, connection reuse, and why pooling matters for async applications
- [ ] Implement async CRUD operations using `sqlx` within a Tokio runtime, handling database errors with proper error types

## Exercises
- [ ] **Exercise 1 - SQLite Setup and Migrations**: Set up a new project with `sqlx` and SQLite: create a migration that defines a `tasks` table (id, title, description, completed, created_at), run the migration, and verify the schema was created using `sqlx::query` to list tables
- [ ] **Exercise 2 - CRUD Module**: Implement a full CRUD module for the `tasks` table using compile-time checked queries: `create_task`, `get_task_by_id`, `list_tasks`, `update_task`, `delete_task` -- each function takes a `&SqlitePool` and returns `Result<_, sqlx::Error>`
- [ ] **Exercise 3 - Integration Tests**: Write an integration test that creates a temporary in-memory SQLite database, runs migrations, performs all CRUD operations, and asserts correctness -- use `#[sqlx::test]` if available, or set up the pool manually in a `#[tokio::test]`
- [ ] **Exercise 4 - Repository Pattern [STRETCH]**: Implement a repository pattern: define a `TaskRepository` trait with async CRUD methods, implement it for `SqliteTaskRepository` that holds a `SqlitePool`, and write a service function that uses `&dyn TaskRepository` to demonstrate the abstraction
  > **Note**: Async methods in traits require either Rust 1.75+ (for return-position `impl Trait` in traits) or the `async-trait` crate.

## Notes
> **SUPERSEDED**: This lesson was split into task-090a.md (SQLite setup, migrations, queries) and task-090b.md (CRUD, testing, repository pattern) during the v13 pacing review on 2026-03-04. The original was ~2.5 hrs with setup time.

_Lesson not yet started._
