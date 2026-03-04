# Changelog - Lesson 034: Vec<T> - creating, updating, accessing, memory model

## Section 8: Collections & Iterators

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: vector creation methods, mutation operations, safe vs panicking access, memory model (ptr+len+cap), iteration modes, Java/Go comparison
- **Exercises added**: capacity growth observation, safe vs unsafe access, stack implementation with Vec, sorting and deduplication

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Moderate for 1-hour lesson
- **Issues found**:
  - 6 objectives is more than usual, but Vec is familiar territory for Java/Go developers
- **Recommendations**: None - well-scoped given learner's background

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Moderate (~1 hr) for 1-2 hour target
- **Changes noted**: 6 objectives (more than most) but Vec is extremely familiar for Java/Go devs (ArrayList, slices). Memory model (ptr+len+cap) maps directly to Go slice internals. Balanced parentheses exercise is a classic.
- **Why**: Familiar territory despite high objective count.
- **v4 recommendations status**: N/A.
- **Gradual progression**: Good section opener.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~50-60 min
- **Pacing verdict**: Moderate
- **Split needed**: No
- **Key issues**: None despite 6 objectives - Vec is extremely familiar (ArrayList/Go slices); good section opener
- **Action taken**: Changelog updated with pacing assessment

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Moderate (~50-60 min)
- **Status**: No changes needed

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~50-60 min (Moderate)
- **Needs split**: No
- **Progression**: Well-scoped opener. Vec maps directly to ArrayList/Go slices.
- **Issues**: None
- **Changes made**: None

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~50-60 min
- **Pacing**: Good
- **Needs split**: No
- **Issues**: None. Despite 6 objectives, Vec maps to Java ArrayList and Go slices. Balanced parentheses exercise is a well-chosen classic.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match
- **Time estimate**: 50-60 minutes (Moderate)
- **Needs splitting**: No
- **Pacing context**: Good section opener. Vec is familiar from Java (ArrayList) and Go (slices).
- **Unresolved from prior reviews**: None
- **New findings**: None
- **Recommendation**: No changes needed. Well-scoped despite 6 objectives due to learner's prior experience.

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 50-60min (Moderate)
- **Needs split**: No
- **Progression**: Solid section opener. Vec maps directly to ArrayList (Java) and slices (Go).
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: None
- **Recommendation**: No changes needed

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 50-65min
- **Pacing**: Good
- **Issues**: None
- **Recommendations**: None
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 60-75min
- **Pacing**: Good
- **Issues**: Exercise 3 is effectively two exercises (stack impl + parentheses checker) — consider splitting or making checker part STRETCH
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 60-75min
- **Pacing**: Medium
- **Issues**: Minor Exercise 3 parentheses portion concern (not fixed)
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 60-75min. **Pacing**: Medium. **Changes**: Marked parentheses checker in Exercise 3 as optional extension. **Why**: Exercise 3 effectively contained two exercises (stack + parentheses checker); marking checker as optional gives a clear stopping point.
