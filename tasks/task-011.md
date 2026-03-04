# Lesson 011: Memory in Rust vs Java/Go - why no GC, RAII, the mental model shift

## Section 3: Ownership System

## Status: pending

## Added
- Initial curriculum design [NEW - bridging lesson]

## Objectives
- [ ] Understand why Rust has no garbage collector by contrasting Java's GC (stop-the-world, generational collection) and Go's GC (concurrent, tri-color mark-and-sweep) with Rust's compile-time ownership model
- [ ] Understand RAII (Resource Acquisition Is Initialization) - values are automatically cleaned up when they go out of scope via the `Drop` trait, similar to Java's try-with-resources but for everything
- [ ] Grasp the stack vs heap mental model - know which data goes where and why heap allocation requires ownership tracking
- [ ] Understand what problems ownership solves: use-after-free, double-free, dangling pointers, and data races - all caught at compile time with zero runtime cost
- [ ] See how Rust's `drop` ordering works - values are dropped in reverse declaration order, struct fields in declaration order

## Exercises
> **Tip**: Read through all objectives above before starting the exercises — the mental model concepts in the objectives will make the hands-on exercises much clearer.

- [ ] **Memory model diagram**: Draw (on paper or in comments) the memory layout for a Java `new ArrayList<String>()` vs a Rust `Vec<String>` - annotate where the GC root / owner lives, where heap data lives, and what happens at cleanup time
- [ ] **RAII in action**: Write a Rust program that opens a file (using `std::fs::File::create`), writes to it, and lets it go out of scope - verify the file is properly closed without explicit `.close()`. Then write a custom struct with a `Drop` implementation that prints when it's dropped, and observe drop order with multiple variables

  > **Note**: The `impl Drop for TypeName` syntax is a trait implementation — covered fully in lesson 40. For now, just follow the template below exactly.

  > **Note**: `File::create` returns a `Result`. Use `.expect()` to handle it for now. `Result` and error handling are covered in lessons 29-30.

  ```rust
  // File::create returns a Result. Use .expect() to handle it for now.
  // Result and error handling are covered in lessons 29-30.
  let file = std::fs::File::create("test.txt").expect("failed to create file");
  ```

  ```rust
  struct MyStruct {
      name: String,
  }

  impl Drop for MyStruct {
      fn drop(&mut self) {
          println!("Dropping {}!", self.name);
      }
  }
  ```
- [ ] **Drop order exploration**: Reuse the `MyStruct` template from Exercise 2 — create three instances (`MyStruct { name: String::from("A") }`, `"B"`, `"C"`) in one function and verify they drop in reverse order C, B, A. Then put them in a Vec and observe the difference
- [ ] **Compile-time safety comparison**: Write a Rust program that creates a `String`, transfers it to another variable, and try to use the original - read the compiler error. Write the equivalent Java code (where this "just works" via GC) and the equivalent Go code (where this copies or shares via pointer) as comments, explaining the tradeoff each language makes

## Notes
_Lesson not yet started._
