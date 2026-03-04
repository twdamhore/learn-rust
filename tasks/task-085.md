# Lesson 085: CI/CD for Rust - GitHub Actions, caching, release builds

## Section 18: Testing & Quality

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Write a GitHub Actions workflow for a Rust project that runs `cargo test`, `cargo clippy`, and `cargo fmt --check` on every push and pull request
- [ ] Configure dependency caching with `actions/cache` or `Swatinem/rust-cache` to avoid rebuilding all dependencies on every CI run
- [ ] Set up a CI matrix to test against stable, beta, and nightly Rust toolchains, and optionally across multiple OS targets
- [ ] Configure automated release builds that compile optimized binaries and optionally publish to crates.io with `cargo publish`
- [ ] Understand cross-compilation in CI using `cross` or `cargo build --target` for Linux, macOS, and Windows targets

## Exercises
- [ ] **Exercise 1 -- Basic CI workflow**: Write a `.github/workflows/ci.yml` that triggers on push and PR to main. It should: (1) check out code, (2) install Rust stable, (3) run `cargo fmt --check`, (4) run `cargo clippy -- -D warnings`, (5) run `cargo test`. Test it by examining the YAML for correctness. Add `RUSTFLAGS: -D warnings` as an env var to catch all warnings.
- [ ] **Exercise 2 -- Caching and matrix**: Extend the CI workflow to: (1) use `Swatinem/rust-cache` for dependency caching, (2) test on a matrix of `{stable, beta, nightly}` x `{ubuntu-latest, macos-latest}`. Add a `continue-on-error: true` for nightly so nightly failures don't block the pipeline. Document expected cache hit savings.
- [ ] **Exercise 3 -- Release workflow**: Write a `.github/workflows/release.yml` that triggers on git tags matching `v*`. It should: (1) build release binaries for Linux and macOS, (2) create a GitHub Release with the tag, (3) upload the binaries as release assets using `softprops/action-gh-release`. Include `cargo build --release` and strip the binary with `strip` on Linux.
- [ ] **Exercise 4 [OPTIONAL] -- Cross-compilation**: Add a job to the CI workflow that cross-compiles for `x86_64-unknown-linux-musl` (static binary) and `aarch64-unknown-linux-gnu` (ARM64). Use `cross` or install the target with `rustup target add`. Verify the produced binaries are for the correct architecture using `file` command in the workflow.

## Notes
_Lesson not yet started._
