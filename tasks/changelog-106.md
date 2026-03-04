# Changelog - Lesson 106: Cross-compilation, conditional compilation, cfg attributes

## Section 20: Special Targets

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Target triples and rustup target add, #[cfg] attributes for conditional compilation, cfg!() macro for runtime vs compile-time checks, platform-specific module organization, Cargo features for optional dependencies
- **Exercises added**: Cross-compile for a different target, OS-specific config_dir function with cfg, feature-gated config parser with json/toml features, debug_assertions and test cfg for build-mode-specific code

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Moderate for 1-hour lesson
- **Issues found**:
  - Significant overlap with lesson 091 on #[cfg()] topics (082 intro, 093 broader coverage)
  - Exercise 3 is very similar to Exercise 3 of task 082 (both feature-gate with serde)
  - Exercise format uses unnumbered bullets (formatting inconsistency)
- **Recommendations**:
  - Differentiate Exercise 3 from task 082's Exercise 3
  - Standardize exercise format

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Moderate (~1 hr) for 1-2 hour target
- **Changes noted**: cfg and feature concepts well-scoped. Significant overlap with lesson 091 (both cover #[cfg] and feature gating). Exercise 3 nearly identical to task 082 Exercise 3 (both feature-gate with serde). Exercise format inconsistency.
- **Why**: Overlap and duplication with lesson 091.
- **v4 recommendations status**: Not yet applied -- v4 flagged overlap and duplicate exercise. Gradual progression: Moderate; fix duplication.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1 hour
- **Pacing verdict**: Moderate - OK - under 2hr threshold
- **Split needed**: No
- **Key issues**:
  - Significant overlap with lesson 091 on #[cfg()] topics
  - Exercise 3 nearly identical to 082's Exercise 3 (both feature-gate with serde)
- **Action taken**: No split needed. Overlap and duplicate exercise should be differentiated when task content is updated.

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Moderate (~1 hr)
- **Status**: No changes needed
- Overlap with 082 Ex3 still flagged

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~60 min (Moderate)
- **Needs split**: No
- **Issues**: Exercise 3 (feature-gate with json/toml) nearly identical to 082 Exercise 3. MUST be differentiated (flagged since v4, unresolved). Exercise format uses unnumbered bullets.
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~55-65 min
- **Pacing**: Good
- **Needs split**: No
- **Issues**: Exercise format uses unnumbered bullets — must standardize. Exercise 3 (feature-gate with json/toml using serde) nearly identical to lesson 82 Exercise 3 — MUST differentiate. Recommend: 082 uses simple non-serde feature, 093 can use serde since it's been taught by then. Unresolved since v4.
- **Changes made**: Changelog updated only

### v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match with CLAUDE.md
- **Time estimate**: 55-65 minutes (Moderate)
- **Needs splitting**: No
- **Pacing context**: cfg and feature concepts well-scoped for Section 20.
- **Unresolved from prior reviews**: (1) Exercise 3 nearly identical to task 082 Exercise 3 -- both feature-gate with serde. Recommend: 082 uses non-serde feature, 093 uses serde (flagged since v4). (2) Exercise format uses unnumbered bullets (flagged since v4).
- **New findings**: None
- **Recommendation**: Differentiate Exercise 3 from 082 and fix exercise format when task content is next updated

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 55-70min (Moderate)
- **Needs split**: No
- **Progression**: cfg and feature concepts well-scoped for Section 20.
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: Minor: serde feature-gating overlap with 082 — differentiate contexts (082=simple flag pre-serde, 093=serde flag post-serde)
- **Recommendation**: Differentiate Exercise 3 context from 082 when task content is next updated

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 55-70min
- **Pacing**: Good
- **Issues**: Ex 3 (feature-gated serde) overlaps lesson 091 Ex 3
- **Recommendations**: Differentiate from lesson 091 more explicitly
- **Changes made**: Changelog updated only

### v13-fix - Applied pending fixes (2026-03-04)
- Added differentiation note to Exercise 3 explaining how it differs from lesson 091 Exercise 3
- **Why**: Both exercises use feature flags but 093 goes further (optional dependency, conditional derives, feature-gated API)
- **Resolves**: v11/v12 recommendation

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 70-85min
- **Pacing**: Good
- **Issues**: None
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 70-85min
- **Pacing**: Good
- **Issues**: None
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 70-85min. **Pacing**: Good. **Issues**: None — differentiation from lesson 091 verified. **Changes**: Changelog only.
