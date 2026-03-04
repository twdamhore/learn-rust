# Lesson 109: Processing Pipeline and Validation

## Section 21: Capstone Projects

## Status: pending

## Prerequisites
- Lesson 108 (CLI Tool Setup and Core Processing)

## Added
- Split from lesson 108 (v6 pacing review)

## Objectives
- [ ] Implement the `process` subcommand with a text transformation pipeline: read input, apply transformations, write output
- [ ] Add input validation: verify files exist, config is valid, and provide meaningful error messages for all failure modes
- [ ] Write comprehensive tests: unit tests for individual transformation functions and integration tests for the full pipeline
- [ ] Add progress output for large files using simple `eprintln!` status messages (or optionally `indicatif` for progress bars)

## Exercises
- [ ] **Exercise 1 -- Process subcommand**: Implement the `process` subcommand: read a text file, apply simple text transformations based on config (e.g., uppercase all lines, filter lines containing a keyword, number each line, remove blank lines). Write output to stdout or a file based on a `--output` flag.
- [ ] **Exercise 2 -- Input validation**: Add validation throughout the tool: check that input files exist before processing, validate config file structure (report specific missing/invalid fields), ensure output directory is writable, and provide helpful error messages that suggest fixes (e.g., "File not found: input.txt" -- for the "Did you mean?" suggestion, use a simple hardcoded check like listing files in the same directory and suggesting exact matches with different extensions, NOT fuzzy/Levenshtein matching).
- [ ] **Exercise 3 -- Testing the pipeline**: Write unit tests for each transformation function. Write integration tests that run the full CLI with sample input files and verify output. Use `assert!` and string comparison for output verification. Test error cases (missing file, invalid config, empty input).

## Notes
_Lesson not yet started._
_Split from original lesson 108 which was rated OVERLOADED (~2.5-3.5 hr). This part builds on the project scaffolding from 108._
