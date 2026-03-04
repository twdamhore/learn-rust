# Changelog - Lesson 063: Threads - std::thread, move, join, scoped threads

## Section 13: Concurrency

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: std::thread::spawn with 'static requirement, move closures for threads, JoinHandle::join with Result, scoped threads via std::thread::scope, comparison with Java Thread/Runnable and Go goroutines
- **Exercises added**: Spawn 5 threads printing index/ID, move ownership with clone refactor, scoped threads borrowing parent stack slices, parallel map implementation with available_parallelism

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - Exercise 4 (parallel map with chunk splitting and available_parallelism) is ambitious for the first concurrency lesson
- **Recommendations**:
  - Make Exercise 4 a stretch goal

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~1.5 hr) for 1-2 hour target
- **Changes noted**: Exercises 1-3 well-scoped. Exercise 4 (parallel map with available_parallelism, chunk splitting, scoped threads) is a mini-project. Good Java/Go comparison (goroutines vs OS threads).
- **Why**: Exercise 4 too ambitious for first concurrency lesson.
- **v4 recommendations status**: Not yet applied -- v4 recommended making Exercise 4 a stretch goal. Gradual progression: Heavy start to concurrency section.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.5 hours
- **Pacing verdict**: Heavy - OK - under 2hr threshold
- **Split needed**: No
- **Key issues**:
  - Exercise 4 (parallel map) too ambitious for first concurrency lesson; should be stretch goal
- **Action taken**: No structural changes. Heavy but within 2hr threshold.

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Heavy (~1.5 hr)
- **Status**: No changes needed under relaxed threshold

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~90 min (Heavy)
- **Needs split**: No
- **Issues**: Exercise 4 (parallel map) should be marked [STRETCH] (flagged since v4, unresolved). Exercises 1-3 are sufficient for lesson objectives.
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~90 min
- **Pacing**: Heavy
- **Needs split**: No
- **Issues**: Exercise 4 (parallel map) too ambitious for first concurrency lesson. Combining chunk splitting, available_parallelism, scoped threads, and result collection is a mini-project. Mark [STRETCH]. Flagged since v4.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match
- **Time estimate**: 90 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: Heavy start to concurrency section, but manageable
- **Unresolved from prior reviews**: Exercise 4 (parallel map) should be marked [STRETCH]. Flagged since v4.
- **New findings**: None
- **Recommendation**: Mark Exercise 4 as [STRETCH] at lesson start

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: ~90min (Heavy)
- **Needs split**: No
- **Progression**: Good concurrency section opener
- **Changelog reconciliation**: "Exercise 4 should be [STRETCH]" flagged since v4 — already applied in task file. Resolved.
- **Genuinely unresolved**: None
- **Recommendation**: No action needed

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 80-100min
- **Pacing**: Heavy
- **Issues**: None
- **Recommendations**: None
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 60-75min
- **Pacing**: Good
- **Issues**: None
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 60-75min
- **Pacing**: Moderate-Good
- **Issues**: None
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 70-80min. **Pacing**: Medium-Heavy. **Issues**: None. **Changes**: Changelog only.
