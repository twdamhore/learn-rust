# Lesson 016b: Thinking in Ownership - Part B: Building with Ownership

## Section 3: Ownership System

## Status: pending

## Added
- Split from task-016 [NEW - bridging lesson] due to overloaded pacing (~3-4 hr)
- Part B focuses on advanced ownership refactoring with structs/methods (~1.5 hr)
- This lesson previews structs and impl blocks (formally taught in lessons 19-20). Follow the provided patterns.

## Objectives
- [ ] Apply ownership thinking to struct design -- decide which fields should be owned (`String`) vs borrowed (`&str`) and understand the tradeoffs
- [ ] Choose the correct self receiver for methods: `&self` for read-only access, `&mut self` for mutation, `self` for consumption/transformation
- [ ] Recognize clone-heavy code and systematically reduce unnecessary clones by replacing them with borrows or restructuring

## Exercises
- [ ] **Build a simple Library**: Create a `struct Library { books: Vec<String> }` with two methods: `fn add_book(&mut self, title: String)` that adds a book, and `fn has_book(&self, title: &str) -> bool` that checks if a book exists. Note how `add_book` takes ownership of the `String` (it will be stored) while `has_book` only borrows the title for comparison. Use the following pattern for the impl block:
    ```rust
    struct Library {
        books: Vec<String>,
    }

    impl Library {
        fn new() -> Library {
            Library { books: Vec::new() }
        }

        fn add_book(&mut self, title: String) {
            // your code here
        }

        fn has_book(&self, title: &str) -> bool {
            // your code here
        }
    }
    ```
- [ ] **Clone elimination**: Given working code with 3 unnecessary `.clone()` calls (provided below), identify each unnecessary clone and replace it with a borrow. For each change, add a comment explaining why the clone was unnecessary. The code will involve functions that pass owned Strings where `&str` would suffice, and variables that are cloned just to print them.
    ```rust
    fn main() {
        let names = vec![
            String::from("Alice"),
            String::from("Bob"),
            String::from("Charlie"),
        ];

        // Clone 1: unnecessary — could use a reference
        let first = names[0].clone();
        println!("First: {}", first);

        // Clone 2: unnecessary — only reading, not modifying
        let all_names = names.clone();
        for name in &all_names {
            println!("Name: {}", name);
        }

        // Clone 3: unnecessary — could take a slice
        // Note: This uses iterator/closure syntax (`iter().map(|n| ...).collect()`) —
        // for now, treat it as a pattern that converts each element. These are covered
        // in lessons 37 and 51.
        let to_process = names.clone();
        let upper: Vec<String> = to_process.iter().map(|n| n.to_uppercase()).collect();
        println!("Upper: {:?}", upper);

        println!("Original: {:?}", names);
    }
    ```
- [ ] **Config vs ConfigView [OPTIONAL]**: Design two approaches to a configuration holder: (1) `struct Config { name: String, value: String }` that owns its data, and (2) `struct ConfigView<'a> { name: &'a str, value: &'a str }` that borrows from an existing Config. Write a function that creates a Config and then creates a ConfigView referencing it. Observe what happens if you try to drop the Config while the ConfigView is still alive. Use the following patterns:
    ```rust
    struct Config {
        name: String,
        value: String,
    }

    struct ConfigView<'a> {
        name: &'a str,
        value: &'a str,
    }
    ```
    Note: Lifetime annotations (`'a`) are formally taught in lesson 46. For now, just follow the pattern -- the `'a` means "this struct borrows data that must live at least as long as the struct does."

## Notes
- This lesson previews structs and impl blocks (formally taught in lessons 19-20). Follow the provided patterns.
- Lifetime annotations in Exercise 3 are a preview of lesson 46. Just follow the pattern for now.
- The goal is to build intuition for ownership in realistic code, not to master struct syntax.
_Lesson not yet started._
