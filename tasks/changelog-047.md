# Changelog - Lesson 047: Operator overloading, Deref/DerefMut, Drop

## Section 9: Generics & Traits

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: std::ops operator traits (Add/Sub/Mul/Neg/Index), Deref/DerefMut for smart pointer behavior, deref coercion chains, Drop for cleanup, Drop vs Copy mutual exclusion
- **Exercises added**: Vector2D arithmetic operators, MyBox with Deref coercion, CaseInsensitiveString wrapper with Deref, DatabaseConnection with Drop and scope observation

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Heavy for 1-hour lesson
- **Issues found**:
  - Three loosely-related sub-topics (operator overloading, Deref, Drop) in one lesson
  - Drop/Copy mutual exclusion objective has no dedicated exercise
- **Recommendations**:
  - Consider making Exercise 3 (CaseInsensitiveString) optional to free time for Drop/Copy exercise

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Heavy (~1.5 hr) for 1-2 hour target
- **Changes noted**: Three loosely-related sub-topics (operator overloading, Deref, Drop). Objective 5 (Drop/Copy mutual exclusion) has no exercise. Vector2D exercise (implementing Add, Sub, Neg, Mul) is substantial alone.
- **Why**: Topics feel scattered; too much breadth.
- **v4 recommendations status**: Not yet applied -- v4 recommended making CaseInsensitiveString optional. Gradual progression: Heavy; two heavy lessons back-to-back (044-045).

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1.5 hours
- **Pacing verdict**: Heavy - OK - under 2hr threshold
- **Split needed**: No
- **Key issues**:
  - Three loosely-related sub-topics (operator overloading, Deref, Drop)
  - Vector2D exercise alone is substantial
  - Objective 5 (Drop/Copy exclusion) has no exercise
  - Back-to-back heavy with 044
- **Action taken**: No structural changes. Heavy but within 2hr threshold.

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Heavy (~1.5 hr)
- **Status**: No changes needed under relaxed threshold
- Three sub-topics acceptable at relaxed pace.

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~90 min (Heavy)
- **Needs split**: No
- **Progression**: Heavy section closer. Three loosely-related sub-topics.
- **Issues**: Objective 5 (Drop/Copy exclusion) has no exercise -- should add a short one (flagged since v4, unresolved). Exercise 3 (CaseInsensitiveString) should be marked optional/stretch.
- **Changes made**: None (content fix deferred to lesson start)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~90 min
- **Pacing**: Heavy
- **Needs split**: No
- **Issues**: Three loosely-related sub-topics (operator overloading, Deref, Drop). UNCOVERED OBJECTIVE — Objective 5 (Drop/Copy exclusion) has no exercise. Exercise 3 (CaseInsensitiveString) should be [STRETCH]. Second heavy in a row after 044. Flagged since v4.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match
- **Time estimate**: 90-100 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: Back-to-back heavy with 044; three loosely-related sub-topics
- **Unresolved from prior reviews**: (1) Exercise 3 (CaseInsensitiveString) should be marked [STRETCH] (flagged since v4). (2) Objective 5 (Drop/Copy exclusion) has no exercise (flagged since v4).
- **New findings**: None
- **Recommendation**: Mark Exercise 3 as [STRETCH]; add short Drop/Copy exclusion exercise or remove Objective 5

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 90-110min (Heavy)
- **Needs split**: No
- **Progression**: Heavy section closer. Three loosely-related sub-topics remain but are manageable at this pace.
- **Changelog reconciliation**: "Exercise 3 should be [STRETCH]" flagged since v4 -- task file already has [STRETCH] on Exercise 3. Resolved.
- **Genuinely unresolved**: No exercise for Drop/Copy mutual exclusion (Objective 5) -- add short exercise
- **Recommendation**: Add short exercise demonstrating Drop/Copy mutual exclusion (e.g., try deriving both, observe compiler error)

### v11-fix - Added Drop/Copy mutual exclusion exercise (2026-03-04)
- Added Exercise 5: try deriving Copy on a type with Drop, read the error
- **Why**: Objective 5 (Drop/Copy exclusion) had no exercise
- **Resolves**: Minor item from v11

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 90-110min
- **Pacing**: Heavy
- **Issues**: Three scattered sub-topics; back-to-back heavy with lesson 046
- **Recommendations**: Reduce Ex 1 from 4 operators to 2 (Add+Neg), making Sub+Mul optional
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing review (2026-03-04)
- Reviewed all 100+ tasks for realistic human pacing (1-2hr OK, split if >2hr)
- **Estimated time**: 90-110min (Heavy but under 2hr)
- **Decision**: No split needed. Exercise 3 already [STRETCH], Exercise 5 is only 5 min.
- **Rationale**: Three sub-topics (operators, Deref, Drop) is heavy breadth but each exercise is manageable. Back-to-back with 044 (also heavy) is a concern, but with 044's Ex 5 now [STRETCH], the combined load is more manageable.
- **Changes made**: No task file changes (already has appropriate STRETCH labels)

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 80-100min
- **Pacing**: Heavy
- **Issues**: Covers 3 distinct topics (operator overloading, Deref/DerefMut, Drop). Exercise 1 requires 4 operator trait impls — consider reducing to 2 required (Add+Neg), rest optional. Lesson is dense but coherent theme of 'special trait implementations'
- **Changes made**: Changelog updated only

### v13-fix - Applied pending task file fixes (2026-03-04)
- Reduced Exercise 1 from 4 required operator impls to 2 required (Add + Neg), with Sub and Mul<f64> as optional
- **Why**: 4 full trait implementations is mechanically heavy; the learning value is captured in the first 2
- **Resolves**: v12 and v13 recommendation

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 80-100min
- **Pacing**: Heavy
- **Issues**: No issues
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 80-100min. **Pacing**: Heavy. **Issues**: Back-to-back heavy pair with 044, mitigated by STRETCH markings. **Changes**: Changelog only.
