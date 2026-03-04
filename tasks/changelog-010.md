# Changelog - Lesson 010: Writing and running tests - #[test], assert!, cargo test

## Section 2: Language Basics

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
- **Objectives added**: #[test] attribute and panic-on-failure model, assert!/assert_eq!/assert_ne! with custom messages, cargo test execution and filtering, #[should_panic] with expected message, #[cfg(test)] mod tests organization and conditional compilation
- **Exercises added**: test the basics (test functions from lessons 5-8 with assert_eq! and custom messages), testing panics (#[should_panic] for divide-by-zero), test organization and filtering (6+ tests, name filtering, #[ignore]), assert_ne! and boundary tests (edge cases with i32::MAX/MIN, reading failure output)

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Moderate for 1-hour lesson
- **Issues found**:
  - Exercise 1 requires functions from lessons 5-8 to be accessible (may need recreation if in separate projects)
  - Exercise 3 asks for 6+ tests which, combined with other exercises, totals ~12+ test functions
- **Recommendations**:
  - Clarify whether to create a fresh project or reuse previous lesson code

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Moderate (~1 hr) for 1-2 hour target
- **Changes noted**: Bridging lesson; testing is familiar from Java/Go. Exercise 1 depends on functions from lessons 5-8 existing in accessible project. Total test function count (~12+) is ambitious.
- **Why**: Good early testing introduction; minor logistics issue.
- **v4 recommendations status**: Not yet applied -- v4 recommended clarifying project structure. Gradual progression: Good bridging lesson placement.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~50-70 min
- **Pacing verdict**: Moderate
- **Split needed**: No
- **Key issues**:
  - Exercise 1 depends on functions from lessons 5-8 being accessible
- **Action taken**: Changelog updated

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Moderate (~50-70 min)
- **Status**: No changes needed

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~50-70 min (Moderate)
- **Needs split**: No
- **Progression**: Good capstone for Section 2. Testing is familiar from Java/Go. Nice bridging lesson.
- **Issues**: Exercise 1 should clarify project setup -- specify creating a fresh project and re-implementing simple functions rather than assuming old lesson code is accessible (flagged since v4, unresolved).
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~50-70 min
- **Pacing**: Good
- **Needs split**: No
- **Issues**: Exercise 1 says "Go back to functions from lessons 5-8" but doesn't clarify if functions are accessible from different lesson directories. Should specify creating a fresh project. Unresolved since v4.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Good match with issues
- **Time estimate**: 50-75 minutes (Moderate)
- **Needs splitting**: No (all under 2 hours)
- **Pacing context**: Good capstone for Sections 1-2; testing is familiar from Java/Go
- **Unresolved from prior reviews**: Exercise 1 should clarify creating a fresh lesson-010 project rather than referencing old lesson code (flagged since v4, never applied)
- **New findings**: None beyond prior reviews
- **Recommendation**: Update Exercise 1 to specify creating a fresh project with re-implemented functions before starting

## v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 50-75min (Moderate)
- **Needs split**: No
- **Progression**: Bridging lesson fits perfectly at position 10; good capstone for Sections 1-2
- **Changelog reconciliation**: Exercise 1 "should clarify project structure" — task file already specifies `cargo new lesson-010 --lib` and "(or rewrite)". Resolved.
- **Genuinely unresolved**: Consider reducing Ex 3 from 6 tests to 4
- **Recommendation**: Ready as-is; optionally trim Ex 3 test count at lesson time

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 50-75min
- **Pacing**: Good
- **Issues**: Minor — Ex 3 could trim from 6 tests to 4
- **Recommendations**: Consider reducing Ex 3 test count
- **Changes made**: Changelog updated only

### v13-fix - Applied pending fixes (2026-03-04)
- Reduced Exercise 3 test count from "at least 6" to "at least 4 (stretch: 6)"
- **Why**: 6 tests was excessive for a lesson focused on learning the testing framework
- **Resolves**: v11/v12 recommendation (low priority)

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 60-75min
- **Pacing**: Good
- **Issues**: None
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 55-75min
- **Pacing**: Medium
- **Issues**: None
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, progression, and content quality
- **Estimated time**: 55-75min
- **Pacing**: Medium
- **Issues**: None
- **Changes made**: Changelog updated only
