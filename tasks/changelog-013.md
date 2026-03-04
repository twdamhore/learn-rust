# Changelog - Lesson 013: Copy vs Clone, when moves happen

## Section 3: Ownership System

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Copy trait and which types implement it, Clone trait for explicit deep copy, when to derive Copy/Clone on structs, Copy-Clone supertrait relationship, recognizing move situations
- **Exercises added**: Derive Copy+Clone on Point vs Label (String field error), explicit clone on String and Vec, three ways to fix a move (clone/return/reference), Copy semantics with arrays of Copy vs non-Copy types

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Moderate for 1-hour lesson
- **Issues found**:
  - Uses `#[derive(Copy, Clone)]` before derive is formally taught in lesson 023
  - Exercise 3 previews references (lesson 014) as one of three fix strategies
- **Recommendations**:
  - Both forward references are pragmatically necessary and acceptable
  - Label reference fix in Exercise 3 as a preview

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Moderate (~1 hr) for 1-2 hour target
- **Changes noted**: Uses #[derive(Copy, Clone)] before derive is formally taught (lesson 21) -- pragmatically necessary. Exercise 3 previews references (lesson 14).
- **Why**: Natural flow from lesson 12's move semantics.
- **v4 recommendations status**: N/A. Gradual progression: Smooth continuation.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~50-70 min
- **Pacing verdict**: Moderate
- **Split needed**: No
- **Key issues**:
  - Minor: uses #[derive(Copy, Clone)] before derive taught (lesson 21)
- **Action taken**: Changelog updated

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Moderate (~50-70 min)
- **Status**: No changes needed

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~50-70 min (Moderate)
- **Needs split**: No
- **Progression**: Good continuation of ownership trilogy (12-13-14).
- **Issues**: Minor derive forward reference (lesson 21) is pragmatically necessary.
- **Changes made**: None

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~50-70 min
- **Pacing**: Good
- **Needs split**: No
- **Issues**: None. Uses derive(Copy, Clone) before lesson 21 — pragmatically necessary. Exercise 3 previews references (lesson 14), appropriate.
- **Changes made**: Changelog updated only

### v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match with CLAUDE.md Section 3 (Ownership System)
- **Time estimate**: 50-70 minutes (Moderate)
- **Needs splitting**: No
- **Pacing context**: Good momentum builder in the ownership trilogy (012-013-014). Minor forward refs (derive Copy before lesson 21) are pragmatically necessary and acceptable.
- **Unresolved from prior reviews**: None
- **New findings**: None beyond prior reviews
- **Recommendation**: No action needed

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 55-75min (Moderate)
- **Needs split**: No
- **Progression**: Minor: `std::array::from_fn` in Ex 4 may confuse. Forward refs to derive and references are pragmatically necessary.
- **Changelog reconciliation**: All prior findings consistent — no stale flags
- **Genuinely unresolved**: None
- **Recommendation**: No action needed.

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 55-80min
- **Pacing**: Good
- **Issues**: Minor — `std::array::from_fn` in Ex 4 is obscure API
- **Recommendations**: Consider simpler construction or inline syntax
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 65-80min
- **Pacing**: Good
- **Issues**: Exercise 4 uses std::array::from_fn which may confuse learners — consider simplifying to explicit array construction
- **Changes made**: Changelog updated only

### v13-fix - Applied pending task file fixes (2026-03-04)
- Simplified `std::array::from_fn` usage in Exercise 4 — added explanatory note for unfamiliar syntax
- **Why**: `std::array::from_fn` is not intuitive for new Rust learners and distracts from the Copy/Clone lesson focus
- **Resolves**: v12 and v13 recommendation

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 60-80min
- **Pacing**: Medium
- **Issues**: None
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, progression, and content quality
- **Estimated time**: 60-80min
- **Pacing**: Medium
- **Issues**: None. Forward references (derive, references) pragmatically necessary
- **Changes made**: Changelog updated only
