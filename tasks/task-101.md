# Lesson 101: Database Part A - SQLite Setup, Migrations, and Queries

## Section 19: Ecosystem & Tooling

## Status: pending

## Added
- Split from original lesson 101 content (v13 pacing review, 2026-03-04)

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
- [ ] Use `sqlx::query!` and `sqlx::query_as!` macros for compile-time verified SQL and typed row mapping (field names/types must match at compile time)
- [ ] Create and run database migrations using `sqlx migrate` CLI commands and embedded migrations with `sqlx::migrate!()`

## Exercises
- [ ] **Exercise 1 - SQLite Setup and Migrations**: Set up a new project with `sqlx` and SQLite: create a migration that defines a `tasks` table (id, title, description, completed, created_at), run the migration, and verify the schema was created using `sqlx::query` to list tables
- [ ] **Exercise 2 - Basic Queries**: Write functions using compile-time checked queries: `create_task(pool, title, description)` to insert a row, `get_task_by_id(pool, id)` to fetch a single task (return `Option`), and `list_tasks(pool)` to fetch all tasks. Use `query_as!` for typed mapping into a `Task` struct with matching field names/types. Test each function with a simple `#[tokio::main]` driver

## Notes
- ~1-1.5 hours estimated (includes setup time)
- Continues in 102 (CRUD completion, testing, repository pattern)
- Optional follow-up: try runtime mapping with `query_as::<_, Task>(...)` plus `#[derive(sqlx::FromRow)]` to compare ergonomics.
