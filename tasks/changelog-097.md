# Changelog - Lesson 097: Project 2 - Web API (axum, sqlx, auth, middleware)

## Section 21: Capstone Projects

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: axum server setup with Router/extractors, REST API design for notes resource, sqlx SQLite integration with State extractor, JWT authentication middleware, handler/service/repo project structure
- **Exercises added**: Define REST routes with hardcoded responses, add SQLite persistence with migrations and repository, implement JWT auth with login endpoint and protected routes, request validation and structured JSON error handling

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Overloaded for 1-hour lesson
- **Issues found**:
  - Introduces axum (entirely new, not taught in any previous lesson) while simultaneously building full CRUD + auth
  - jsonwebtoken crate is also entirely new
  - Learning axum Router + extractors + response types while building a complete API is realistically 3-4 hours
  - Exercise format uses unnumbered bullets (formatting inconsistency)
  - **Most overloaded task in the 081-100 range**
- **Recommendations**:
  - Rebalance split with lesson 098: move auth/JWT to 098, keep axum basics + CRUD in 097
  - Or add an axum introduction lesson before the capstone
  - Standardize exercise format

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: OVERLOADED (~3-4 hr) for 1-2 hour target
- **Changes noted**: MOST CRITICAL CURRICULUM GAP -- axum is never taught before this capstone. jsonwebtoken also entirely new. Learning axum from scratch while building complete REST API with auth is 3-4 hours minimum. Exercise format inconsistency.
- **Why**: No introductory axum lesson exists in the curriculum.
- **v4 recommendations status**: Not yet applied -- v4 recommended rebalancing with 098 or adding axum intro lesson. Gradual progression: CRITICAL -- biggest pacing problem in 081-100.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~3-4 hours
- **Pacing verdict**: OVERLOADED - split required
- **Split needed**: Yes - split into 097a/097b
- **Key issues**:
  - CRITICAL: axum is never taught in any previous lesson; learner must learn axum from scratch
  - Simultaneously building complete REST API with CRUD, SQLite, JWT auth
  - jsonwebtoken crate also entirely new
  - Most overloaded task in the 081-100 range
- **Action taken**: Split into task-097a.md (Axum Web API Basics -- axum introduction, Router, handlers, extractors, in-memory CRUD) and task-097b.md (Database and Authentication -- SQLite with sqlx, JWT auth, middleware). Part A provides the missing axum introduction using in-memory storage only. Part B adds database and auth. Each part is now ~1.5-2 hours.

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Already split in v6 into 097a/097b
- **Status**: No changes needed
- Prior split was adequate under relaxed threshold; no additional changes required

### v8 - Full curriculum pacing review (2026-03-03)
- Original lesson correctly split into 097a/097b at v6. Original was ~180-240 min (most overloaded in 081-100).
- **Changes made**: None (split already done)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~180-240 min
- **Pacing**: OVERLOADED
- **Needs split**: Already split into 097a/097b
- **Issues**: Most overloaded in 081-100. axum never taught in any previous lesson.
- **Changes made**: Changelog updated only

### v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: SUPERSEDED by 097a/097b
- **Time estimate**: 180-240 minutes (Overloaded -- original)
- **Needs splitting**: Already split into 097a/097b at v6
- **Pacing context**: Most overloaded in 081-100. axum never taught previously. Split correctly separates axum intro (097a) from database/auth (097b).
- **Unresolved from prior reviews**: None (issues resolved by split)
- **New findings**: None
- **Recommendation**: No action needed on original; see 097a and 097b changelogs

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: N/A (SUPERSEDED)
- **Needs split**: N/A
- **Progression**: SUPERSEDED by 097a/097b. Split was correct. In-memory storage for axum intro was the key insight.
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: None
- **Recommendation**: No action needed on original; see 097a and 097b changelogs

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- SUPERSEDED by 097a/097b. No changes to parent.

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: N/A
- **Pacing**: SUPERSEDED
- **Issues**: SUPERSEDED by 097a/097b
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. Correctly superseded. **Changes**: Changelog only.
