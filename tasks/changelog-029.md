# Changelog - Lesson 029: Cargo workspaces, features, profiles

## Section 6: Project Organization

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Create workspaces with multiple packages, workspace member dependencies with path, cargo features for conditional compilation, build profiles (dev/release/custom), comparison with Java/Go multi-module projects
- **Exercises added**: Workspace with core/cli/server members, feature flags with #[cfg(feature)] and default features, build profile configuration comparing debug vs release binary sizes, workspace-level cargo commands (test/clippy/check --workspace)

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - Workspace setup (Exercise 1) requires creating three separate crates with inter-dependencies
  - Combined with feature flags and build profiles, this is dense for 1 hour
- **Recommendations**:
  - Consider making Exercise 3 (custom build profiles) lighter or optional

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~1.5 hr) for 1-2 hour target
- **Changes noted**: Three distinct Cargo concepts (workspaces + features + profiles). Exercise 1 (workspace with 3 crate members) is substantial setup. Exercise 3 (custom build profiles) is nice-to-know, not essential.
- **Why**: Too many concepts in one lesson.
- **v4 recommendations status**: Not yet applied -- v4 recommended making Exercise 3 optional. Gradual progression: Heavy; three concepts is ambitious.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.5 hr
- **Pacing verdict**: Heavy - under 2hr threshold
- **Split needed**: No
- **Key issues**:
  - Three Cargo concepts in one lesson (workspaces, features, profiles)
  - Exercise 1 requires creating 3 crates
  - Exercise 3 (custom build profiles with LTO) should be optional
- **Action taken**: Changelog updated with pacing assessment

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Heavy (~1.5-2 hr)
- **Status**: No changes needed
- No changes needed under relaxed threshold. Three Cargo concepts acceptable at relaxed pace.

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~90-120 min (Heavy)
- **Needs split**: No
- **Progression**: Three Cargo concepts (workspaces, features, profiles) is ambitious but achievable.
- **Issues**: Exercise 3 (custom build profiles) should be marked [STRETCH] (flagged since v4, unresolved).
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~90-120 min
- **Pacing**: Heavy
- **Needs split**: No (upper edge)
- **Issues**: Three Cargo concepts in one lesson (workspaces, features, profiles). Exercise 3 (custom build profiles with LTO comparison) should be [STRETCH]. Unresolved since v4.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match
- **Time estimate**: 90-120 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: Three distinct Cargo concepts (workspaces, features, profiles) is ambitious. Exercise 1 (workspace with 3 crate members) is substantial setup alone.
- **Unresolved from prior reviews**: Exercise 3 (custom build profiles with LTO) should be marked [STRETCH]. Flagged since v4, never applied.
- **New findings**: None
- **Recommendation**: Apply [STRETCH] tag to Exercise 3 when lesson begins

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 90-120min (Heavy, upper edge)
- **Needs split**: No
- **Progression**: Workspace setup is mechanically heavy; skeleton structures would help.
- **Changelog reconciliation**: "Exercise 3 should be [STRETCH]" flagged since v4 as never applied -- but task file Exercise 3 IS already tagged [STRETCH]. Resolved.
- **Genuinely unresolved**: None
- **Recommendation**: No changes needed

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 90-120min
- **Pacing**: Heavy
- **Issues**: Three distinct Cargo concepts in one lesson. Ex 3 [STRETCH].
- **Recommendations**: None
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 80-100min
- **Pacing**: Heavy
- **Issues**: Covers 3 large topics (workspaces, features, profiles) with significant boilerplate. Exercise 1 requires 3-member workspace from scratch (4+ Cargo.toml files). Could benefit from starter workspace skeleton like lesson 25's directory structures
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 80-100min
- **Pacing**: Heavy
- **Issues**: None (v13 skeleton concern resolved)
- **Changes made**: Added workspace skeleton Cargo.toml template (root + member) to Exercise 1, task file updated

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 80-100min. **Pacing**: Heavy. **Changes**: Renamed workspace member `core` to `shared` throughout exercises and skeleton templates. **Why**: `core` conflicts with Rust's built-in `core` crate, potentially confusing learner.
