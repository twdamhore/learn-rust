# Changelog - Lesson 067: Atomics - AtomicBool, AtomicUsize, ordering, lock-free basics

## Section 13: Concurrency

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: AtomicBool/AtomicUsize/AtomicI64 operations (load, store, fetch_add, compare_exchange), memory ordering levels (Relaxed, Acquire/Release, SeqCst), atomics vs Mutex decision criteria, atomics as synchronization building blocks
- **Exercises added**: Atomic counter with 10 threads and Relaxed ordering, AtomicBool shutdown flag with Acquire/Release, atomic vs Mutex vs RwLock benchmark comparison, SpinLock implementation with compare_exchange

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - Memory ordering (Relaxed vs Acquire/Release vs SeqCst) is conceptually dense for someone without C/C++ background
  - Benchmark exercise (Exercise 3) may take 20+ minutes to set up and run
- **Recommendations**:
  - Consider providing the benchmark harness so learners focus on understanding ordering
  - SpinLock exercise (Exercise 4) could be made optional

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~1.5-2 hr) for 1-2 hour target
- **Changes noted**: Memory ordering (Acquire/Release/SeqCst) is extremely dense with no C/C++ background. Benchmark exercise (Exercise 3) requires setup of three implementations. SpinLock exercise (Exercise 4) with compare_exchange is non-trivial
- **Why**: Memory ordering is a steep cliff for this learner
- **v4 recommendations status**: Not yet applied -- v4 recommended providing benchmark harness and making SpinLock optional. Gradual progression: Heavy spike ending concurrency section

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.5-2 hours
- **Pacing verdict**: Heavy - borderline 2hr threshold
- **Split needed**: No
- **Key issues**:
  - Memory ordering (Relaxed, Acquire/Release, SeqCst) is a steep cliff for non-C/C++ background
  - SpinLock with compare_exchange is non-trivial
  - Heavy ending to the concurrency section
- **Action taken**: No split required, but remains borderline. Previous v4 recommendations (provide benchmark harness, make SpinLock optional) should be applied when lesson is started

### v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Heavy (~1.5-2 hr borderline)
- **Status**: No changes needed under relaxed threshold
- SpinLock exercise should be made optional when lesson is started
- Memory ordering is dense but acceptable at the relaxed 2hr pace

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~110 min (Heavy, borderline 2hr)
- **Needs split**: No
- **Issues**: Memory ordering is steepest cliff for non-C/C++ learner. Add preamble with "practical recipes" approach (Relaxed for counters, Acquire/Release for flags, SeqCst when in doubt). Exercise 3 should provide benchmark harness. Exercise 4 (SpinLock) should be [STRETCH]. All flagged since v4, unresolved.
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~100-120 min
- **Pacing**: Heavy
- **Needs split**: No (borderline)
- **Issues**: Memory ordering (Relaxed/Acquire/Release/SeqCst) is extremely dense for non-C/C++ background. Exercise 4 (SpinLock with compare_exchange) should be [STRETCH]. Exercise 3 should provide benchmark harness. Add "practical recipes" preamble for memory ordering. Unresolved since v4.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match
- **Time estimate**: 100-120 minutes (Heavy-Borderline)
- **Needs splitting**: No (borderline but under 2hr threshold)
- **Pacing context**: Steepest cliff in concurrency section for non-C/C++ learner. Memory ordering concepts are extremely dense.
- **Unresolved from prior reviews**: (1) Exercise 4 SpinLock should be [STRETCH], (2) Exercise 3 needs benchmark harness provided, (3) Add practical memory ordering recipes preamble (Relaxed for counters, Acquire/Release for flags, SeqCst when in doubt). All unresolved since v4.
- **New findings**: None
- **Recommendation**: Apply all three unresolved fixes when lesson is started

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 100-120min (Heavy-Borderline)
- **Needs split**: No
- **Progression**: Steepest cliff in concurrency section for non-C/C++ learner
- **Changelog reconciliation**: (1) "Exercise 4 SpinLock should be [STRETCH]" — already in task file. Resolved. (2) "Add memory ordering recipes" — quick reference table and rule-of-thumb box already in task file. Resolved.
- **Genuinely unresolved**: Exercise 3 benchmark harness (minor, defer to lesson start)
- **Recommendation**: Provide benchmark harness for Exercise 3 at lesson start

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 100-120min
- **Pacing**: Heavy (borderline)
- **Issues**: Ex 3 (atomic vs Mutex vs RwLock benchmark) needs a benchmark harness — 20-30min of boilerplate otherwise
- **Recommendations**: Provide benchmark scaffold with timing loop and output formatting
- **Changes made**: Changelog updated only

### v12-fix - Task file changes applied (2026-03-04)
- Added benchmark harness starter code to Exercise 3 (atomic vs Mutex vs RwLock benchmark)
- Provides `bench()` timing function and `main()` with three labeled closures for the learner to fill in
- **Why**: Exercise 3 requires 20-30min of boilerplate setup; learner should focus on understanding atomics vs locks, not on writing timing infrastructure
- **Resolves**: Unresolved item from v4/v8/v9/v10/v11/v12

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 75-90min
- **Pacing**: Good (borderline Heavy)
- **Issues**: None
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 75-90min
- **Pacing**: Heavy
- **Issues**: None
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 80-95min. **Pacing**: Heavy. **Issues**: None — all mitigations in place (memory ordering reference, benchmark harness, STRETCH). **Changes**: Changelog only.
