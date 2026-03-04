# Learn Rust - Zero to Grandmaster

## Project Overview
A structured 100-lesson Rust learning curriculum. Each lesson is ~1 hour.
The learner has Java and Go experience but is new to Rust.

## Structure
- `tasks/task-XXX.md` - Individual lesson plans and progress tracking (001-100)
- `tasks/changelog-XXX.md` - Change history for each lesson (001-100)
- Lesson code goes in per-lesson directories: `lessons/lesson-XXX/`
- Each task file tracks: status (pending/in-progress/done), objectives, exercises

## Curriculum Sections (21 sections, 100 lessons)

### Section 1: Getting Started (1-4)
1. Installing Rust, toolchain overview (rustup, rustc, cargo)
2. Cargo deep dive - new, build, run, check, project structure
3. **[NEW]** Clippy, rustfmt, rust-analyzer - setting up your dev workflow
4. Hello World, println!, formatting, comments, basic I/O

### Section 2: Language Basics (5-10)
5. Variables, mutability, constants, shadowing
6. Scalar types - integers, floats, bool, char, casting with `as`
7. Compound types - tuples, arrays, ranges
8. Functions, parameters, return values, expressions vs statements
9. Control flow - if/else, loop, while, for, labels, break with values
10. **[NEW]** Writing and running tests - `#[test]`, `assert!`, `cargo test`

### Section 3: Ownership System (11-16)
11. **[NEW]** Memory in Rust vs Java/Go - why no GC, RAII, the mental model shift
12. Stack vs heap, what ownership is, move semantics
13. Copy vs Clone, when moves happen
14. References and borrowing - `&` and `&mut`
15. Borrowing rules, the borrow checker, common errors
16. **[NEW]** Thinking in ownership - refactoring patterns, borrow checker battles

### Section 4: Strings & Slices (17-18)
17. Slices - string slices, array slices, `&str` vs `String`
18. **[NEW]** Strings in Rust for Java/Go devs - String, &str, when to use which

### Section 5: Structuring Data (19-24)
19. Structs - named, tuple, unit structs
20. Methods and associated functions (`impl` blocks)
21. **[NEW]** The `derive` attribute - Debug, Clone, PartialEq, Eq, Hash
22. Enums - basic, with data, `Option<T>`
23. Pattern matching - `match`, `if let`, `while let`, destructuring
24. Advanced patterns - guards, bindings, nested patterns, `@`

### Section 6: Project Organization (25-28)
25. Modules - `mod`, file structure, visibility (`pub`)
26. Crates, packages, `use`, re-exports, prelude pattern
27. Cargo workspaces, features, profiles
28. Publishing crates, documentation (`///`), `cargo doc`

### Section 7: Error Handling (29-33)
29. Panic, `unwrap`, `expect`, when to panic
30. `Result<T,E>`, the `?` operator, propagation
31. Custom error types, `From` trait, error conversion
32. Error ecosystem - `thiserror`, `anyhow`, best practices
33. **[NEW]** Testing with ownership, Result, and custom types

### Section 8: Collections & Iterators (34-38)
34. `Vec<T>` - creating, updating, accessing, memory model
35. `String` in depth - UTF-8, indexing, manipulation
36. `HashMap`, `HashSet`, `BTreeMap`, entry API
37. Iterators - `Iterator` trait, adaptors, `collect`, chaining
38. Custom iterators, `IntoIterator`, lazy evaluation

### Section 9: Generics & Traits (39-45)
39. Generic functions and structs
40. Traits - defining, implementing, default methods
41. Trait bounds, `where` clauses, `impl Trait` syntax
42. **[NEW]** `impl Trait` in argument vs return position, when to use which
43. Trait objects - `dyn Trait`, vtables, object safety
44. Common std traits - `Display`, `Debug`, `Default`, `From`/`Into`
45. Operator overloading, `Deref`/`DerefMut`, `Drop`

### Section 10: Lifetimes (46-50)
46. What lifetimes are, lifetime annotations `'a`
47. Lifetime elision rules, function lifetimes
48. Struct lifetimes, `'static`, lifetime bounds on generics
49. **[NEW]** Lifetime practice - common errors, fixing lifetime puzzles
50. Advanced lifetimes - HRTBs, variance, subtyping

### Section 11: Closures & Functional Patterns (51-53)
51. Closures - syntax, capturing, `Fn`/`FnMut`/`FnOnce`
52. `move` closures, closures as parameters and return values
53. Functional patterns - `map`, `filter`, `fold`, method chaining

### Section 12: Smart Pointers & Interior Mutability (54-57)
54. `Box<T>` - heap allocation, recursive types
55. `Rc<T>`, `Arc<T>` - reference counting, shared ownership
56. `RefCell<T>`, `Cell<T>` - interior mutability, runtime borrow checking
57. `Cow<T>`, `Weak` references, `Pin<T>`, `PhantomData`

### Section 13: Concurrency (58-62)
58. Threads - `std::thread`, `move`, `join`, scoped threads
59. Message passing - channels, `mpsc`, patterns
60. Shared state - `Mutex<T>`, `RwLock`, `Arc<Mutex<T>>`
61. `Send` and `Sync` traits, thread safety guarantees
62. Atomics - `AtomicBool`, `AtomicUsize`, ordering, lock-free basics

### Section 14: Async Rust (63-67)
63. Futures, `async fn`, `.await`, what the runtime does
64. Tokio basics - tasks, `spawn`, `select!`, `join!`
65. Async I/O - files, networking, timers
66. Streams, async iterators, async channels
67. Advanced async - `Pin`/`Unpin` in depth, writing a mini executor, cancellation

### Section 15: Macros (68-72)
68. Declarative macros - `macro_rules!`, matchers, repetition
69. **[NEW]** Practical declarative macros - useful patterns, debugging macros
70. Advanced `macro_rules!` - TT munching, push-down accumulation
71. Procedural macros - function-like, derive macros
72. Attribute macros, real-world macro patterns

### Section 16: Unsafe & FFI (73-76)
73. Unsafe blocks, raw pointers, dereferencing
74. Unsafe functions, unsafe traits, `unsafe impl`
75. FFI - calling C from Rust (`extern "C"`, `bindgen`)
76. FFI - exposing Rust to C/Python, `cbindgen`, `PyO3`

### Section 17: Advanced Type System (77-80)
77. Associated types, GATs (generic associated types)
78. Newtype pattern, type aliases, zero-sized types
79. Typestate pattern, builder pattern, RAII in Rust
80. Sealed traits, marker traits, type-level programming

### Section 18: Testing & Quality (81-85)
81. Unit tests in depth - organization, helpers, test modules
82. Integration tests, test fixtures, conditional compilation
83. Property-based testing (`proptest`), fuzzing (`cargo-fuzz`)
84. Benchmarking - `criterion`, profiling, flamegraphs
85. CI/CD for Rust - GitHub Actions, caching, release builds

### Section 19: Ecosystem & Tooling (86-90)
86. Serde - `Serialize`/`Deserialize`, JSON, TOML, custom
87. Logging and tracing - `log`, `tracing`, structured logging
88. Clap - CLI argument parsing, subcommands, derive API
89. Networking - `reqwest`, `hyper`, raw TCP/UDP
90. Database - `sqlx`, connection pools, migrations

### Section 20: Special Targets (91-94)
91. `no_std` - embedded basics, `core` vs `std`
92. WebAssembly - `wasm-pack`, `wasm-bindgen`, browser integration
93. Cross-compilation, conditional compilation, `cfg` attributes
94. Memory layout - `repr`, alignment, size optimization

### Section 21: Capstone Projects (95-100)
95. Project 1 - CLI tool (file processor with clap, serde, error handling)
96. Project 1 - continued (testing, publishing)
97. Project 2 - Web API (axum, sqlx, auth, middleware)
98. Project 2 - continued (async patterns, deployment)
99. Project 3 - Systems tool (async runtime piece OR parser OR custom data structure)
100. Project 3 - continued (unsafe where needed, optimization, benchmarks)

## Bridging Lessons Added (v2 revision)
10 lessons were added after reviewing the original 90-lesson plan for gaps:
- **003** - Dev tooling (clippy/rustfmt) moved to day 1 instead of lesson 75
- **010** - Basic testing introduced early instead of waiting until lesson 71
- **011** - Memory model bridge for Java/Go developers before ownership
- **016** - Ownership practice before moving on to new topics
- **018** - String deep-dive before structs (biggest pain point from Java/Go)
- **021** - derive basics (used everywhere, previously not taught until macros)
- **033** - Testing with real types after error handling
- **042** - impl Trait clarity before trait objects
- **049** - Lifetime practice before advanced lifetimes
- **069** - Practical macros bridge before TT munching

## Conventions
- Always run `cargo check` and `cargo clippy` on lesson code
- Each lesson builds on previous ones - complete in order
- Exercises should be attempted before looking at solutions
- File naming: 3-digit zero-padded (task-001.md, lesson-001/)
