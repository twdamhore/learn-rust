# Changelog - Lesson 049: Lifetime practice - common errors, fixing lifetime puzzles

## Section 10: Lifetimes

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
- **Objectives added**: Diagnosing common lifetime error patterns, fix strategies (extend scope/restructure/own/clone), when to restructure vs annotate, reference vs owned data intuition, reading complex error messages
- **Exercises added**: 5 lifetime puzzle programs to fix, borrowed-to-owned Tokenizer refactor, over-annotated simplification with clippy, Cache struct with borrow conflict resolution

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - Exercise 1 alone is 5 broken programs to fix (could take 25-50 minutes)
  - Exercise 2 (Tokenizer refactor) is a substantial code transformation
  - Total volume is ambitious for 1 hour
- **Recommendations**:
  - Reduce Exercise 1 from 5 puzzle programs to 3
  - Or make Exercises 3-4 optional

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy-to-Overloaded (~1.5-2 hr) for 1-2 hour target
- **Changes noted**: Exercise 1 alone has 5 broken programs to debug and fix (25-50 min). Exercise 2 (Tokenizer refactor) is substantial transformation. Good bridging lesson concept but volume is excessive.
- **Why**: Bridging lesson intent excellent; execution too ambitious.
- **v4 recommendations status**: Not yet applied -- v4 recommended reducing Exercise 1 from 5 to 3 programs or making Exercises 3-4 optional. Gradual progression: Too heavy for a practice/consolidation lesson.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.5-2 hours
- **Pacing verdict**: Heavy - OK - under 2hr threshold (borderline)
- **Split needed**: No
- **Key issues**:
  - Exercise 1 contains 5 broken programs to debug (25-50 min alone)
  - Tokenizer refactor is substantial
  - Ironic that "practice/consolidation" bridging lesson is one of the heaviest
- **Action taken**: No structural changes. Borderline but kept as single lesson.

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: OVERLOADED (~2-2.5 hr)
- **Status**: Changes noted below
- **SPLIT into 049a and 049b** during this review. 049a covers diagnosing lifetime errors (puzzles + tokenizer refactor). 049b covers lifetime design patterns (simplification + cache struct).

### v8 - Full curriculum pacing review (2026-03-03)
- Original lesson correctly split into 049a/049b at v7. Original was ~150 min.
- **Changes made**: None (split already done)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~150 min (original)
- **Pacing**: OVERLOADED
- **Needs split**: Yes (already split into 049a/049b)
- **Issues**: None — good split. Diagnosing errors vs design patterns.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: SUPERSEDED by 049a/049b
- **Time estimate**: 120-150 minutes original (correctly split)
- **Needs splitting**: Already split at v7
- **Pacing context**: Original bridging lesson was ironically one of the heaviest; split resolved this
- **Unresolved from prior reviews**: None for parent -- see 049a/049b changelogs
- **New findings**: None
- **Recommendation**: No changes to parent; see 049a/049b for sub-part status

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 120-150min original (OVERLOADED)
- **Needs split**: No (SUPERSEDED by 049a/049b)
- **Progression**: Split was correct. Original was 120-150min.
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: None -- see 049a/049b changelogs
- **Recommendation**: No changes to parent; see 049a/049b for sub-part status

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- SUPERSEDED by 049a/049b. No changes to parent.

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: N/A
- **Pacing**: SUPERSEDED
- **Issues**: SUPERSEDED by 049a/049b
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. Correctly superseded by 049a/049b. **Changes**: Changelog only.
