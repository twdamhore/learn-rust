# Changelog - Lesson 039: Iterators - Iterator trait, adaptors, collect, chaining

## Section 8: Collections & Iterators

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Iterator trait and next(), adaptors (map/filter/enumerate/zip/take/skip/etc.), collect with turbofish, chaining, laziness
- **Exercises added**: filter-map-collect pipeline, multi-step adaptor chain, zip and enumerate combinations, lazy evaluation proof with noisy function

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - 9 iterator adaptors listed is a large surface area
- **Recommendations**:
  - Focus deep coverage on most important adaptors (map, filter, collect), let others be reference material

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~1.5 hr) for 1-2 hour target
- **Changes noted**: 9 iterator adaptors represents large API surface. Risk is breadth over depth. Exercise 2 (five-step pipeline) is ambitious.
- **Why**: Too many adaptors listed.
- **v4 recommendations status**: Not yet applied -- v4 recommended deep coverage on map/filter/collect, reference for rest.
- **Gradual progression**: Heavy back-to-back with lesson 36.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.5 hr
- **Pacing verdict**: Heavy - under 2hr threshold
- **Split needed**: No
- **Key issues**:
  - 9 iterator adaptors is too many
  - Exercise 2 (5-step pipeline) ambitious
  - Second heavy lesson in a row after 036
  - v4 recommendation to focus on map/filter/collect not applied
- **Action taken**: Changelog updated with pacing assessment

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Heavy (~1.5 hr)
- **Status**: No changes needed
- No changes needed under relaxed threshold. 9 iterator adaptors still flagged as dense. Note: second of three heavy in a row.

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~90 min (Heavy)
- **Needs split**: No
- **Progression**: Second of three consecutive heavy lessons. 9 iterator adaptors risks shallow coverage.
- **Issues**: Should restructure Objective 2 to distinguish "core" adaptors (map, filter, collect, enumerate) from "reference" adaptors (zip, take, skip, chain, flat_map, peekable) (flagged since v4, unresolved). Exercise 2's 5-step pipeline should provide scaffold/template.
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~90 min
- **Pacing**: Heavy
- **Needs split**: No
- **Issues**: 9 iterator adaptors (map, filter, enumerate, zip, take, skip, chain, flat_map, peekable) too many for deep coverage. Should split into "core" (map, filter, collect, enumerate) vs "reference" (others). Exercise 2 requires 5-step pipeline, ambitious. FATIGUE WARNING — second of three consecutive heavy lessons. Unresolved since v4.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Good match
- **Time estimate**: 90 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: Second of three consecutive heavy lessons (036-037-038). Fatigue risk.
- **Unresolved from prior reviews**: (1) 9 iterator adaptors is too many -- split into core (map/filter/enumerate/collect) vs reference. (2) Exercise 2 five-step pipeline needs scaffold/template. Both unresolved since v4.
- **New findings**: None
- **Recommendation**: Restructure Objective 2 into "core" vs "reference" adaptors. Provide scaffold for Exercise 2's pipeline. Both fixes are straightforward.

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 80-90min (Heavy)
- **Needs split**: No
- **Progression**: Second of 3 consecutive heavy lessons (036-037-038). Fatigue risk remains.
- **Changelog reconciliation**: "9 iterator adaptors too many" flagged since v4 -- task file has already been restructured into "core" vs "reference" adaptors. Resolved.
- **Genuinely unresolved**: Exercise 2 five-step pipeline still needs starter code/scaffold
- **Recommendation**: Provide starter code scaffold for Exercise 2 before lesson start

### v11-fix - Added pipeline starter code to Exercise 2 (2026-03-04)
- Added starter template showing first 2 steps of 5-step pipeline
- **Why**: 5-step pipeline without scaffold was frustrating for learners
- **Resolves**: Minor item from v11

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 80-95min
- **Pacing**: Heavy
- **Issues**: Second heavy in 036-038 cluster.
- **Recommendations**: None
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 65-80min
- **Pacing**: Good
- **Issues**: Exercise 2 starter code step numbering inconsistent with exercise description. Closures (|x| ...) used throughout without formal introduction — add brief note referencing Java lambdas/Go function literals
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 65-80min
- **Pacing**: Medium-Heavy
- **Issues**: Exercise 2 starter code steps didn't match exercise description; closure syntax used without introduction
- **Changes made**: Fixed Exercise 2 starter code to align steps with description (Step 1 skip header, Step 2 filter empty, Step 3 trim, Step 4 enumerate, Step 5 collect). Added closure syntax note referencing Java lambdas and Go function literals, with pointer to lesson 055.

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 65-80min. **Pacing**: Medium-Heavy. **Issues**: None — core/reference adaptor split good, closure note essential. **Changes**: Changelog only.
