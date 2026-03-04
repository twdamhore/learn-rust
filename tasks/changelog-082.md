# Changelog - Lesson 082: Integration tests, test fixtures, conditional compilation

## Section 18: Testing & Quality

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: tests/ directory setup, shared test utilities in common/mod.rs, conditional compilation with #[cfg], unit vs integration test distinction, testing error conditions from user perspective
- **Exercises added**: Calculator integration tests, shared test fixtures across files, feature-gated serde tests, exhaustive error condition testing

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Moderate for 1-hour lesson
- **Issues found**:
  - Exercise 3 references serde feature-gating -- serde not taught until lesson 086 (light forward reference)
- **Recommendations**:
  - Note serde dependency or replace with a simpler feature example

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Moderate (~1 hr, with caveat) for 1-2 hour target
- **Changes noted**: Exercise 3 uses serde (feature-gating) before serde is taught (lesson 086). A simpler feature example would be more appropriate.
- **Why**: Forward reference to serde undermines the exercise
- **v4 recommendations status**: Not yet applied -- v4 flagged serde forward reference. Gradual progression: Mostly smooth; fix serde reference.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1-1.25 hours
- **Pacing verdict**: Moderate - OK - under 2hr threshold
- **Split needed**: No
- **Key issues**:
  - Exercise 3 uses serde feature-gating but serde not taught until lesson 086 (forward reference)
- **Action taken**: No split needed. Forward reference to serde in Exercise 3 should be addressed when task content is updated (replace with simpler feature example).

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Moderate (~1-1.25 hr)
- **Status**: No changes needed
- Serde forward reference in Ex3 still flagged

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~70 min (Moderate)
- **Needs split**: No
- **Issues**: Exercise 3 uses serde feature-gating but serde not taught until lesson 086. Replace with simpler feature example (flagged since v4 across 4 review rounds, STILL unresolved).
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~65-75 min
- **Pacing**: Good
- **Needs split**: No
- **Issues**: Exercise 3 uses serde feature-gating but serde not taught until lesson 86 — prerequisite violation. Replace with simpler feature example (e.g., optional verbose feature with extra debug output). Unresolved since v4.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match
- **Time estimate**: 65-75 minutes (Moderate)
- **Needs splitting**: No
- **Pacing context**: Solid progression from 081. Conditional compilation is well-scoped.
- **Unresolved from prior reviews**: Exercise 3 uses serde feature-gating but serde not taught until lesson 086 — replace with simpler feature example. Also overlaps with task 093 Exercise 3 (both feature-gate with serde).
- **New findings**: None
- **Recommendation**: Replace Exercise 3 serde dependency with simpler feature example before lesson start

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 65-80min (Moderate)
- **Needs split**: No
- **Progression**: Solid progression from 081
- **Changelog reconciliation**: "Exercise 3 serde forward reference" flagged since v4 -- task file now uses `verbose` feature with `println!`, not serde. Resolved.
- **Genuinely unresolved**: None
- **Recommendation**: No action needed

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 65-80min
- **Pacing**: Good
- **Issues**: None
- **Recommendations**: None
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 75-90min
- **Pacing**: Good
- **Issues**: None
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 70-85min
- **Pacing**: Moderate
- **Issues**: None
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 70-85min. **Pacing**: Moderate. **Issues**: None — serde forward-reference resolution verified. **Changes**: Changelog only.
