# Lesson 088: Clap - CLI argument parsing, subcommands, derive API

## Section 19: Ecosystem & Tooling

## Status: pending

## Prerequisites
- Lesson 086 (serde) — Exercise 2 uses serde/JSON for task persistence.

## Added
- Initial curriculum design

## Objectives
- [ ] Parse command-line arguments using clap's derive API (`#[derive(Parser)]`) and understand the struct-as-schema approach compared to Go's `flag` package or cobra
- [ ] Define subcommands using `#[derive(Subcommand)]` enums, mirroring how tools like `git` and `cargo` have subcommands (e.g., `mytool add`, `mytool list`)
- [ ] Use clap's argument types, validation, and constraints: positional args, `--flag` options, `#[arg(short, long)]`, `value_parser`, `default_value`, `required`, `conflicts_with`
- [ ] Generate `--help` text automatically from doc comments and struct attributes, and generate shell completions for bash/zsh/fish using `clap_complete`
- [ ] Compare clap's derive API to Go's cobra/flag pattern and appreciate the compile-time type safety of the Rust approach

## Exercises
- [ ] **Exercise 1 -- Basic CLI tool**: Build a `file-stats` CLI that takes a required positional `<PATH>` argument and optional `--lines` / `--words` / `--bytes` boolean flags (all default to true if none specified). Use `#[derive(Parser)]` with doc comments for help text. Parse args and print the requested statistics for the file. Handle file-not-found errors gracefully.
- [ ] **Exercise 2 -- Subcommands**: Create a `task-manager` CLI with subcommands: `add <TITLE> [--priority <low|medium|high>]` and `list [--filter <STATUS>]`. Use `#[derive(Subcommand)]` for the enum. Store tasks in a JSON file using serde (connecting to lesson 086). Implement both subcommands end-to-end.
- [ ] **Exercise 3 -- Validation and constraints**: Extend the task-manager with input validation: `--priority` must be one of `low/medium/high` (use an enum with `ValueEnum`), `<ID>` must be a positive integer (use `value_parser!(u32)`), add `--before <DATE>` and `--after <DATE>` filters to `list` that parse dates. Add `conflicts_with` so `--all` and `--filter` cannot be used together. Test that invalid input produces clear error messages.
- [ ] **Exercise 4 [STRETCH] -- Shell completions**: Add a hidden `completions` subcommand that generates shell completion scripts using `clap_complete`. Generate completions for bash and zsh. Install the bash completions in your shell and verify that tab-completion works for subcommands and `--flags`. Document the steps needed for a user to install completions.

## Notes
_Lesson not yet started._
