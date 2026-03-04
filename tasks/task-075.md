# Lesson 075: FFI - calling C from Rust (extern C, bindgen)

## Section 16: Unsafe & FFI

## Status: pending

## Added
- Initial curriculum design

## Prerequisites
```bash
# Required system packages for bindgen
sudo apt install libclang-dev build-essential
```

## Objectives
- [ ] Use `extern "C"` blocks to declare foreign functions from C libraries and call them from Rust
- [ ] Link to system C libraries using `#[link(name = "...")]` and Cargo build script (`build.rs`) configurations

**What is `build.rs`?** Cargo automatically compiles and runs a file named `build.rs` in your crate root before building your crate. Build scripts are used for code generation, linking native libraries, and setting `cfg` flags. The script communicates with Cargo through `println!("cargo:...")` directives. This is your first encounter with build scripts in this curriculum.
- [ ] Use `bindgen` to automatically generate Rust FFI bindings from C header files
- [ ] Handle C-compatible types: `std::ffi::c_int`, `c_char`, `CString`, `CStr`, and null pointer checks
- [ ] Understand the unsafe boundary at FFI: all foreign function calls are inherently unsafe

## Exercises
- [ ] **Call libc functions**: Use `extern "C"` to declare `abs`, `sqrt`, and `strlen` from libc; call each one from Rust inside `unsafe` blocks; for `strlen`, create a `CString` and pass its `.as_ptr()`; print all results
- [ ] **Bindgen basics**: Write a simple C header file (e.g., `mylib.h` with a struct `Point { int x; int y; }` and a function `int add(int a, int b)`); use `bindgen` in a `build.rs` to generate Rust bindings; include the generated bindings and use the struct and function

  **Starter `build.rs`:**
  ```rust
  // build.rs
  fn main() {
      // Tell Cargo to only re-run this build script if wrapper.h changes.
      println!("cargo:rerun-if-changed=wrapper.h");

      let bindings = bindgen::Builder::default()
          .header("wrapper.h")
          .parse_callbacks(Box::new(bindgen::CargoCallbacks::new()))
          .generate()
          .expect("Unable to generate bindings");

      let out_path = std::path::PathBuf::from(std::env::var("OUT_DIR").unwrap());
      bindings
          .write_to_file(out_path.join("bindings.rs"))
          .expect("Couldn't write bindings!");
  }
  ```

  **Add to `Cargo.toml`:**
  ```toml
  [build-dependencies]
  bindgen = "0.69"
  ```

  **Include the generated bindings in `main.rs` (or `lib.rs`):**
  ```rust
  include!(concat!(env!("OUT_DIR"), "/bindings.rs"));
  ```
- [ ] **Safe wrapper for C function**: Wrap the C `getenv` function in a safe Rust function `fn get_env(key: &str) -> Option<String>` that handles `CString` conversion, null pointer checking, and `CStr`-to-`String` conversion; test with known environment variables like `HOME` and `PATH`
- [ ] **Exercise 4 [STRETCH] -- C string conversions**: Write a module that demonstrates all the C string conversion patterns: `&str` -> `CString` -> `*const c_char` for passing to C; `*const c_char` -> `CStr` -> `&str` for receiving from C; handle the case where C returns a null pointer; handle invalid UTF-8

## Notes
_Lesson not yet started._
