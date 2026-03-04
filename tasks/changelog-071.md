# Changelog - Lesson 071: Procedural macros - function-like, derive macros

## Section 15: Macros

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Three proc macro types, proc macro crate setup, syn for parsing and quote for codegen, derive macro implementation, TokenStream fundamentals
- **Exercises added**: Derive Hello trait macro, function-like make_getter! proc macro, FieldNames derive macro parsing struct fields, Builder derive macro with quote!

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Overloaded for 1-hour lesson
- **Issues found**:
  - Four proc macros each requiring multi-crate setup is too much for 1 hour
  - Setting up a proc macro crate for the first time takes significant time (separate crate, Cargo.toml, proc_macro2)
  - Builder derive macro (Exercise 4) is essentially a mini-project
  - **Too much content for 1 hour**
- **Recommendations**:
  - Reduce to 2 exercises (derive Hello and FieldNames)
  - Move Builder derive to lesson 072 or make optional

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: OVERLOADED (~2-3 hr) for 1-2 hour target
- **Changes noted**: Most overloaded lesson in 061-080 range. Setting up proc macro crate (separate crate, correct Cargo.toml, proc_macro2 vs proc_macro) is itself time-consuming. 4 exercises each requiring multi-crate setup is untenable. Builder derive (Exercise 4) alone is a mini-project.
- **Why**: 4 proc macros with multi-crate setup in 1 hour is impossible.
- **v4 recommendations status**: Not yet applied -- v4 recommended reducing to 2 exercises and moving Builder to lesson 072 or optional. Gradual progression: CRITICAL -- needs immediate content reduction.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~2-3 hours
- **Pacing verdict**: OVERLOADED - split required
- **Split needed**: Yes - split into 071a/071b
- **Key issues**:
  - 4 proc macros each requiring multi-crate setup
  - Setting up a proc macro crate for the first time takes significant time
  - Builder derive macro (Exercise 4) is a mini-project alone
  - Most overloaded lesson in 061-080 range
- **Action taken**: Split into two lessons:
  - **071a**: "Procedural Macros - Part A: Setup and Derive Macros" -- proc macro crate setup, HelloMacro derive, FieldNames derive (2 exercises)
  - **071b**: "Procedural Macros - Part B: Function-Like and Advanced Derive" -- function-like proc macros, custom syntax parsing, Builder derive as guided exercise (2 exercises)
  - Original task-071.md preserved as-is for reference; new task-071a.md and task-071b.md created

### v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: N/A (already split in v6)
- **Status**: No changes needed
- The v6 split into 071a/071b was already the right call -- no additional changes needed under relaxed threshold

### v8 - Full curriculum pacing review (2026-03-03)
- Original lesson correctly split into 071a/071b at v6. Original was ~2.5-3 hrs.
- **Changes made**: None (split already done)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~150-180 min
- **Pacing**: OVERLOADED
- **Needs split**: No (already split into 071a/071b)
- **Issues**: Most overloaded in 061-080 range. Four proc macros each requiring multi-crate setup was untenable.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: SUPERSEDED by 071a/071b
- **Time estimate**: 150-180 minutes (Overloaded)
- **Needs splitting**: No (already split into 071a/071b at v6)
- **Pacing context**: Original was 2.5-3 hours; correctly split
- **Unresolved from prior reviews**: None (split resolved the overload)
- **New findings**: None
- **Recommendation**: No action on this file; see 071a and 071b changelogs

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: N/A (SUPERSEDED)
- **Needs split**: N/A
- **Progression**: SUPERSEDED by 071a/071b. Split at v6 was correct.
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: None (tracked in 071a/071b)
- **Recommendation**: No action on this file; see changelog-071a.md and changelog-071b.md

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- SUPERSEDED by 071a/071b. No changes to parent.

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: N/A
- **Pacing**: SUPERSEDED
- **Issues**: SUPERSEDED by 071a/071b
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. Correctly superseded by 071a/071b. **Changes**: Changelog only.
