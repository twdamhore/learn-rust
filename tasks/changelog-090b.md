# Changelog - Lesson 090b: Database Part B - CRUD, Testing, and Repository Pattern

## Section 19: Ecosystem & Tooling

### v1 - Created from split (2026-03-04)
- Split from task-090 during v13 full curriculum pacing review
- **Why split**: Original lesson 090 rated ~2.5 hours with setup time. CRUD + integration tests + repository pattern too much for one session.
- **What this part covers**: Complete CRUD operations (update, delete), connection pools, integration testing with in-memory SQLite, repository pattern [STRETCH]
- **Exercises**: Complete CRUD module (extends 090a queries), integration tests with in-memory DB, repository pattern [STRETCH] (original Ex 4 with async-trait note retained)
- **Estimated time**: ~1-1.5 hours
- **Prerequisite**: 090a

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 70-90min
- **Pacing**: Good
- **Issues**: Exercise 3 (STRETCH) uses async-trait crate without explanation — add brief note about what the crate does (proc macro desugaring async trait methods into Pin<Box<dyn Future>>)
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 70-90min
- **Pacing**: Good
- **Issues**: None
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 70-90min. **Pacing**: Good. **Issues**: None — async-trait note verified. **Changes**: Changelog only.
