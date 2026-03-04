# Learn Rust - Zero to Grandmaster

## Project Overview
A structured 119-lesson Rust learning curriculum. Each lesson is ~1-2 hours.
The learner has Java and Go experience but is new to Rust.

## Structure
- `tasks/task-XXX.md` - Individual lesson plans and progress tracking (001-119)
- `tasks/changelog-XXX.md` - Change history for each lesson (001-119)
- Lesson code goes in per-lesson directories: `lessons/lesson-XXX/`
- Each task file tracks: status (pending/in-progress/done), objectives, exercises

## Curriculum Sections (21 sections, 119 lessons)

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

### Section 3: Ownership System (11-17)
11. **[NEW]** Memory in Rust vs Java/Go - why no GC, RAII, the mental model shift
12. Stack vs heap, what ownership is, move semantics
13. Copy vs Clone, when moves happen
14. References and borrowing - `&` and `&mut`
15. Borrowing rules, the borrow checker, common errors
16. **[NEW]** Ownership Patterns and Strategies
17. **[NEW]** Building with Ownership

### Section 4: Strings & Slices (18-20)
18. Slices - string slices, array slices, `&str` vs `String`
19. **[NEW]** Strings Part A - String vs &str, When to Use Which
20. **[NEW]** Strings Part B - UTF-8 and String Manipulation

### Section 5: Structuring Data (21-26)
21. Structs - named, tuple, unit structs
22. Methods and associated functions (`impl` blocks)
23. **[NEW]** The `derive` attribute - Debug, Clone, PartialEq, Eq, Hash
24. Enums - basic, with data, `Option<T>`
25. Pattern matching - `match`, `if let`, `while let`, destructuring
26. Advanced patterns - guards, bindings, nested patterns, `@`

### Section 6: Project Organization (27-30)
27. Modules - `mod`, file structure, visibility (`pub`)
28. Crates, packages, `use`, re-exports, prelude pattern
29. Cargo workspaces, features, profiles
30. Publishing crates, documentation (`///`), `cargo doc`

### Section 7: Error Handling (31-35)
31. Panic, `unwrap`, `expect`, when to panic
32. `Result<T,E>`, the `?` operator, propagation
33. Custom error types, `From` trait, error conversion
34. Error ecosystem - `thiserror`, `anyhow`, best practices
35. **[NEW]** Testing with ownership, Result, and custom types

### Section 8: Collections & Iterators (36-40)
36. `Vec<T>` - creating, updating, accessing, memory model
37. `String` in depth - UTF-8, indexing, manipulation
38. `HashMap`, `HashSet`, `BTreeMap`, entry API
39. Iterators - `Iterator` trait, adaptors, `collect`, chaining
40. Custom iterators, `IntoIterator`, lazy evaluation

### Section 9: Generics & Traits (41-47)
41. Generic functions and structs
42. Traits - defining, implementing, default methods
43. Trait bounds, `where` clauses, `impl Trait` syntax
44. **[NEW]** `impl Trait` in argument vs return position, when to use which
45. Trait objects - `dyn Trait`, vtables, object safety
46. Common std traits - `Display`, `Debug`, `Default`, `From`/`Into`
47. Operator overloading, `Deref`/`DerefMut`, `Drop`

### Section 10: Lifetimes (48-54)
48. What lifetimes are, lifetime annotations `'a`
49. Lifetime elision rules, function lifetimes
50. Struct lifetimes, `'static`, lifetime bounds on generics
51. **[NEW]** Lifetime Practice Part A: Diagnosing Lifetime Errors
52. **[NEW]** Lifetime Practice Part B: Lifetime Design Patterns
53. Higher-Ranked Trait Bounds
54. Variance and Subtyping

### Section 11: Closures & Functional Patterns (55-57)
55. Closures - syntax, capturing, `Fn`/`FnMut`/`FnOnce`
56. `move` closures, closures as parameters and return values
57. Functional patterns - `map`, `filter`, `fold`, method chaining

### Section 12: Smart Pointers & Interior Mutability (58-62)
58. `Box<T>` - heap allocation, recursive types
59. `Rc<T>`, `Arc<T>` - reference counting, shared ownership
60. `RefCell<T>`, `Cell<T>` - interior mutability, runtime borrow checking
61. Smart Pointers Part A - Cow and Weak References
62. Smart Pointers Part B - PhantomData and Type-Level Markers

### Section 13: Concurrency (63-67)
63. Threads - `std::thread`, `move`, `join`, scoped threads
64. Message passing - channels, `mpsc`, patterns
65. Shared state - `Mutex<T>`, `RwLock`, `Arc<Mutex<T>>`
66. `Send` and `Sync` traits, thread safety guarantees
67. Atomics - `AtomicBool`, `AtomicUsize`, ordering, lock-free basics

### Section 14: Async Rust (68-74)
68. Futures, `async fn`, `.await`, what the runtime does
69. Tokio basics - tasks, `spawn`, `select!`, `join!`
70. Async I/O Part A: Files and Timeouts
71. Async I/O Part B: Async Networking
72. Streams, async iterators, async channels
73. The Future Trait and Cancellation
74. Pin, Unpin, and Executor Internals

### Section 15: Macros (75-80)
75. Declarative macros - `macro_rules!`, matchers, repetition
76. **[NEW]** Practical declarative macros - useful patterns, debugging macros
77. Advanced `macro_rules!` - TT munching, push-down accumulation
78. Setup and Derive Macros
79. Function-Like and Advanced Derive
80. Attribute macros, real-world macro patterns

### Section 16: Unsafe & FFI (81-85)
81. Unsafe blocks, raw pointers, dereferencing
82. Unsafe functions, unsafe traits, `unsafe impl`
83. FFI - calling C from Rust (`extern "C"`, `bindgen`)
84. Exposing Rust to C (`cdylib`, `cbindgen`)
85. Exposing Rust to Python (`PyO3`)

### Section 17: Advanced Type System (86-89)
86. Associated types, GATs (generic associated types)
87. Newtype pattern, type aliases, zero-sized types
88. Typestate pattern, builder pattern, RAII in Rust
89. Sealed traits, marker traits, type-level programming

### Section 18: Testing & Quality (90-96)
90. Unit tests in depth - organization, helpers, test modules
91. Integration tests, test fixtures, conditional compilation
92. Property-Based Testing with `proptest`
93. Fuzzing with `cargo-fuzz`
94. Benchmarking Part A: Criterion and Measurement
95. Benchmarking Part B: Profiling and Optimization
96. CI/CD for Rust - GitHub Actions, caching, release builds

### Section 19: Ecosystem & Tooling (97-102)
97. Serde - `Serialize`/`Deserialize`, JSON, TOML, custom
98. Logging and tracing - `log`, `tracing`, structured logging
99. Clap - CLI argument parsing, subcommands, derive API
100. Networking - `reqwest`, `hyper`, raw TCP/UDP
101. Database Part A - SQLite Setup, Migrations, and Queries
102. Database Part B - CRUD, Testing, and Repository Pattern

### Section 20: Special Targets (103-107)
103. `no_std` - embedded basics, `core` vs `std`
104. Rust to WASM Basics
105. Browser Integration
106. Cross-compilation, conditional compilation, `cfg` attributes
107. Memory layout - `repr`, alignment, size optimization

### Section 21: Capstone Projects (108-119)
108. Project 1 - CLI Tool Setup and Core Processing
109. Project 1 - Processing Pipeline and Validation
110. Project 1 - Testing the CLI Tool
111. Project 1 - Documentation, CI, and Publishing
112. Project 2 - Axum Web API Basics
113. Project 2 - Database and Authentication
114. Project 2 - Async Patterns and Observability
115. Project 2 - Testing and Deployment
116. Project 3 - Architecture and Core Implementation
117. Project 3 - Completion and Polish
118. Project 3 - Benchmarking and Optimization
119. Project 3 - Polish and Retrospective

## Bridging Lessons Added (v2 revision)
10 lessons were added after reviewing the original 90-lesson plan for gaps:
- **003** - Dev tooling (clippy/rustfmt) moved to day 1 instead of lesson 83
- **010** - Basic testing introduced early instead of waiting until lesson 78
- **011** - Memory model bridge for Java/Go developers before ownership
- **016-017** - Ownership practice before moving on to new topics
- **019-020** - String deep-dive before structs (biggest pain point from Java/Go)
- **023** - derive basics (used everywhere, previously not taught until macros)
- **035** - Testing with real types after error handling
- **044** - impl Trait clarity before trait objects
- **051-052** - Lifetime practice before advanced lifetimes
- **076** - Practical macros bridge before TT munching

## Conventions
- Always run `cargo check` and `cargo clippy` on lesson code
- Each lesson builds on previous ones - complete in order
- Exercises should be attempted before looking at solutions
- File naming: 3-digit zero-padded (task-001.md, lesson-001/)
