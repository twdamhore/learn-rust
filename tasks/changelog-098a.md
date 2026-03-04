# Changelog - Lesson 098a: Project 2 Part C: Async Patterns and Observability
## Section 21: Capstone Projects

### v1 - Created from split (2026-03-03)
- Split from original lesson 098 which was rated >2 hrs during v7 review
- **Reason for split**: Original lesson 098 combined 4 exercises covering completely different skill areas (async concurrency, tracing/observability, integration testing, Docker deployment), each requiring significant setup and learning. The exercises share no common throughline and each could easily consume 1+ hour on its own.
- **Scope**: Concurrent stats endpoint with `tokio::join!` (parallel database queries, timing comparison) and tracing integration (structured logging with `tracing-subscriber`, `#[tracing::instrument]`, request logging middleware via `tower-http`)
- **Estimated time**: ~1-1.5 hours

### v2 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and changelog for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~75-90 min (Moderate-Heavy)
- **Needs split**: No
- **Issues**: Exercise 2 introduces tower-http crate without prior mention. Add explanatory note. Dropped objectives (pagination, dotenvy) should be noted as "explore on your own" stretch goals.
- **Changes made**: None

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~75-90 min
- **Pacing**: Good
- **Needs split**: No
- **Issues**: Minor: Exercise 2 introduces tower-http crate without prior mention — add explanatory note. Dropped objectives should be noted as "explore on your own" stretch goals.
- **Changes made**: Changelog updated only

### v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match (split sub-part)
- **Time estimate**: 75-90 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: Async patterns and observability focused. Builds well on 097a/097b foundation.
- **Unresolved from prior reviews**: (1) tower-http introduced without prior mention -- add explanatory note. (2) Dropped objectives (pagination, dotenvy) should be noted as stretch goals.
- **New findings**: None
- **Recommendation**: Add tower-http note and list dropped objectives as stretch goals when task content is next updated

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 80-95min (Heavy)
- **Needs split**: No
- **Progression**: Async patterns and observability focused. Builds well on 097a/097b foundation.
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: Minor: tower-http needs introductory note. Dropped objectives from original should be documented as stretch.
- **Recommendation**: Add tower-http introductory note and document dropped objectives as stretch goals

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 80-100min
- **Pacing**: Heavy
- **Issues**: (1) tower-http introduced without context. (2) Ex 1 needs latency simulation hint.
- **Recommendations**: Add tower-http intro note; provide tokio::time::sleep hint for simulated latency
- **Changes made**: Changelog updated only

### v12-fix - Task file changes applied (2026-03-04)
- Added tower-http introduction where it is first mentioned in Exercise 2 (explains it provides HTTP-specific middleware for tower-based frameworks like axum)
- Added latency simulation hint to Exercise 1 (tokio::time::sleep for making sequential vs concurrent difference visible)

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 80-100min
- **Pacing**: Heavy
- **Issues**: Exercise 2 overloaded — asks for tracing setup + #[instrument] + tower-http TraceLayer middleware + span verification in single exercise. Should be split into 2 exercises (tracing setup, then tower-http middleware)
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 80-100min
- **Pacing**: Heavy
- **Issues**: Exercise 2 overloaded — combines tracing setup + tower-http middleware in single exercise
- **Changes made**: Split overloaded Exercise 2 into two exercises (tracing setup, then tower-http middleware), task file updated

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 80-100min. **Pacing**: Heavy. **Issues**: None — tower-http intro, latency hint, and exercise split verified. **Changes**: Changelog only.
