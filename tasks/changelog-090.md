# Changelog - Lesson 090: Database - sqlx, connection pools, migrations

## Section 19: Ecosystem & Tooling

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: sqlx with SQLite setup, compile-time checked queries with query!/query_as!, migrations with sqlx migrate, connection pooling with SqlitePool, async CRUD operations
- **Exercises added**: Set up SQLite with migrations for a tasks table, implement full CRUD module with compile-time checked queries, integration test with in-memory database, repository pattern with trait abstraction

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - sqlx compile-time query checking (DATABASE_URL, sqlx prepare) is a notorious setup pain point
  - Exercise 4 (repository pattern with async trait methods) requires async-trait crate or experimental async fn in traits
  - Exercise format uses unnumbered bullets (formatting inconsistency)
- **Recommendations**:
  - Standardize exercise format
  - Note async-trait dependency for Exercise 4
  - Allocate extra time for initial sqlx setup

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~1.5-2 hr) for 1-2 hour target
- **Changes noted**: sqlx compile-time checking (DATABASE_URL, sqlx prepare) is notorious setup pain point -- 20-30 min alone. Exercise 4 silently requires async-trait crate or Rust 1.75+ RPITIT. Exercise format inconsistency.
- **Why**: Setup complexity underestimated; hidden dependency
- **v4 recommendations status**: Not yet applied -- v4 recommended noting async-trait dependency and extra setup time. Gradual progression: Heavy; setup-intensive.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.75-2.5 hours
- **Pacing verdict**: Heavy - TRIM (not split)
- **Split needed**: No
- **Key issues**:
  - sqlx setup takes 20-30 min alone (DATABASE_URL, compile-time checking, sqlx prepare)
  - Exercise 4 silently requires async-trait crate or Rust 1.75+ (RPITIT)
  - Exercise format inconsistent (unnumbered bullets)
- **Action taken**: Note setup overhead and hidden async-trait dependency in task content when updated. No split needed -- setup awareness and noting the dependency bring expectations in line.

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Heavy (~1.5-2 hr)
- **Status**: No changes needed
- Within relaxed threshold. SQLx setup pain and hidden async-trait dependency still flagged.

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~100-120 min (Heavy, tight under 2hr)
- **Needs split**: No
- **Issues**: Exercise format uses unnumbered bullets. Must add DATABASE_URL setup warning. Exercise 4 needs async-trait crate note or Rust 1.75+ RPITIT requirement.
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~100-120 min
- **Pacing**: Heavy (tight at upper boundary)
- **Needs split**: No, but needs content fixes
- **Issues**: Exercise format uses unnumbered bullets — must standardize. sqlx compile-time query checking setup (DATABASE_URL, sqlx prepare) is notorious pain point that can consume 20-30 min — must add explicit setup instructions. Exercise 4 (repository pattern with async trait methods) silently requires async-trait crate or Rust 1.75+ RPITIT — must document. Unresolved since v4.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match
- **Time estimate**: 100-120 minutes (Heavy-Borderline)
- **Needs splitting**: No (if trimmed and setup documented)
- **Pacing context**: Section 19 closer. Setup-heavy but database concepts transfer from Java/Go.
- **Unresolved from prior reviews**: (1) Exercise format uses unnumbered bullets, (2) sqlx setup needs detailed instructions (DATABASE_URL, sqlx prepare), (3) Exercise 4 silently needs async-trait or Rust 1.75+, (4) Exercise 4 should be [STRETCH]
- **New findings**: None
- **Recommendation**: Standardize exercise format, add sqlx setup guide, document async-trait requirement, mark Exercise 4 [STRETCH] before lesson start

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 100-130min (Heavy-Borderline)
- **Needs split**: No (within 2hr with setup)
- **Progression**: Section 19 closer. Database concepts transfer from Java/Go. Setup-heavy.
- **Changelog reconciliation**: Prerequisites section with setup commands present. Exercise 4 already [STRETCH]. async-trait less critical with Rust 1.75+ RPITIT.
- **Genuinely unresolved**: None
- **Recommendation**: No action needed — setup instructions, Exercise 4 [STRETCH], and async-trait notes already present in task file

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 100-130min
- **Pacing**: Heavy (borderline OVERLOADED)
- **Issues**: (1) sqlx setup can burn 20-30min. (2) Ex 4 async trait needs RPITIT (Rust 1.75+) or async-trait crate — not noted.
- **Recommendations**: Add setup time warning; note RPITIT/async-trait for Ex 4; if setup struggles, defer Ex 3 to lesson 096
- **Changes made**: Changelog updated only

### v12-fix - Task file changes applied (2026-03-04)
- Added setup time warning after Prerequisites section about sqlx compile-time query checking taking 20-30 minutes on first encounter
- Added async-trait/Rust 1.75+ RPITIT note to Exercise 4 (repository pattern with async trait methods)

### v13 - Full curriculum pacing review and split (2026-03-04)
- Reviewed all 100+ tasks for realistic human pacing (1-2hr OK, split if >2hr)
- **Estimated time**: ~2.5 hours (100-130 min exercises + 20-30 min setup)
- **Decision**: SPLIT into task-090a.md and task-090b.md
- **Rationale**: sqlx setup alone takes 20-30 min (noted since v4). Full CRUD + integration tests + repository pattern is too much for one session even with the setup budgeted. 12 prior reviews flagged this as Heavy-to-OVERLOADED.
- **090a covers**: SQLite setup, migrations, basic queries (2 exercises, includes setup time)
- **090b covers**: Complete CRUD, integration tests, repository pattern [STRETCH] (3 exercises)
- **Key improvement**: Basic queries separated from full CRUD to let learner absorb setup before building more
- **Status**: SUPERSEDED -- see task-090a.md and task-090b.md

### v13-review - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: N/A
- **Pacing**: SUPERSEDED
- **Issues**: SUPERSEDED by 090a/090b
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. Correctly superseded. **Changes**: Changelog only.
