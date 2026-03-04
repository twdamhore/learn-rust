# Lesson 106: Cross-compilation, conditional compilation, cfg attributes

## Section 20: Special Targets

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Understand target triples (e.g., `x86_64-unknown-linux-gnu`, `aarch64-apple-darwin`) and how to add cross-compilation targets with `rustup target add`
- [ ] Use `#[cfg(...)]` attributes for conditional compilation: `target_os`, `target_arch`, `target_family`, `feature`, `test`, and `debug_assertions` -- and understand how this differs from Go's build tags
- [ ] Use the `cfg!()` macro for runtime checks vs `#[cfg()]` for compile-time code elimination, understanding when to use each
- [ ] Organize platform-specific code using `cfg` on modules, functions, and entire files (e.g., `#[cfg(unix)] mod unix_impl;`)
- [ ] Use Cargo features to enable optional dependencies and conditional code paths, defining features in `Cargo.toml` and gating code with `#[cfg(feature = "...")]`

## Exercises
- [ ] **Exercise 1 - Cross-Compilation**: Install a cross-compilation target (e.g., `wasm32-unknown-unknown` or a different architecture if available) with `rustup target add`, then cross-compile a simple hello-world binary and inspect the output with `file` to verify the target architecture
- [ ] **Exercise 2 - Platform-Specific Config Dirs**: Write a module that provides a `get_config_dir() -> PathBuf` function using `#[cfg(target_os = "linux")]`, `#[cfg(target_os = "macos")]`, and `#[cfg(target_os = "windows")]` to return the OS-appropriate configuration directory -- use `cfg!(target_os = "...")` in a fallback to print a warning at runtime
- [ ] **Exercise 3 - Feature-Gated Serialization**: Create a library crate with a `serde` Cargo feature (not enabled by default) that optionally depends on `serde` and `serde_json` -- when the feature is enabled, derive `Serialize`/`Deserialize` on your types using `#[cfg_attr(feature = "serde", derive(Serialize, Deserialize))]` and provide a `to_json`/`from_json` function; write tests that run with `--features serde` to verify serialization works, and tests without the feature to verify the library still compiles and functions without serde

  > **Note**: Lesson 091 Exercise 3 used simple boolean feature flags (`#[cfg(feature = "verbose")]`). This exercise goes further: the feature controls an **optional dependency** (`serde`), uses `cfg_attr` for **conditional derives**, and provides **feature-gated public API** (`to_json`/`from_json`) -- a real-world pattern used by crates like `uuid`, `chrono`, and `time`.
- [ ] **Exercise 4 - Debug vs Release Instrumentation**: Write a program that uses `#[cfg(debug_assertions)]` to include verbose debug logging and timing instrumentation, then compile in both debug and release modes and compare the output -- also use `#[cfg(test)]` to include test helper functions that are excluded from the final binary

## Notes
_Lesson not yet started._
