# Changelog - Lesson 096: CI/CD for Rust - GitHub Actions, caching, release builds

## Section 18: Testing & Quality

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: GitHub Actions workflow for Rust, dependency caching with rust-cache, CI matrix across toolchains and OS, automated release builds and publishing, cross-compilation with cross
- **Exercises added**: Basic CI workflow YAML, caching and matrix strategy, release workflow with binary uploads, cross-compilation for musl and ARM64

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Moderate-to-Heavy for 1-hour lesson
- **Issues found**:
  - Primarily a DevOps/CI lesson rather than Rust language lesson
  - Cannot be easily tested locally without pushing to GitHub or using `act`
  - Minor inconsistency: objectives mention `beta` but Exercise 2 only uses stable/nightly
- **Recommendations**:
  - Note that local testing with `act` is an option

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Moderate-to-Heavy (~1-1.25 hr) for 1-2 hour target
- **Changes noted**: Primarily DevOps/CI rather than Rust language. Cannot test locally without GitHub or act. Objectives mention beta but Exercise 2 only uses stable/nightly (minor inconsistency).
- **Why**: More DevOps than Rust; limited hands-on testing
- **v4 recommendations status**: Not yet applied -- v4 noted act for local testing and beta inconsistency. Gradual progression: Conceptual shift to DevOps.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1-1.25 hours
- **Pacing verdict**: Moderate - OK - under 2hr threshold
- **Split needed**: No
- **Key issues**:
  - More DevOps than Rust; exercises hard to test locally without pushing to GitHub
  - Objectives mention beta toolchain but Exercise 2 only uses stable/nightly
- **Action taken**: No changes needed. Issues are minor and can be addressed in task content updates.

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Moderate (~1-1.25 hr)
- **Status**: No changes needed

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~65-75 min (Moderate)
- **Needs split**: No
- **Issues**: Beta toolchain mentioned in Objective 3 but absent from Exercise 2 matrix. Consider suggesting `act` for local CI testing.
- **Changes made**: None

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~65-75 min
- **Pacing**: Good
- **Needs split**: No
- **Issues**: Primarily DevOps lesson. Objective 3 mentions beta toolchain but Exercise 2 only uses stable/nightly (inconsistency). Exercise 4 (cross-compilation for musl + ARM64) may be challenging — consider optional. Suggest act for local testing.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match
- **Time estimate**: 65-75 minutes (Moderate)
- **Needs splitting**: No
- **Pacing context**: DevOps-focused lesson. Concepts transfer from Java/Go CI experience.
- **Unresolved from prior reviews**: (1) Objective 3 mentions beta but Exercise 2 only uses stable/nightly, (2) Suggest `act` for local CI testing, (3) Exercise 4 cross-compilation should be [OPTIONAL]
- **New findings**: None
- **Recommendation**: Fix beta inconsistency, add `act` note, mark Exercise 4 [OPTIONAL] before lesson start

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 60-75min (Moderate)
- **Needs split**: No
- **Progression**: DevOps-focused; familiar from Java/Go CI experience
- **Changelog reconciliation**: "Exercise 4 should be [OPTIONAL]" -- already applied in task file. Resolved.
- **Genuinely unresolved**: None
- **Recommendation**: Minor: beta inconsistency (Objective 3 says "beta" but Exercise 2 matrix only uses stable/nightly)

### v11-fix - Fixed beta inconsistency (2026-03-04)
- Added beta to Exercise 2 toolchain matrix to match Objective 3
- **Resolves**: Minor item from v11

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 60-75min
- **Pacing**: Good
- **Issues**: None
- **Recommendations**: Minor — mention `act` for local GitHub Actions testing
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 70-90min
- **Pacing**: Good
- **Issues**: Primarily YAML/CI configuration rather than Rust code. Without a GitHub remote, workflows cannot be tested — lesson acknowledges this. Consider adding note that this is infrastructure/workflow focused
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 65-80min
- **Pacing**: Moderate
- **Issues**: None
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 65-80min. **Pacing**: Moderate. **Issues**: None — DevOps-focused, acceptable trade-off. **Changes**: Changelog only.

### v16 (2026-03-04) — Full curriculum review (119 lessons)
- No changes needed — reviewed for pacing, progression, and forward references

### v17 (2026-03-04) — Human-learning clarity pass
- Added a dedicated Prerequisites section for repository access, YAML familiarity, and release permissions.
- Goal: reduce hidden setup blockers before starting CI/CD exercises.
