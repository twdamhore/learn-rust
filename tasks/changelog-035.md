# Changelog - Lesson 035: String in depth - UTF-8, indexing, manipulation

## Section 8: Collections & Iterators

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: String as Vec<u8> wrapper, UTF-8 encoding and indexing, chars vs bytes iteration, safe slicing, common string methods
- **Exercises added**: chars vs bytes on multi-language string, safe substring with char boundary checking, three approaches to string building, CSV line parser

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Moderate for 1-hour lesson
- **Issues found**:
  - Overlaps with lesson 018 on string topics (018 = which type to use, 035 = internal structure)
- **Recommendations**: None - overlap is intentional and complementary

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Moderate (~1 hr) for 1-2 hour target
- **Changes noted**: Intentional and complementary overlap with lesson 18 (18 = when to use which type; 35 = internal structure and manipulation). No issues.
- **Why**: Well-justified deeper dive.
- **v4 recommendations status**: N/A.
- **Gradual progression**: Steady.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~50-60 min
- **Pacing verdict**: Moderate
- **Split needed**: No
- **Key issues**: None - intentional complement to lesson 018 (018 = which type, 035 = internals); CSV parser may cause borrow checker issues
- **Action taken**: Changelog updated with pacing assessment

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Moderate (~50-60 min)
- **Status**: No changes needed

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~50-60 min (Moderate)
- **Needs split**: No
- **Progression**: Strong complement to lesson 018. CSV parser exercise is right difficulty for this stage.
- **Issues**: None
- **Changes made**: None

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~50-60 min
- **Pacing**: Good
- **Needs split**: No
- **Issues**: None. Intentional overlap with lesson 18 (18=when to use which, 35=internal structure). Well-justified.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match
- **Time estimate**: 50-60 minutes (Moderate)
- **Needs splitting**: No
- **Pacing context**: Complements lesson 018 well (018=when to use which type, 035=UTF-8 internals and manipulation).
- **Unresolved from prior reviews**: None
- **New findings**: None
- **Recommendation**: No changes needed. Intentional and complementary overlap with lesson 018.

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 60-75min (Moderate)
- **Needs split**: No
- **Progression**: Slightly underestimated in prior reviews. UTF-8 char boundaries genuinely new for Java/Go devs. CSV parser (Ex 4) may trigger borrow checker issues.
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: None
- **Recommendation**: No changes needed. Monitor CSV parser exercise for borrow checker friction at lesson time.

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 60-80min
- **Pacing**: Good
- **Issues**: Minor — CSV parser (Ex 4) may trigger borrow checker friction.
- **Recommendations**: Consider providing lifetime hint for Ex 4.
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 55-70min
- **Pacing**: Good
- **Issues**: Some overlap with lesson 018 (String bridge lesson) — intentional deepening. CSV parser in Exercise 4 may trigger borrow checker friction — consider providing lifetime hint
- **Changes made**: Changelog updated only

### v13-fix - Applied pending task file fixes (2026-03-04)
- Added lifetime/borrow hint to Exercise 4 (CSV parser)
- **Why**: CSV parsing with string slices commonly triggers borrow checker friction at this stage
- **Resolves**: v12 and v13 recommendation

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 55-70min
- **Pacing**: Medium
- **Issues**: No issues
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 55-70min. **Pacing**: Medium. **Issues**: None — good complement to lesson 018. **Changes**: Changelog only.
