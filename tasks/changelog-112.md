# Changelog - Lesson 112: Axum Web API Basics
## Section 21: Capstone Projects

### v1 - Created from split (2026-03-03)
- Split from original lesson 112 which was rated OVERLOADED (~3-4 hrs)
- **Reason for split**: CRITICAL -- axum is never taught in any previous lesson; learner must learn axum from scratch while simultaneously building complete REST API with CRUD, SQLite, and JWT auth; jsonwebtoken crate also entirely new; most overloaded task in 081-100
- **Scope**: Introduction to axum (Router, handlers, extractors, State), in-memory CRUD API, JSON request/response, structured error responses. Uses in-memory storage only -- no database or auth. This provides the axum introduction that was missing from the curriculum.
- **Estimated time**: ~1-1.5 hours

### v2 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and changelog for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~80-95 min (Moderate-Heavy)
- **Needs split**: No
- **Progression**: Fills the critical axum introduction gap. In-memory storage is the right approach.
- **Issues**: Add brief note explaining why Arc<Mutex<>> is needed for shared state.
- **Changes made**: None

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~80-95 min
- **Pacing**: Good
- **Needs split**: No
- **Issues**: Minor: Should add note explaining why Arc<Mutex<>> needed for shared state (connect to lesson 60). Fills critical curriculum gap — provides missing axum introduction. In-memory storage was key insight. Prerequisites correctly listed.
- **Changes made**: Changelog updated only

### v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match (split sub-part)
- **Time estimate**: 80-95 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: Fills critical axum introduction gap. In-memory storage keeps focus on learning axum, not database setup.
- **Unresolved from prior reviews**: None
- **New findings**: Minor -- add note explaining why Arc<Mutex<>> is needed for shared state, connecting back to lesson 065 (Shared state -- Mutex, RwLock, Arc<Mutex<>>)
- **Recommendation**: Add Arc<Mutex<>> explanation note when task content is next updated

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 80-100min (Heavy)
- **Needs split**: No
- **Progression**: Excellent split — provides the missing axum introduction. Should note connection back to lesson 065 (Arc<Mutex<>>).
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: None
- **Recommendation**: Add note connecting Arc<Mutex<>> usage back to lesson 065 when task content is next updated

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 80-100min
- **Pacing**: Heavy
- **Issues**: Task file doesn't explain why Arc<Mutex<Vec>> needed for shared state
- **Recommendations**: Add brief note connecting back to lesson 065
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 80-100min
- **Pacing**: Heavy
- **Issues**: Axum web framework introduced for first time during a capstone project — no prior standalone axum lesson exists (unlike clap/serde/sqlx which get dedicated lessons). Lesson is self-aware about this and provides axum introduction, but learner is simultaneously learning framework AND building project
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 80-100min
- **Pacing**: Heavy
- **Issues**: Lesson 065 (shared state) not listed as prerequisite despite Arc<Mutex<Vec>> usage; no note connecting back to lesson 065
- **Changes made**: Added lesson 065 prerequisite and Arc<Mutex> note in Exercise 1, task file updated

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 80-100min. **Pacing**: Heavy. **Changes**: Added axum version note ("0.8") and Cargo.toml dependency scaffold (axum, tokio, serde, serde_json). **Why**: Axum API changes significantly between versions; learner needs version guidance and dependency setup to avoid frustration.
