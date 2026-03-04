# Changelog - Lesson 060: Shared state - Mutex<T>, RwLock, Arc<Mutex<T>>

## Section 13: Concurrency

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Mutex<T> with MutexGuard auto-unlock, Arc<Mutex<T>> for multi-threaded shared state, RwLock for read-heavy workloads, lock poisoning handling, comparison with Java synchronized and Go sync.Mutex
- **Exercises added**: Shared counter with 10 threads x 1000 increments, thread-safe cache with RwLock<HashMap>, Mutex vs RwLock performance comparison, poisoned lock recovery with into_inner

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - Exercise 2 (thread-safe cache) and Exercise 3 (Mutex vs RwLock timing) are both substantial
  - Lock poisoning (Exercise 4) requires deliberately panicking inside a thread
- **Recommendations**:
  - Will fill the full hour but is achievable -- no changes needed

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~1 hr achievable) for 1-2 hour target
- **Changes noted**: Exercise 3 timing comparison depends on micro-benchmarking knowledge (lesson 84). Lock poisoning is niche but worth covering. Rust Mutex<T> (protects data) vs Java synchronized (protects code) is key insight.
- **Why**: Heavy but achievable given concurrency context.
- **v4 recommendations status**: N/A (v4 said no changes needed). Gradual progression: Reasonable for late-section lesson.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.25 hours
- **Pacing verdict**: Moderate-Heavy - OK - under 2hr threshold
- **Split needed**: No
- **Key issues**:
  - Exercise 3 benchmarking knowledge from lesson 084 (minor forward reference)
- **Action taken**: No structural changes. Manageable pacing.

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Moderate-Heavy (~1.25 hr)
- **Status**: No changes needed

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~75 min (Moderate-Heavy)
- **Needs split**: No
- **Progression**: Mutex-protects-data insight is the highlight.
- **Issues**: Minor forward reference to benchmarking in Exercise 3 (lesson 084), but Instant/elapsed is self-explanatory.
- **Changes made**: None

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~75 min
- **Pacing**: Heavy (moderate-heavy)
- **Needs split**: No
- **Issues**: None
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match
- **Time estimate**: 75 minutes (Moderate-Heavy)
- **Needs splitting**: No
- **Pacing context**: Mutex-protects-data insight well-highlighted. Good Java/Go comparison.
- **Unresolved from prior reviews**: None
- **New findings**: None
- **Recommendation**: No changes needed

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 75-90min (Moderate-Heavy)
- **Needs split**: No
- **Progression**: Mutex-protects-data insight well-highlighted
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: None
- **Recommendation**: No action needed

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 75-90min
- **Pacing**: Good (upper end)
- **Issues**: None
- **Recommendations**: None
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing review (2026-03-04)
- Reviewed all 100+ tasks for realistic human pacing (1-2hr OK, split if >2hr)
- **Estimated time**: ~90-110min (slightly heavy)
- **Decision**: No split. Added [STRETCH] to Exercise 3 (Mutex vs RwLock comparison benchmark)
- **Rationale**: 4 exercises with no STRETCH label. The benchmark exercise (timing Mutex vs RwLock with 8 readers/2 writers) is the heaviest and involves threaded timing code. Marking it STRETCH lets learners focus on the core Mutex/RwLock concepts.
- **Changes made**: Exercise 3 marked [STRETCH] in task file

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 70-85min
- **Pacing**: Good
- **Issues**: None
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 70-85min
- **Pacing**: Moderate-Heavy
- **Issues**: None
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 75-85min. **Pacing**: Medium-Heavy. **Issues**: None. **Changes**: Changelog only.
