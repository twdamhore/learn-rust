# Lesson 101: Database Part A - SQLite Setup, Migrations, and Queries

## Section 19: Ecosystem & Tooling (split from lesson 101)

## Status: pending

## Added
- Split from task-101 (v13 pacing review, 2026-03-04)

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

## Exercises
- [ ] **Exercise 1 - SQLite Setup and Migrations**: Set up a new project with `sqlx` and SQLite: create a migration that defines a `tasks` table (id, title, description, completed, created_at), run the migration, and verify the schema was created using `sqlx::query` to list tables
- [ ] **Exercise 2 - Basic Queries**: Write functions using compile-time checked queries: `create_task(pool, title, description)` to insert a row, `get_task_by_id(pool, id)` to fetch a single task (return `Option`), and `list_tasks(pool)` to fetch all tasks. Map results to a `Task` struct using `FromRow`. Test each function with a simple `#[tokio::main]` driver

## Notes
- ~1-1.5 hours estimated (includes setup time)
- Continues in 102 (CRUD completion, testing, repository pattern)
