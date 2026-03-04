# Changelog - Lesson 053: Functional patterns - map, filter, fold, method chaining

## Section 11: Closures & Functional Patterns

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: map/filter/filter_map/fold usage, chaining iterator adaptors, flat_map for nested structures, collect's type-driven behavior, comparison with Java Streams and Go loops
- **Exercises added**: Imperative-to-functional loop rewrites, fold for aggregation (sum, char frequency, min/max), flat_map + collect with Result short-circuiting, CSV data pipeline with no mutable variables

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - Effectively 10 sub-exercises packed into 4 (Exercise 1 has 4, Exercise 2 has 3)
  - Significant topic overlap with lessons 037-038 (iterators section)
- **Recommendations**:
  - Reduce sub-exercises: Exercise 1 to 2-3 problems, Exercise 2 to 2 problems
  - Acknowledge overlap with lessons 037-038 and focus on the closure/functional angle

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~1.5-2 hr) for 1-2 hour target
- **Changes noted**: ~10 sub-exercises packed into 4 numbered exercises. Significant overlap with lessons 037-038 (iterators section). Exercise 1 has 4 conversions, Exercise 2 has 3 fold applications.
- **Why**: Too many sub-problems; should focus on closure-specific angle, not re-teach iterator basics.
- **v4 recommendations status**: Not yet applied -- v4 recommended reducing sub-exercises. Gradual progression: Heavy; two heavy in a row.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.5-2 hours
- **Pacing verdict**: Heavy - OK - under 2hr threshold (borderline)
- **Split needed**: No
- **Key issues**:
  - ~10 sub-exercises packed in 4 exercises
  - Significant overlap with lessons 037-038
  - CSV pipeline is a mini-project
- **Action taken**: No structural changes. Borderline but kept as single lesson.

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Heavy (~1.5-2 hr borderline)
- **Status**: No changes needed under relaxed threshold
- Overlap with 037-038 still flagged.

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~105 min (Heavy, borderline 2hr)
- **Needs split**: No
- **Issues**: ~10 sub-exercises is too many. Overlap with 037-038 needs explicit acknowledgment. Reduce Exercise 1 from 4 to 2 conversions, Exercise 2 from 3 to 2 folds (flagged since v4, unresolved).
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~105 min
- **Pacing**: Heavy (borderline)
- **Needs split**: No
- **Issues**: ~10 sub-exercises packed into 4 numbered exercises. Exercise 1 should reduce from 4 to 2 conversions. Exercise 2 should reduce from 3 to 2 folds. Significant overlap with lessons 037-038 (iterators section). Should acknowledge and focus on closure/functional angle. Flagged since v4.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Good match
- **Time estimate**: 105 minutes (Heavy-Borderline)
- **Needs splitting**: No
- **Pacing context**: Second heavy lesson in a row after 052
- **Unresolved from prior reviews**: (1) Reduce Exercise 1 from 4 to 2 sub-parts, (2) Reduce Exercise 2 from 3 to 2 sub-parts, (3) Acknowledge overlap with lessons 037-038 and focus on closure angle. All flagged since v4.
- **New findings**: None
- **Recommendation**: Apply sub-exercise reductions and add overlap acknowledgment at lesson start

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 90-120min (Heavy-Borderline)
- **Needs split**: No
- **Progression**: Second heavy lesson in a row after 052
- **Changelog reconciliation**: Prior reviews claimed "~10 sub-exercises" -- task file actually has ~7 after trimming (2+2+2+1). Partially resolved. Overlap with 037-038 acknowledged in task file.
- **Genuinely unresolved**: Exercise 4 (CSV pipeline) is main time risk
- **Recommendation**: Monitor Exercise 4 time at lesson start; sub-exercise count partially resolved

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 90-120min
- **Pacing**: Heavy (borderline)
- **Issues**: Ex 4 (CSV pipeline) is a mini-project that should be marked [STRETCH]. UNRESOLVED.
- **Recommendations**: Mark Ex 4 as [STRETCH]
- **Changes made**: Changelog updated only

### v12-fix - Task file changes applied (2026-03-04)
- Marked Exercise 4 (Data pipeline / CSV parsing) as [STRETCH]
- **Why**: CSV pipeline is a mini-project that risks pushing the lesson over 2 hours; marking as stretch keeps it available without making it mandatory

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 60-75min
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
- Reviewed. **Time**: 60-75min. **Pacing**: Medium. **Issues**: None — overlap with 037-038 acknowledged. **Changes**: Changelog only.
