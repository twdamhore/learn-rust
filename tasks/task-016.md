# Lesson 016: Thinking in ownership - refactoring patterns, borrow checker battles

## Section 3: Ownership System

## Status: pending

## Added
- Initial curriculum design [NEW - bridging lesson]

## Objectives
- [ ] Recognize common ownership patterns: returning owned data from constructors, borrowing in read-only functions, taking `&mut` for modification, consuming `self` for transformations
- [ ] Refactor code from excessive `.clone()` calls to using references - understand when cloning is the right choice (shared ownership boundaries, thread spawning, small data) vs when it signals a design problem
- [ ] Develop a personal strategy for borrow checker battles: start with owned data, introduce references when needed, use the compiler errors as a design guide rather than fighting them
- [ ] Understand the "ownership design" mindset: decide who owns each piece of data at design time, not as an afterthought - contrast with Java (GC decides) and Go (GC + escape analysis)

## Exercises
- [ ] **Refactor 5 snippets**: Fix each of these ownership-broken programs (each is a separate function): (1) a function that builds a String and returns `&str` referencing it, (2) a loop that moves a Vec into a function on each iteration, (3) a struct constructor that takes ownership of a String unnecessarily, (4) code that clones a large Vec just to read the first element, (5) a function that takes `String` as parameter when `&str` would suffice
- [ ] **Build a student registry**: Create a `struct Student { name: String, grades: Vec<u32> }` and a `struct Registry { students: Vec<Student> }`. Implement: `fn add_student(&mut self, student: Student)`, `fn find_student(&self, name: &str) -> Option<&Student>`, `fn add_grade(&mut self, name: &str, grade: u32)`, and `fn highest_average(&self) -> Option<&Student>`. Think carefully about what each method borrows vs owns
- [ ] **Clone elimination**: Start with a working program that uses `.clone()` in 6+ places (e.g., a function that processes a list of names, filters them, groups them by first letter). Progressively eliminate each clone by introducing references, reordering operations, or restructuring - keep a comment for each change explaining the tradeoff
- [ ] **Ownership puzzle challenge**: Implement a function `fn longest_name(names: &[String]) -> &str` that returns a reference to the longest name in a slice. Then implement `fn format_names(names: &[String]) -> String` that joins names with commas. Then combine them: print the longest name and the formatted list using the same input slice, dealing with any borrow issues that arise

## Notes
_**SUPERSEDED**: This lesson has been split into [Lesson 16a](task-016a.md) and [Lesson 16b](task-016b.md). Use those files instead._

_Lesson not yet started._
