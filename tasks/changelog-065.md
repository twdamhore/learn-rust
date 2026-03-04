# Changelog - Lesson 065: Async I/O - files, networking, timers

## Section 14: Async Rust

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Async file I/O with tokio::fs, TCP client/server with tokio::net, timeouts with tokio::time, async I/O efficiency rationale
- **Exercises added**: Concurrent file reader, echo TCP server, timeout wrapper, concurrent directory word counter

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - Echo TCP server (Exercise 2) alone is substantial (server + client + testing with telnet)
  - Four exercises total is ambitious for async I/O
- **Recommendations**:
  - Provide starter code for the TCP server
  - Or make Exercise 4 (concurrent file processor) optional

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~2+ hr) for 1-2 hour target
- **Changes noted**: Echo TCP server alone (Exercise 2) is substantial -- building server, handling multiple connections, testing. Combined with 3 other exercises is too much. Exercise 4 overlaps with Exercise 1
- **Why**: TCP echo server is a significant exercise on its own; 4 exercises total too ambitious
- **v4 recommendations status**: Not yet applied -- v4 recommended starter code for TCP or making Exercise 4 optional. Gradual progression: Heavy; exceeds target significantly

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~2+ hours
- **Pacing verdict**: Heavy - TRIM recommended (not split)
- **Split needed**: No
- **Key issues**:
  - TCP echo server (Exercise 2) is a mini-project on its own
  - Exercise 4 (concurrent dir word counter) is redundant with Exercise 1 (concurrent file reader)
- **Action taken**: Mark Exercise 4 as optional/stretch in changelog. Recommend providing TCP server starter code when lesson is started. No split needed -- trimming exercises is sufficient

### v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: OVERLOADED (~2+ hr)
- **Status**: Changes noted below
- **SPLIT into 065a and 065b** during this review:
  - **065a**: Async file I/O and timeouts
  - **065b**: Async networking (TCP server)
- v6 recommended trimming only, but under the >2hr split rule this lesson exceeds the threshold
- See changelog-065a.md and changelog-065b.md for split lesson changelogs

### v8 - Full curriculum pacing review (2026-03-03)
- Original lesson correctly split into 065a/065b at v7. Original was ~2.5+ hrs.
- **Changes made**: None (split already done)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~150+ min
- **Pacing**: OVERLOADED
- **Needs split**: Yes (already split into 065a/065b)
- **Issues**: File I/O vs networking is clean divide.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: SUPERSEDED by 065a/065b
- **Time estimate**: 150+ minutes (original, before split)
- **Needs splitting**: Already split correctly at v7
- **Pacing context**: Original combined async file I/O, TCP networking, timeouts, and concurrent file processing. Far exceeded 2hr threshold.
- **Unresolved from prior reviews**: None (issues tracked in 065a/065b changelogs)
- **New findings**: None
- **Recommendation**: No action on this file; see changelog-065a.md and changelog-065b.md

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: N/A (SUPERSEDED)
- **Needs split**: N/A
- **Progression**: SUPERSEDED by 065a/065b. Split at v7 was correct (file I/O vs networking).
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: None (tracked in 065a/065b)
- **Recommendation**: No action on this file; see changelog-065a.md and changelog-065b.md

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- SUPERSEDED by 065a/065b. No changes to parent.

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: N/A
- **Pacing**: SUPERSEDED
- **Issues**: SUPERSEDED by 065a/065b
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. Correctly superseded by 065a/065b. **Changes**: Changelog only.
