# Changelog - Lesson 004: Hello World, println!, formatting, comments, basic I/O

## Section 1: Getting Started

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: fn main() entry point; println!/eprintln! with format specifiers ({}, {:?}, {:#?}, padding); comment styles (// and ///); read stdin with read_line and .expect(); parse strings to numeric types
- **Exercises added**: Format string showcase with 6+ specifiers; echo program with line numbers and stderr summary; temperature converter with input parsing and error messages; self-documenting code with doc comments and cargo doc

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Moderate-to-Heavy for 1-hour lesson
- **Issues found**:
  - Introduces `.expect()` and `match` on `Result` from `.parse()` before error handling is formally taught (lessons 29-33)
  - Temperature converter (Exercise 3) involves reading input, parsing, matching, and formatting -- a lot for lesson 4
  - Exercise 4 (`cargo doc` with doc comments and `# Examples`) is advanced for a 'Getting Started' lesson
- **Recommendations**:
  - Mark `.expect()` and `match` usage as 'follow the pattern for now, explained fully in lesson 29-30'
  - Consider making Exercise 4 (cargo doc) optional or lighter

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Moderate-to-Heavy (~1-1.5 hr) for 1-2 hour target
- **Changes noted**: Temperature converter (Exercise 3) requires stdin reading, parsing, match on Result, and formatting -- too much for lesson 4. Exercise 4 (cargo doc) premature for "Getting Started." Forward references to error handling (.expect(), match on Result).
- **Why**: Lesson tries to cover formatting + I/O + parsing + error patterns + docs simultaneously.
- **v4 recommendations status**: Not yet applied -- v4 recommended marking Exercise 4 optional and adding "follow the pattern" notes. Gradual progression: Slight spike from lessons 1-3; consider simplifying Exercise 3.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1-1.5 hr
- **Pacing verdict**: Moderate-Heavy
- **Split needed**: No
- **Key issues**:
  - Temperature converter too complex for lesson 4
  - Forward references to error handling (.expect, match on Result)
- **Action taken**: Changelog updated

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Moderate-Heavy (~1-1.5 hr)
- **Status**: No changes needed
- Forward reference issues (expect, match on Result) still flagged from v4 but within 2hr limit

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~60-90 min (Moderate-Heavy)
- **Needs split**: No
- **Progression**: Noticeable spike from lessons 1-3. Five sub-topics is the most in Section 1.
- **Issues**: Forward references to .expect() and match on Result need "follow the pattern for now" annotations (flagged since v4, unresolved). Exercise 4 (cargo doc) could be marked optional.
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~60-90 min
- **Pacing**: Good (upper end)
- **Needs split**: No
- **Issues**: Forward references to .expect() and match on Result (lessons 29-30). Exercise 4 (cargo doc) advanced for lesson 4. Both unresolved since v4.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Good match with issues
- **Time estimate**: 60-90 minutes (Heavy-Moderate)
- **Needs splitting**: No (all under 2 hours)
- **Pacing context**: Noticeable spike from lessons 1-3; heaviest in Section 1
- **Unresolved from prior reviews**: (1) Forward refs to .expect()/match on Result need "preview" annotations, (2) Exercise 4 should be marked [STRETCH/OPTIONAL] (both flagged since v4, never applied)
- **New findings**: None beyond prior reviews
- **Recommendation**: Add "preview -- explained fully in lesson 29-30" notes and mark Exercise 4 optional before starting

## v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 60-90min (Moderate-Heavy)
- **Needs split**: No
- **Progression**: Heaviest in Section 1 but within 2hr limit
- **Changelog reconciliation**: (1) Exercise 4 "should be [OPTIONAL]" flagged since v4 — already applied in task file. Resolved. (2) Forward references to Result/match "need preview note" — task file already has `> **Preview**` note. Resolved.
- **Genuinely unresolved**: Temperature converter (Ex 3) could benefit from a `read_line`/`parse` hint
- **Recommendation**: Ready as-is; consider adding a hint to Ex 3 at lesson time

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 60-90min
- **Pacing**: Heavy
- **Issues**: Temperature converter (Ex 3) ambitious for lesson 4 — could use read_line/parse hint
- **Recommendations**: Add code snippet showing read_line → trim → parse pattern before Ex 3
- **Changes made**: Changelog updated only

### v13-fix - Applied pending fixes (2026-03-04)
- Added `read_line`/`parse` hint scaffolding to Exercise 3 (temperature converter)
- **Why**: Complex input pattern for lesson 4; learners need the read_line -> trim -> parse template
- **Resolves**: v11/v12 recommendation

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 75-90min
- **Pacing**: Good (borderline Heavy)
- **Issues**: Exercise 2 uses loop/break/&mut/String::new() all untaught at this point — needs more scaffolding code
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 70-95min
- **Pacing**: Heavy
- **Issues**: Exercise 2 needed scaffolding code for the stdin reading loop
- **Changes made**: Task file updated — added complete BufRead/lines() starter template to Exercise 2 with explanatory note about untaught concepts

### v15 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, progression, and content quality
- **Estimated time**: 70-95min
- **Pacing**: Heavy
- **Issues**: Exercise 2 scaffolding heavy but well-framed as template to focus on formatting
- **Changes made**: Changelog updated only
