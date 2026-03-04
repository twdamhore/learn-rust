# Changelog - Lesson 023: The derive attribute - Debug, Clone, PartialEq, Eq, Hash

## Section 5: Structuring Data

### v1 - Initial creation
- Lesson added to curriculum
- **NEW**: Bridging lesson added after gap analysis

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and bridging lesson tag all align with curriculum
- Correctly tagged as [NEW - bridging lesson] matching CLAUDE.md [NEW] designation
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Understand #[derive] syntax, Debug for printing, Clone/Copy for duplication, PartialEq/Eq for comparison, Hash for HashMap keys
- **Exercises added**: Student/Classroom Debug printing with {:?} and {:#?}, Clone vs Copy with Point and Label, equality comparison with Coordinate, HashMap key usage with Tile struct requiring Hash+Eq+PartialEq

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Moderate for 1-hour lesson
- **Issues found**: None
- **Recommendations**: None - well-scoped bridging lesson, each exercise targets one derive trait

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Moderate (~1 hr) for 1-2 hour target
- **Changes noted**: Well-scoped bridging lesson. Each exercise targets one derive trait. Copy vs Clone is the only genuinely new concept.
- **Why**: Java/Go devs will find Debug/PartialEq natural.
- **v4 recommendations status**: N/A. Gradual progression: Smooth start to Section 5.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~50-60 min
- **Pacing verdict**: Moderate
- **Split needed**: No
- **Key issues**: None - derive attribute is natural for Java/Go devs (Debug ~ toString, PartialEq ~ equals)
- **Action taken**: Changelog updated with pacing assessment

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Moderate (~50-60 min)
- **Status**: No changes needed
- Good breather lesson

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~50-60 min (Moderate)
- **Needs split**: No
- **Progression**: Comfortable on-ramp to Section 5. Low cognitive load.
- **Issues**: None
- **Changes made**: None

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~50-60 min
- **Pacing**: Good
- **Needs split**: No
- **Issues**: None
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match
- **Time estimate**: 50-60 minutes (Moderate)
- **Needs splitting**: No
- **Pacing context**: Clean lesson. Java/Go devs find Debug ~ toString and PartialEq ~ equals natural. Good on-ramp to Section 5.
- **Unresolved from prior reviews**: None
- **New findings**: None
- **Recommendation**: No changes needed

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 50-60min (Moderate)
- **Needs split**: No
- **Progression**: Cleanest lesson in the 021-033 range. Bridging lesson fits well as on-ramp to Section 5.
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: None
- **Recommendation**: No changes needed

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 50-60min
- **Pacing**: Good
- **Issues**: None
- **Recommendations**: None
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 50-60min
- **Pacing**: Good
- **Issues**: Exercise 4 uses HashMap (lesson 36) — minor forward reference; add brief note
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 50-60min
- **Pacing**: Light-Medium
- **Issues**: None
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, progression, and content quality
- **Estimated time**: 50-60min
- **Pacing**: Light-Medium
- **Changes made**: Added HashMap usage note to Exercise 4 explaining minimal HashMap usage needed and pointing to lesson 038
- **Why**: Minor forward reference to HashMap (lesson 038) lacked usage context
