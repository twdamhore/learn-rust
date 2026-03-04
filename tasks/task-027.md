# Lesson 027: Cargo workspaces, features, profiles

## Section 6: Project Organization

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Create a Cargo workspace with a root `Cargo.toml` containing `[workspace] members = [...]` and multiple member packages that share a `target/` directory and `Cargo.lock`
- [ ] Understand how workspace members depend on each other using `path` dependencies in their individual `Cargo.toml` files
- [ ] Define and use Cargo features with `[features]` in `Cargo.toml` for conditional compilation using `#[cfg(feature = "...")]`, understanding that features are additive
- [ ] Understand build profiles (`dev`, `release`, `test`, `bench`) and customize settings like `opt-level`, `debug`, `lto`, and `overflow-checks` in `[profile.*]`
- [ ] Compare Cargo workspaces with Java multi-module projects (Maven/Gradle) and Go workspaces (`go.work`), noting shared lock files and unified builds

## Exercises
- [ ] **Exercise 1 - Workspace setup**: Create a workspace with three members: `shared` (library crate with shared types and logic), `cli` (binary crate depending on `shared`), and `server` (binary crate depending on `shared`). Add a shared struct and function in `shared`, use them from both `cli` and `server`. Run `cargo build` from the workspace root and verify all members compile together.

  > **Starter skeleton**:
  > ```toml
  > # Root Cargo.toml
  > [workspace]
  > members = ["shared", "cli", "server"]
  >
  > # cli/Cargo.toml (similar for server/)
  > [package]
  > name = "cli"
  > version = "0.1.0"
  > edition = "2021"
  >
  > [dependencies]
  > shared = { path = "../shared" }
  > ```
- [ ] **Exercise 2 - Feature flags**: In the `shared` library, add a feature called `verbose` that enables extra debug output. Use `#[cfg(feature = "verbose")]` to conditionally compile a `debug_info()` function. In `cli/Cargo.toml`, depend on `shared` with `features = ["verbose"]` while `server` does not enable it. Verify that `cargo build -p cli` includes the verbose code and `cargo build -p server` does not. Add a `default` feature and practice `default-features = false`.
- [ ] **Exercise 3 - Build profiles** [STRETCH]: In the workspace `Cargo.toml`, configure `[profile.dev]` with `opt-level = 1` and `[profile.release]` with `lto = true`. Build the `cli` crate in both debug and release mode (`cargo build -p cli` vs `cargo build -p cli --release`). Compare the binary sizes. Add a custom profile `[profile.profiling]` that inherits from `release` but keeps `debug = true` for profiling with debug symbols.
- [ ] **Exercise 4 - Workspace-level commands**: Practice running workspace-wide commands: `cargo test --workspace` (runs tests in all members), `cargo clippy --workspace`, `cargo check --workspace`. Then run commands for individual members: `cargo test -p shared`, `cargo run -p cli`. Understand how `Cargo.lock` is shared across the workspace and why this matters for reproducible builds.

## Notes
_Lesson not yet started._
