# Changelog - Lesson 077: Advanced macro_rules! - TT munching, push-down accumulation

## Section 15: Macros

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: TT munching pattern, push-down accumulation, recursive macros, internal @-prefixed helper rules, macro limitations
- **Exercises added**: Counting macro with TT munching, nested Option type builder, reverse! macro with push-down accumulation, calc! DSL macro

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - Exercise 4 (calc! DSL) is ambitious for someone just learning TT munching
- **Recommendations**:
  - Make calc! DSL a stretch goal

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~1.5 hr) for 1-2 hour target
- **Changes noted**: TT munching and push-down accumulation require careful mental modeling. calc! DSL (Exercise 4) is ambitious for first encounter
- **Why**: Advanced macro patterns need more time
- **v4 recommendations status**: Not yet applied -- v4 recommended making calc! DSL a stretch goal. Gradual progression: Heavy spike after two moderate lessons

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.5 hours
- **Pacing verdict**: Heavy - under 2hr threshold
- **Split needed**: No
- **Key issues**:
  - TT munching and push-down accumulation need careful mental modeling
  - calc! DSL (Exercise 4) is ambitious for first encounter
- **Action taken**: No split required. Previous v4 recommendation to make calc! DSL a stretch goal should be applied when lesson is started

### v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Heavy (~1.5 hr)
- **Status**: No changes needed under relaxed threshold
- calc! DSL exercise should be made a stretch goal when lesson is started

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~80-100 min (Heavy)
- **Needs split**: No
- **Issues**: Exercise 4 (calc! DSL) should be marked [STRETCH] (flagged since v4, unresolved).
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~80-100 min
- **Pacing**: Heavy
- **Needs split**: No
- **Issues**: Exercise 4 (calc! DSL) is ambitious for first TT munching encounter. Should be [STRETCH]. @-prefixed internal rules need clear explanation. Noticeable difficulty spike after two moderate lessons. Unresolved since v4.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match
- **Time estimate**: 80-100 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: Noticeable difficulty spike after two moderate lessons (068, 069). TT munching and push-down accumulation require careful mental modeling.
- **Unresolved from prior reviews**: (1) Exercise 4 (calc! DSL) should be [STRETCH] (unresolved since v4), (2) @-prefixed internal rules need clearer explanation
- **New findings**: None
- **Recommendation**: Mark Exercise 4 as [STRETCH] and add explanatory comments for @-prefixed internal rules when lesson is started

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: ~90min (Heavy)
- **Needs split**: No
- **Progression**: Noticeable difficulty spike after two moderate lessons (068, 069)
- **Changelog reconciliation**: "Exercise 4 should be [STRETCH]" — already in task file. Resolved.
- **Genuinely unresolved**: `@`-prefixed internal rules need clearer explanation during teaching
- **Recommendation**: Provide clearer `@`-prefixed internal rules explanation at lesson start

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 80-100min
- **Pacing**: Heavy
- **Issues**: @-prefixed internal rules need clearer explanation
- **Recommendations**: Provide explanation of @ convention at lesson start
- **Changes made**: Changelog updated only

### v13-fix - Applied pending fixes (2026-03-04)
- Added explanation of `@`-prefixed internal rules convention in Objective 4
- **Why**: Without explanation, the `@` prefix pattern is opaque to learners
- **Resolves**: v11/v12 recommendation (high priority)

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 70-90min
- **Pacing**: Good (borderline Heavy)
- **Issues**: None
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 75-95min
- **Pacing**: Heavy
- **Issues**: None
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 80-95min. **Pacing**: Heavy. **Changes**: Added hint to Exercise 3 showing initial `@acc` call transformation pattern for push-down accumulation. **Why**: Learner's first encounter with push-down accumulation pattern; the hint reduces the discovery burden by showing the entry point.
