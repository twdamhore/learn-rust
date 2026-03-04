# Changelog - Lesson 075: Declarative macros - macro_rules!, matchers, repetition

## Section 15: Macros

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: macro_rules! basics, fragment specifiers (expr/ident/ty/tt/etc), repetition patterns, macro hygiene, cargo expand for inspection
- **Exercises added**: Custom my_vec! macro, function generator macro (make_adder!), variadic debug_print! macro with stringify!, cargo expand inspection exercise

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Moderate for 1-hour lesson
- **Issues found**:
  - Requires `cargo-expand` installation for Exercise 4 -- should be noted
- **Recommendations**:
  - Note cargo-expand as a prerequisite installation

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Moderate (~1 hr) for 1-2 hour target
- **Changes noted**: Declarative macros are pattern-matching based, accessible. Exercises build in complexity. cargo-expand (Exercise 4) requires installation
- **Why**: Well-designed with clear progression
- **v4 recommendations status**: Not yet applied -- v4 noted cargo-expand prerequisite. Gradual progression: Good section opener after heavy async

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1 hour
- **Pacing verdict**: Moderate - under 2hr threshold
- **Split needed**: No
- **Key issues**: None (requires cargo-expand installation as tool prerequisite)
- **Action taken**: No changes needed. Good section opener

### v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Moderate (~1 hr)
- **Status**: No changes needed
- Good section opener for macros

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~50-65 min (Moderate)
- **Needs split**: No
- **Progression**: Welcome relief after heavy async block. Well-designed progressive exercises.
- **Issues**: cargo-expand requires nightly toolchain -- should note as prerequisite (flagged since v4).
- **Changes made**: None

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~50-65 min
- **Pacing**: Good
- **Needs split**: No
- **Issues**: cargo-expand requires nightly toolchain (rustup run nightly cargo expand). Should note as prerequisite.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match
- **Time estimate**: 50-65 minutes (Moderate)
- **Needs splitting**: No
- **Pacing context**: Welcome relief after heavy async section. Well-designed progressive exercises. Good macros section opener.
- **Unresolved from prior reviews**: Add note that cargo-expand requires nightly toolchain (`rustup run nightly cargo expand`) (flagged since v4)
- **New findings**: None
- **Recommendation**: Add nightly toolchain prerequisite note when lesson is started

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: ~60min (Moderate)
- **Needs split**: No
- **Progression**: Welcome relief after heavy async section. Good macros section opener.
- **Changelog reconciliation**: "Add cargo-expand nightly note" flagged since v4 — task file Notes section already includes `rustup toolchain install nightly` and `cargo +nightly expand`. Resolved.
- **Genuinely unresolved**: None
- **Recommendation**: No action needed

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 50-65min
- **Pacing**: Good
- **Issues**: None
- **Recommendations**: None
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 65-80min
- **Pacing**: Good
- **Issues**: None
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 60-75min
- **Pacing**: Moderate
- **Issues**: None
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 60-75min. **Pacing**: Moderate. **Issues**: None — good macros section opener. **Changes**: Changelog only.

### v16 (2026-03-04) — Full curriculum review (119 lessons)
- No changes needed — reviewed for pacing, progression, and forward references

### v17 (2026-03-04) — Human-learning clarity pass
- Added a dedicated Prerequisites section for optional `cargo-expand` tooling.
- Softened nightly wording to avoid over-prescribing: use nightly only if stable flow fails for `cargo expand`.
