# Changelog - Lesson 006: Scalar types - integers, floats, bool, char, casting with as

## Section 2: Language Basics

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: all integer types (i8-i128, u8-u128, isize/usize), f32/f64 and IEEE 754 pitfalls, bool and char (4-byte Unicode), type inference and annotations, casting with `as` and truncation, overflow behavior (debug panic vs release wrapping, explicit methods)
- **Exercises added**: type inference explorer (discovering inferred types), overflow behavior (debug vs release, checked/wrapping/saturating), casting chain (i32 to i8 to u8 to f64), char and Unicode (emoji, CJK, code points, size_of)

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - 6 objectives spanning numeric types, casting, AND overflow handling
  - Overflow methods (wrapping_*, checked_*, saturating_*, overflowing_*) are dense sub-topic
- **Recommendations**:
  - Mark overflow methods as 'awareness level' rather than 'mastery level' to reduce pressure

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~1.5 hr) for 1-2 hour target
- **Changes noted**: 6 objectives is the most in any lesson in 001-020. Overflow methods (wrapping_*, checked_*, saturating_*, overflowing_*) are dense for someone without C/C++ background.
- **Why**: Too many sub-topics packed in; overflow handling deserves awareness-level treatment.
- **v4 recommendations status**: Not yet applied -- v4 recommended awareness-level for overflow methods. Gradual progression: Spike from lesson 5; heavy for this early stage.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.25-1.75 hr
- **Pacing verdict**: Heavy but under 2hr threshold
- **Split needed**: No
- **Key issues**:
  - 6 objectives is the most in any lesson in 001-020
  - Overflow methods dense for non-C/C++ background
- **Action taken**: Changelog updated

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Heavy (~1.25-1.75 hr)
- **Status**: No changes needed
- Overflow methods dense but acceptable at this pace

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~75-105 min (Heavy)
- **Needs split**: No
- **Progression**: Significant spike from lesson 5 but tolerable because integer types are familiar from Java/Go.
- **Issues**: Overflow methods (wrapping_*, checked_*, saturating_*, overflowing_*) should be marked as awareness-level, not mastery (flagged since v4, unresolved).
- **Contingency**: If learner struggles, split into 006a (types + inference) and 006b (casting + overflow).
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~75-105 min
- **Pacing**: Heavy
- **Needs split**: No
- **Issues**: 6 objectives, overflow methods (wrapping_*/checked_*/saturating_*/overflowing_*) are dense for non-C/C++ background. Should be awareness-level, not mastery. Unresolved since v4.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Good match with issues
- **Time estimate**: 75-105 minutes (Heavy)
- **Needs splitting**: No (all under 2 hours)
- **Pacing context**: Significant spike from lesson 5; heaviest in Section 2 alongside lesson 9
- **Unresolved from prior reviews**: Overflow methods (wrapping_*, checked_*, etc.) should be marked awareness-level not mastery-level (flagged since v4, never applied). Contingency split plan (006a/006b) exists but not needed unless learner struggles.
- **New findings**: None beyond prior reviews
- **Recommendation**: Mark overflow methods as awareness-level in task file before starting; keep split plan as contingency

## v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 75-100min (Heavy)
- **Needs split**: No
- **Progression**: Significant spike from lesson 5 but tolerable with Java/Go integer familiarity
- **Changelog reconciliation**: Overflow methods "should be awareness-level" flagged since v4 — task file objective 6 already says "(awareness-level)". Resolved.
- **Genuinely unresolved**: Contingency 006a/006b split plan is sensible but not needed pre-emptively
- **Recommendation**: Ready as-is; keep split plan as contingency if learner struggles

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 75-110min
- **Pacing**: Heavy
- **Issues**: 6 objectives is a lot; casting chain (Ex 3) is most time-consuming
- **Recommendations**: If learner runs over, defer Ex 3 to lesson 7 warm-up
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 60-75min
- **Pacing**: Good
- **Issues**: None
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 65-90min
- **Pacing**: Heavy
- **Issues**: None
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, progression, and content quality
- **Estimated time**: 65-100min
- **Pacing**: Heavy
- **Issues**: Overflow methods correctly at awareness-level. Heavy but within bounds
- **Changes made**: Changelog updated only
