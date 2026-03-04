# Lesson 017: Building with Ownership

## Section 3: Ownership System

## Status: pending

## Added
- Split from task-016 [NEW - bridging lesson] due to overloaded pacing (~3-4 hr)
- Part B focuses on advanced ownership refactoring with structs/methods (~1.5 hr)
- This lesson previews structs and impl blocks (formally taught in lessons 021-022). Follow the provided patterns.

## Objectives
- [ ] Apply ownership thinking to struct design -- prefer owned fields (`String`) for long-lived struct data, and use borrowed parameters (`&str`) in methods when you only need temporary read access
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

        // Clone 3: unnecessary — could iterate by reference
        let to_process = names.clone();
        let mut upper: Vec<String> = Vec::new();
        for name in &to_process {
            upper.push(name.to_uppercase());
        }
        println!("Upper: {:?}", upper);

        println!("Original: {:?}", names);
    }
    ```
- [ ] **Owned vs borrowed API design [OPTIONAL]**: Define `struct Config { name: String, value: String }`. Implement methods showing both ownership and borrowing choices: `fn set_name(&mut self, name: &str)` (borrows input and stores an owned copy), `fn name(&self) -> &str` (returns a borrowed view), and `fn into_name(self) -> String` (consumes the config and returns owned data). Add comments explaining why each signature uses borrow vs ownership.
    ```rust
    struct Config {
        name: String,
        value: String,
    }
    ```

## Notes
- This lesson previews structs and impl blocks (formally taught in lessons 021-022). Follow the provided patterns.
- Exercise 3 intentionally avoids lifetime syntax so you can stay focused on ownership and borrowing decisions.
- The goal is to build intuition for ownership in realistic code, not to master struct syntax.
_Lesson not yet started._
