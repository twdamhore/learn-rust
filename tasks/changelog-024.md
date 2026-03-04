# Changelog - Lesson 024: Enums - basic, with data, Option<T>

## Section 5: Structuring Data

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Basic C-style enums, data-carrying variants (tuple and struct), Option<T> as null replacement, Option methods (unwrap/map/and_then), comparison with Java enums and Go iota
- **Exercises added**: IpAddr enum with V4/V6 data variants, Message enum mixing all variant types, Option fundamentals with find_first_even, Option chaining with map/and_then for HashMap lookups

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - Covers two major topics: basic enums AND the entire Option<T> API with 8+ methods
  - Learner new to algebraic data types from Java/Go may need more time to absorb enums-with-data
- **Recommendations**:
  - Consider splitting: basic enums + Option core in main exercises, Option chaining methods as stretch

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~1.5-2 hr) for 1-2 hour target
- **Changes noted**: Two major conceptual areas (Rust enums as ADTs + full Option<T> API with 8+ methods). Java/Go devs have never seen enum variants carrying heterogeneous data. Exercise 4 (Option chaining with HashMap and_then) is demanding while absorbing enum concepts.
- **Why**: Enums + full Option API is too much for one lesson.
- **v4 recommendations status**: Not yet applied -- v4 recommended splitting into core (enums + basic Option) and stretch (Option chaining). Gradual progression: Significant spike; should mark Option chaining exercises as stretch.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.5-2 hr
- **Pacing verdict**: Heavy - under 2hr threshold
- **Split needed**: No
- **Key issues**:
  - Two major concepts (algebraic enums + full Option API with 8+ methods)
  - Exercise 4 (Option chaining) is demanding
  - v4 recommendation to mark Option chaining as stretch not applied
- **Action taken**: Changelog updated with pacing assessment

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Heavy (~1.5-2 hr)
- **Status**: No changes needed
- No changes needed under relaxed threshold. Option chaining exercise still flagged as stretch-worthy but within limit.

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~90-120 min (Heavy)
- **Needs split**: No
- **Progression**: Two major conceptual leaps (algebraic enums + full Option API) in one lesson.
- **Issues**: Exercise 4 (Option chaining with and_then on HashMap) should be marked [STRETCH] (flagged since v4, unresolved).
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~90-120 min
- **Pacing**: Heavy
- **Needs split**: No (upper edge)
- **Issues**: Exercise 4 (Option chaining with and_then on HashMap) should be marked [STRETCH]. Flagged since v4, never applied to task file.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match
- **Time estimate**: 90-120 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: Two major concepts (enums as ADTs + full Option API) in one lesson. Java/Go devs have never seen enum variants carrying heterogeneous data.
- **Unresolved from prior reviews**: Exercise 4 (Option chaining with and_then) should be marked [STRETCH]. Flagged since v4, never applied to task file.
- **New findings**: None
- **Recommendation**: Apply [STRETCH] tag to Exercise 4 when lesson begins

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 90-120min (Heavy, upper edge)
- **Needs split**: No
- **Progression**: Two major conceptual areas (enums as ADTs + full Option API). Within 2hr limit with stretch tag.
- **Changelog reconciliation**: "Exercise 4 should be [STRETCH]" flagged since v4 as never applied -- but task file Exercise 4 IS already tagged [STRETCH]. Resolved.
- **Genuinely unresolved**: None
- **Recommendation**: No changes needed

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 90-120min
- **Pacing**: Heavy
- **Issues**: Dense — enums as ADTs + full Option<T> API. Ex 4 is [STRETCH].
- **Recommendations**: None
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 60-75min
- **Pacing**: Good
- **Issues**: Minor if-let forward reference (lesson 23) in Exercise 3 — introduced with context so acceptable
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 80-100min
- **Pacing**: Heavy
- **Issues**: None (if-let forward reference now has inline syntax guidance)
- **Changes made**: Added if-let syntax inline (`if let Some(value) = option { ... }`) and lesson 025 cross-reference to Exercise 3, task file updated

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 80-100min. **Pacing**: Heavy. **Issues**: None — two major concepts (ADT enums + Option) managed with STRETCH tag on Ex 4 and inline if-let guidance. **Changes**: Changelog only.
