# Changelog - Lesson 061: Send and Sync traits, thread safety guarantees

## Section 13: Concurrency

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Send trait for cross-thread transfer, Sync trait for shared references, which std types are/aren't Send+Sync, using Send+Sync bounds in generics, auto-trait derivation
- **Exercises added**: Rc !Send compiler error vs Arc, Cell !Sync error vs AtomicI32, compile-time assertions on custom structs with various fields, thread-safe trait objects with Send+Sync bounds

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Moderate for 1-hour lesson
- **Issues found**: None
- **Recommendations**: None - well-scoped, natural progression from lesson 060

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Moderate (~1 hr) for 1-2 hour target
- **Changes noted**: No issues. Exercises focus on observing compiler errors and understanding -- short and focused
- **Why**: Novel concepts but low implementation burden
- **v4 recommendations status**: N/A. Gradual progression: Well-paced; appropriate

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1 hour
- **Pacing verdict**: Moderate - under 2hr threshold
- **Split needed**: No
- **Key issues**: None
- **Action taken**: No changes needed. Low implementation burden -- mostly observing compiler errors

### v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Moderate (~1 hr)
- **Status**: No changes needed
- Low implementation burden remains well under relaxed threshold

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~60 min (Moderate)
- **Needs split**: No
- **Progression**: Conceptual lesson with low implementation burden. Good relief before heavy 062.
- **Issues**: None
- **Changes made**: None

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~55-65 min
- **Pacing**: Good
- **Needs split**: No
- **Issues**: None
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match
- **Time estimate**: 55-65 minutes (Moderate)
- **Needs splitting**: No
- **Pacing context**: Good conceptual relief before heavy lesson 062. Low implementation burden -- mostly observing compiler errors.
- **Unresolved from prior reviews**: None
- **New findings**: None
- **Recommendation**: No changes needed

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: ~60min (Moderate)
- **Needs split**: No
- **Progression**: Good breather before heavy 062
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: None
- **Recommendation**: No action needed

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 55-65min
- **Pacing**: Good
- **Issues**: None
- **Recommendations**: None
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 55-70min
- **Pacing**: Good
- **Issues**: Exercise 2 uses AtomicI32 (lesson 62) as fix for Cell<i32> that is !Sync — add preview note for the atomic type
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 55-70min
- **Pacing**: Moderate
- **Issues**: Added AtomicI32 preview note to Exercise 2 (forward reference to lesson 062)
- **Changes made**: Task file updated — added note to Exercise 2 explaining AtomicI32 preview and Arc<Mutex<i32>> alternative

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 55-70min. **Pacing**: Moderate. **Issues**: None — good conceptual breather. **Changes**: Changelog only.
