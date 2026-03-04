# Lesson 076a: FFI - Part A: Exposing Rust to C (cdylib, cbindgen)

## Section 16: Unsafe & FFI

## Status: pending

## Added
- Split from lesson 076 (v6 pacing review)

## Prerequisites
```bash
# Required for C compilation
sudo apt install build-essential
# Verify gcc is available
gcc --version
# Install cbindgen for generating C headers from Rust
cargo install cbindgen
```

## Objectives
- [ ] Build a Rust library as a C dynamic library (`cdylib` crate type)
- [ ] Write `extern "C"` functions with `#[no_mangle]` for C-compatible export
- [ ] Use `cbindgen` to auto-generate C header files from Rust source
- [ ] Call the Rust library from a C program, linking against the cdylib

## Exercises
- [ ] **Rust math library as cdylib**: Create a Rust library with `add` and `multiply` as `extern "C"` functions; configure `Cargo.toml` with `crate-type = ["cdylib"]`; build and verify symbols exist with `nm` or `objdump`
- [ ] **cbindgen header generation**: Use `cbindgen` to generate a `.h` header file; write a C program that `#include`s the header, links against the Rust cdylib, and calls the math functions; compile and run the C program

  **gcc compilation commands:**
  ```bash
  # Build the Rust library first
  cargo build --release

  # Compile the C program, linking against the Rust library
  gcc -o main main.c -L target/release -l <your_crate_name> -Wl,-rpath,./target/release

  # Run it
  ./main
  ```

  > **Note:** Replace `<your_crate_name>` with the `lib` name from your Cargo.toml's `[lib]` section (with hyphens replaced by underscores).
- [ ] **String FFI boundary**: Handle strings across the FFI boundary -- write an `extern "C"` function that accepts `*const c_char` and returns `*mut c_char`; use `CString` and `CStr` for safe conversion; document the ownership contract (who allocates, who frees)

## Notes
_Lesson not yet started._
