# Changelog - Lesson 098: Project 2 - continued (async patterns, deployment)

## Section 21: Capstone Projects

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Async patterns (tokio::join!, spawn, graceful shutdown), tracing with structured logging and request instrumentation, API integration tests, pagination and search, deployment configuration with env vars
- **Exercises added**: Concurrent stats endpoint with tokio::join!, tracing setup with EnvFilter and request logging middleware, full integration test suite for auth and CRUD flows, Dockerfile with multi-stage build and health check endpoint

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - Objective 4 (pagination/search) has no dedicated exercise
  - Objective 5 (dotenvy) has no exercise
  - Exercise 4 introduces Docker -- not a Rust topic, assumes Docker knowledge
  - Exercise format uses unnumbered bullets (formatting inconsistency)
- **Recommendations**:
  - Add exercises for pagination and dotenvy, or remove those objectives
  - Consider replacing Docker exercise with simpler deployment approach
  - Standardize exercise format

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~1.5-2 hr) for 1-2 hour target
- **Changes noted**: Objectives 4 (pagination) and 5 (dotenvy) have no exercises. Exercise 4 (Docker) is not a Rust topic. Assumes lesson 097 was completed successfully, but 097 is itself overloaded. Exercise format inconsistency.
- **Why**: Objectives without exercises; non-Rust content; depends on overloaded predecessor.
- **v4 recommendations status**: Not yet applied -- v4 flagged all issues. Gradual progression: Heavy; compromised by 097.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.5-2 hours
- **Pacing verdict**: Heavy - borderline under 2hr threshold
- **Split needed**: No
- **Key issues**:
  - Objectives 4 (pagination) and 5 (dotenvy) have no exercises
  - Exercise 4 (Dockerfile) assumes Docker knowledge outside Rust scope
  - Depends on overloaded lesson 097 (now split into 097a/097b which improves this)
- **Action taken**: No split needed. With lesson 097 split into 097a/097b, the dependency chain improves. Remaining issues (missing exercises for pagination/dotenvy, Docker assumption) should be addressed in task content updates.

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: OVERLOADED (~2+ hr)
- **Status**: Changes noted below
- **SPLIT into 098a and 098b**: 098a covers async patterns and observability (tokio::join!, tracing). 098b covers integration testing and Docker deployment.

### v8 - Full curriculum pacing review (2026-03-03)
- Original lesson correctly split into 098a/098b at v7. Original was ~120+ min.
- **Changes made**: None (split already done)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~120+ min
- **Pacing**: OVERLOADED
- **Needs split**: Already split into 098a/098b
- **Issues**: Combined four unrelated skill areas.
- **Changes made**: Changelog updated only

### v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: SUPERSEDED by 098a/098b
- **Time estimate**: 120+ minutes (Overloaded -- original)
- **Needs splitting**: Already split into 098a/098b at v7
- **Pacing context**: Original combined four unrelated skill areas (async, tracing, testing, Docker). Correctly split.
- **Unresolved from prior reviews**: None (issues resolved by split)
- **New findings**: None
- **Recommendation**: No action needed on original; see 098a and 098b changelogs

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: N/A (SUPERSEDED)
- **Needs split**: N/A
- **Progression**: SUPERSEDED by 098a/098b. Split was correct.
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: None
- **Recommendation**: No action needed on original; see 098a and 098b changelogs

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- SUPERSEDED by 098a/098b. No changes to parent.

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: N/A
- **Pacing**: SUPERSEDED
- **Issues**: SUPERSEDED by 098a/098b
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. Correctly superseded. **Changes**: Changelog only.
