# Changelog - Lesson 044: impl Trait in argument vs return position, when to use which

## Section 9: Generics & Traits

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
- **Objectives added**: impl Trait in argument position (sugar for generics), return position (existential type), when each is appropriate, return-position limitation (same concrete type), comparison with dyn Trait
- **Exercises added**: Three-way argument position equivalence, return-position iterator with impl Iterator, return-position limitation and two fixes (Vec/Box<dyn>), closure return with impl Fn

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Moderate for 1-hour lesson
- **Issues found**:
  - Deliberate overlap with task 041 (impl Trait intro) and task 043 (dyn Trait) -- bridges the two
  - Exercise 4 (make_adder) is duplicated in task 052
- **Recommendations**:
  - Differentiate Exercise 4 from task 052's make_adder or cross-reference between lessons

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Moderate (~1 hr) for 1-2 hour target
- **Changes noted**: Good bridging lesson. Duplicate exercise: make_adder appears here (Exercise 4) and in task 052 (Exercise 2). Minor dyn Trait preview from lesson 43.
- **Why**: Duplication should be resolved.
- **v4 recommendations status**: Not yet applied -- v4 flagged make_adder duplication. Gradual progression: Good bridging; smooth pace.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1 hour
- **Pacing verdict**: Moderate - OK - under 2hr threshold
- **Split needed**: No
- **Key issues**:
  - make_adder exercise duplicated in task 052 Exercise 2
- **Action taken**: No structural changes. Bridging lesson with deliberate overlap noted.

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Moderate (~1 hr)
- **Status**: No changes needed
- make_adder duplication with 052 still flagged.

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~60 min (Moderate)
- **Needs split**: No
- **Progression**: Effective bridging lesson between trait bounds (041) and trait objects (043).
- **Issues**: Exercise 4 (make_adder) duplicated in task 052 Exercise 2. Should change to make_multiplier or add cross-reference (flagged since v4, unresolved).
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~60 min
- **Pacing**: Good
- **Needs split**: No
- **Issues**: DUPLICATE EXERCISE — Exercise 4 (make_adder) nearly identical to task 052 Exercise 2. Recommend changing to make_multiplier. Flagged since v4. Deliberate overlap with 041/043 is intentional bridging.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match
- **Time estimate**: 60 minutes (Moderate)
- **Needs splitting**: No
- **Pacing context**: Good bridging lesson between trait bounds (041) and trait objects (043)
- **Unresolved from prior reviews**: Exercise 4 (make_adder) duplicated in task 052 Exercise 2 -- rename to make_multiplier (flagged since v4)
- **New findings**: None
- **Recommendation**: Rename Exercise 4 from make_adder to make_multiplier before lesson start

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 60-70min (Moderate)
- **Needs split**: No
- **Progression**: Bridging lesson serves purpose well. Smooth transition from trait bounds (041) to trait objects (043).
- **Changelog reconciliation**: "Exercise 4 make_adder duplicates task 052" flagged since v4 -- task file now says `make_multiplier`. Resolved.
- **Genuinely unresolved**: None
- **Recommendation**: No further changes needed. Duplication resolved.

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 60-75min
- **Pacing**: Good
- **Issues**: Minor — lightly previews dyn Trait from lesson 045
- **Recommendations**: None
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 55-70min
- **Pacing**: Good
- **Issues**: Intentionally previews dyn Trait (lesson 43) and Box<dyn Iterator> (lessons 43/54) — well-motivated as this is the bridging lesson designed for comparison
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 55-70min
- **Pacing**: Medium
- **Issues**: Exercise 1 option (c) asked learner to explain dispatch trade-offs before trait objects are taught
- **Changes made**: Softened Exercise 1 option (c) about `&dyn Summary` from requiring dispatch trade-off explanation to a simple preview observation, deferring explanation to lesson 045.

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 55-70min. **Pacing**: Medium. **Issues**: None — well-designed bridging lesson. **Changes**: Changelog only.
