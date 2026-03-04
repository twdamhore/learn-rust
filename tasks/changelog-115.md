# Changelog - Lesson 115: Project 2 Part D: Testing and Deployment
## Section 21: Capstone Projects

### v1 - Created from split (2026-03-03)
- Split from original lesson 114 which was rated >2 hrs during v7 review
- **Reason for split**: Original lesson 114 combined 4 exercises covering completely different skill areas (async concurrency, tracing/observability, integration testing, Docker deployment), each requiring significant setup and learning. The exercises share no common throughline and each could easily consume 1+ hour on its own.
- **Scope**: Integration tests (spin up server with in-memory DB, test auth flows, test CRUD end-to-end, test error cases) and deployment configuration (multi-stage Dockerfile, externalized env-var config, health check endpoint)
- **Estimated time**: ~1-1.5 hours

### v2 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and changelog for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~80-100 min (Moderate-Heavy)
- **Needs split**: No
- **Issues**: Exercise 2 (Dockerfile) assumes Docker installed. Add prerequisite note with fallback.
- **Changes made**: None

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~80-100 min
- **Pacing**: Good
- **Needs split**: No
- **Issues**: Exercise 2 (Dockerfile) assumes Docker installed. Add prerequisite note with fallback option.
- **Changes made**: Changelog updated only

### v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match (split sub-part)
- **Time estimate**: 80-100 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: Integration testing and deployment configuration. Practical capstone continuation.
- **Unresolved from prior reviews**: Dockerfile exercise assumes Docker installed -- add prerequisite note with fallback (e.g., write Dockerfile without building, or use cargo-dist as alternative)
- **New findings**: None
- **Recommendation**: Add Docker prerequisite note with fallback when task content is next updated

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 85-110min (Heavy)
- **Needs split**: No
- **Progression**: Integration testing and deployment configuration. Practical capstone continuation.
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: Minor: Docker prerequisite note with fallback (write Dockerfile without building) needed
- **Recommendation**: Add Docker prerequisite note with fallback option when task content is next updated

### v11-fix - Added Docker prerequisite note with fallback (2026-03-04)
- Added note: write Dockerfile without building if Docker unavailable
- **Resolves**: Minor item from v11

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 85-110min
- **Pacing**: Heavy
- **Issues**: Ex 1 integration test suite is very large (3 sub-tests, each 20-30min)
- **Recommendations**: Split Ex 1 into core test (CRUD happy path) + [STRETCH] error/auth tests
- **Changes made**: Changelog updated only

### v12-fix - Task file changes applied (2026-03-04)
- Restructured Exercise 1 integration test suite: CRUD happy-path test is now the required core (~30-40min), auth flow test and error cases test marked as [STRETCH] sub-items to reduce required scope from ~60-90min to ~30-40min

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 80-100min
- **Pacing**: Heavy
- **Issues**: Docker assumed as external knowledge. Pragmatic fallback provided (write Dockerfile without building). Exercise 1 STRETCH tests (auth flow, error cases) appropriately labeled
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 80-100min
- **Pacing**: Heavy
- **Issues**: None
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 80-100min. **Pacing**: Heavy. **Changes**: Added clarifying note to Exercise 2 that it has two distinct parts (health endpoint Rust code + Dockerfile config). **Why**: Exercise conflates application code with deployment configuration; separating into sub-tasks improves clarity.
