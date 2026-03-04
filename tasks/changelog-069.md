# Changelog - Lesson 069: Tokio basics - tasks, spawn, select!, join!

## Section 14: Async Rust

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Tokio runtime setup, tokio::spawn with Send+'static bounds, select! for racing, join!/try_join! for concurrency, task vs thread distinction
- **Exercises added**: Concurrent tasks with JoinHandle, select! racing with channel branch, join! wall-clock time comparison, task vs thread performance benchmark

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Moderate-to-Heavy for 1-hour lesson
- **Issues found**:
  - Exercise 4 (task vs thread at 1000 units) memory measurement is tricky from within Rust
- **Recommendations**:
  - Provide guidance on how to measure memory (e.g., /proc/self/status on Linux)

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Moderate-to-Heavy (~1-1.5 hr) for 1-2 hour target
- **Changes noted**: Exercise 4 (1000 tasks vs 1000 threads with memory measurement) is tricky -- measuring memory from within Rust is non-trivial cross-platform. Exercises 1-3 are reasonable
- **Why**: Memory measurement needs platform-specific guidance
- **v4 recommendations status**: Not yet applied -- v4 recommended /proc/self/status guidance for Linux. Gradual progression: Slight upward push

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1-1.5 hours
- **Pacing verdict**: Moderate-Heavy - under 2hr threshold
- **Split needed**: No
- **Key issues**:
  - Exercise 4 (memory measurement for 1000 tasks vs threads) is tricky and platform-specific
  - v4 recommended providing /proc/self/status guidance
- **Action taken**: No split required. Previous recommendation to provide /proc/self/status guidance for Linux should be applied when lesson is started

### v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Moderate-Heavy (~1-1.5 hr)
- **Status**: No changes needed
- Well within relaxed threshold

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~70-90 min (Moderate-Heavy)
- **Needs split**: No
- **Issues**: Exercise 4 memory measurement needs guidance -- add note about /proc/self/status or htop (flagged since v4, unresolved).
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~70-90 min
- **Pacing**: Good (upper end)
- **Needs split**: No
- **Issues**: Exercise 4 memory measurement requires /proc/self/status guidance. Add Linux-specific guidance. Unresolved since v4.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match
- **Time estimate**: 70-90 minutes (Moderate-Heavy)
- **Needs splitting**: No
- **Pacing context**: Exercises 1-3 are well-scoped. Exercise 4 memory measurement is the only sticking point.
- **Unresolved from prior reviews**: Exercise 4 memory measurement needs /proc/self/status guidance for Linux (unresolved since v4)
- **New findings**: None
- **Recommendation**: Add Linux /proc/self/status guidance to Exercise 4 when lesson is started

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: ~80min (Moderate-Heavy)
- **Needs split**: No
- **Progression**: Exercises 1-3 well-scoped; Exercise 4 is the only sticking point
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: Exercise 4 memory measurement needs `/proc/self/status` guidance for Linux
- **Recommendation**: Add `/proc/self/status` parsing guidance to Exercise 4 at lesson start

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 70-90min
- **Pacing**: Good
- **Issues**: Ex 4 still needs /proc/self/status memory measurement guidance. UNRESOLVED from v4.
- **Recommendations**: Add Linux-specific guidance or simplify to wall-clock time comparison only
- **Changes made**: Changelog updated only

### v12-fix - Task file changes applied (2026-03-04)
- Added memory measurement guidance tip to Exercise 4 (task vs thread comparison)
- Simplified requirement: wall-clock time is the primary metric; memory comparison is optional
- Added Linux-specific tip: use `/proc/self/status | grep VmRSS` from within the program or observe with `htop`
- **Why**: Measuring memory from within Rust is non-trivial cross-platform; wall-clock time alone demonstrates the dramatic difference
- **Resolves**: Unresolved item from v4/v5/v6/v8/v9/v10/v11/v12

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
- **Issues**: Added tokio::sync::mpsc bridging note to Exercise 2
- **Changes made**: Task file updated — added note to Exercise 2 explaining tokio::sync::mpsc as async equivalent of std::sync::mpsc from lesson 064

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 75-85min. **Pacing**: Medium-Heavy. **Issues**: None. **Changes**: Changelog only.
