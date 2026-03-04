# Lesson 079: Typestate pattern, builder pattern, RAII in Rust

## Section 17: Advanced Type System

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Implement the typestate pattern to encode state machines in the type system so that invalid state transitions are caught at compile time rather than runtime
- [ ] Build the builder pattern for constructing complex structs, including required vs optional fields and compile-time enforcement of required fields using typestate
- [ ] Understand RAII (Resource Acquisition Is Initialization) in Rust and how `Drop` enables deterministic cleanup -- compare to Java's try-with-resources and Go's `defer`
- [ ] Combine typestate with generics so state transitions return a new type (e.g., `Connection<Disconnected>` -> `Connection<Connected>`) and methods are only available in the correct state

## Exercises
- [ ] **Exercise 1 -- Typestate connection**: Build a `TcpConnection` that uses typestate to enforce `Disconnected -> Connected -> Authenticated` transitions. `connect()` is only available on `Disconnected`, `authenticate()` only on `Connected`, and `send_data()` only on `Authenticated`. Verify that calling methods in the wrong order fails to compile.
- [ ] **Exercise 2 -- Builder with required fields**: Implement a builder for a `DatabaseConfig` struct with required fields (`host`, `port`, `database`) and optional fields (`username`, `password`, `max_connections`). Use typestate generics so that `build()` is only available after all required fields are set. Compare this to a runtime-validated builder that returns `Result`.

  **Scaffold — typestate builder with per-field generic parameters:**
  ```rust
  // Marker types for tracking which fields have been set
  struct Set;
  struct Unset;

  // Builder with generic parameters tracking required field status
  struct DatabaseConfigBuilder<Host = Unset, Port = Unset, DbName = Unset> {
      host: Option<String>,
      port: Option<u16>,
      db_name: Option<String>,
      // PhantomData or direct generics to track state
      _host: std::marker::PhantomData<Host>,
      _port: std::marker::PhantomData<Port>,
      _db_name: std::marker::PhantomData<DbName>,
  }

  // Start with all fields Unset
  impl DatabaseConfigBuilder {
      fn new() -> DatabaseConfigBuilder<Unset, Unset, Unset> {
          DatabaseConfigBuilder {
              host: None, port: None, db_name: None,
              _host: std::marker::PhantomData,
              _port: std::marker::PhantomData,
              _db_name: std::marker::PhantomData,
          }
      }
  }

  // Setting host transitions Host from Unset to Set
  impl<Port, DbName> DatabaseConfigBuilder<Unset, Port, DbName> {
      fn host(self, host: impl Into<String>) -> DatabaseConfigBuilder<Set, Port, DbName> {
          // Your implementation: construct a new builder with Set for Host
          todo!()
      }
  }

  // build() is only available when ALL required fields are Set
  impl DatabaseConfigBuilder<Set, Set, Set> {
      fn build(self) -> DatabaseConfig {
          // All fields guaranteed to be set at compile time!
          todo!()
      }
  }
  ```

  > **Note:** This scaffold shows the pattern. Your task: complete the implementation for all three setters and the build method. The key insight is that each setter changes one generic parameter from `Unset` to `Set`, and `build()` is only callable when all three are `Set`.
- [ ] **Exercise 3 -- RAII guard**: Create a `Timer` struct that records the start time on creation and prints the elapsed duration when dropped. Use it to time blocks of code. Then create a `TempFile` RAII guard that creates a temporary file on construction and deletes it on drop, even if a panic occurs. Compare to Go's `defer`.

  Useful APIs: For `Timer`, use `std::time::Instant::now()` and `instant.elapsed()`. For `TempFile`, use `std::fs::File::create(path)` to create and `std::fs::remove_file(path)` to delete. Rust's `Drop` trait runs during stack unwinding, so your cleanup will execute even if a panic occurs.
- [ ] **Exercise 4 [STRETCH] -- Typestate file handle**: Implement a `File<State>` wrapper where `State` is one of `Closed`, `OpenRead`, `OpenWrite`. Opening for read returns `File<OpenRead>` (with `read()` method), opening for write returns `File<OpenWrite>` (with `write()` method), and `close()` consumes the file and returns `File<Closed>`. Ensure you cannot read from a write-mode file or vice versa at compile time.

## Notes
_Lesson not yet started._
