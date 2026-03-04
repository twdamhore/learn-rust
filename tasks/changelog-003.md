# Changelog - Lesson 003: Clippy, rustfmt, rust-analyzer - setting up your dev workflow

## Section 1: Getting Started

### v1 - Initial creation
- Lesson added to curriculum
- **NEW**: Bridging lesson added after gap analysis

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and bridging lesson tag all align with curriculum
- Correctly tagged as [NEW - bridging lesson] matching CLAUDE.md [NEW] designation
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Run cargo clippy and understand its linter role; clippy lint levels and configuration; set up rustfmt with custom config; configure rust-analyzer in editor; understand the dev feedback loop
- **Exercises added**: Trigger and fix 4+ clippy warnings on intentional bad code; create rustfmt.toml with custom settings and format code; experiment with allow/deny/warn lint levels and pedantic mode; verify rust-analyzer IDE features (hover, diagnostics, go-to-def, autocomplete)

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Moderate for 1-hour lesson
- **Issues found**:
  - Exercise 1 asks learner to trigger 4 clippy warnings using idiomatic patterns not yet taught, though concrete examples are provided
  - Exercise 4 (IDE verification) is environment-dependent and may take variable time
- **Recommendations**:
  - Ensure Exercise 1 provides all code patterns verbatim since the learner has not yet internalized idiomatic Rust

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Moderate (~1 hr) with variability for 1-2 hour target
- **Changes noted**: Exercise 1 asks learner to write bad code triggering clippy warnings, but they barely know Rust syntax at lesson 3. Exercise 4 (IDE setup) timing is unpredictable.
- **Why**: Dev tooling early is good, but exercises need to match current knowledge.
- **v4 recommendations status**: Not yet applied -- v4 recommended providing verbatim code for Exercise 1. Gradual progression: Good placement; tooling early prevents bad habits.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~45-75 min
- **Pacing verdict**: Moderate (variable)
- **Split needed**: No
- **Key issues**:
  - Exercise 1 asks learner to trigger clippy warnings before knowing Rust syntax
- **Action taken**: Changelog updated

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Moderate (~45-75 min)
- **Status**: No changes needed
- Note: v4 clippy syntax issue still unfixed but acceptable

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~45-80 min (Moderate with variability)
- **Needs split**: No
- **Progression**: Good placement -- tooling early prevents bad habits.
- **Issues**: Exercise 1 still needs verbatim code blocks for clippy exercise (flagged since v4, unresolved). Learner can't write intentionally bad code when they barely know Rust syntax.
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~45-80 min
- **Pacing**: Good
- **Needs split**: No
- **Issues**: Exercise 1 asks learner to write "intentionally poor code" but they barely know Rust syntax at lesson 3. Should provide verbatim starter code. Unresolved since v4.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Good match with issues
- **Time estimate**: 45-80 minutes (Moderate)
- **Needs splitting**: No (all under 2 hours)
- **Pacing context**: Good early placement; tooling before bad habits form
- **Unresolved from prior reviews**: Exercise 1 needs verbatim starter code -- learner cannot write "intentionally poor code" at lesson 3 (flagged since v4, never applied to task file)
- **New findings**: None beyond prior reviews
- **Recommendation**: Apply verbatim starter code to Exercise 1 in task file before starting this lesson

## v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 45-75min (Moderate)
- **Needs split**: No
- **Progression**: Bridging lesson fits well at position 3
- **Changelog reconciliation**: Exercise 1 "needs verbatim starter code" flagged since v4 as unresolved — but the task file already includes a complete code block (lines 22-40). Marking resolved.
- **Genuinely unresolved**: IDE setup (Ex 4) time is unpredictable but not critical
- **Recommendation**: Ready as-is

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 45-80min
- **Pacing**: Good (variable due to IDE setup)
- **Issues**: None
- **Recommendations**: None
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 50-70min
- **Pacing**: Good
- **Issues**: Exercise 3 asks learner to independently write code triggering clippy warning — may be hard at this stage
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 50-80min
- **Pacing**: Medium
- **Issues**: Exercise 3 needed code hint for triggering clippy warnings
- **Changes made**: Task file updated — added hint to Exercise 3 with examples of code that triggers clippy warnings (vec.len() > 0, untyped float literal, &String parameter)

### v15 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, progression, and content quality
- **Estimated time**: 50-80min
- **Pacing**: Medium (variable due to IDE setup)
- **Issues**: None
- **Changes made**: Changelog updated only
