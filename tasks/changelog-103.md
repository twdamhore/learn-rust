# Changelog - Lesson 103: no_std - embedded basics, core vs std

## Section 20: Special Targets

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: #![no_std] and what it removes, core vs std vs alloc, writing no_std-compatible code, conditional std/no_std compilation with features, real-world use cases compared to Go
- **Exercises added**: Fixed-size ArrayStack using only core types, conditional std feature gating, SortedVec with alloc crate, testing with --no-default-features

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Moderate for 1-hour lesson
- **Issues found**:
  - Exercise format uses unnumbered bullets (formatting inconsistency)
- **Recommendations**:
  - Standardize exercise format to 'Exercise N -- Title'

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Moderate (~1 hr) for 1-2 hour target
- **Changes noted**: Concepts well-explained, exercises appropriately scoped. ArrayStack and SortedVec reinforce earlier lessons. Exercise format inconsistency (unnumbered bullets).
- **Why**: Concrete implementations accessible without embedded experience.
- **v4 recommendations status**: Not yet applied -- v4 noted format inconsistency. Gradual progression: Good; manageable.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1 hour
- **Pacing verdict**: Moderate - OK - under 2hr threshold
- **Split needed**: No
- **Key issues**:
  - Exercise format uses unnumbered bullets (inconsistent with earlier lessons)
- **Action taken**: No changes needed. Well-scoped lesson. Exercise format inconsistency is minor and should be fixed when task content is updated.

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Moderate (~1 hr)
- **Status**: No changes needed

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~60 min (Moderate)
- **Needs split**: No
- **Progression**: Good section opener for Special Targets. Concrete implementations keep it grounded.
- **Issues**: Exercise format uses unnumbered bullets (must standardize).
- **Changes made**: None

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~55-65 min
- **Pacing**: Good
- **Needs split**: No
- **Issues**: Exercise format uses unnumbered bullets — must standardize. Go comparison (single-runtime makes bare-metal Go impractical) is nice bridge. Unresolved since v4.
- **Changes made**: Changelog updated only

### v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match with CLAUDE.md
- **Time estimate**: 55-65 minutes (Moderate)
- **Needs splitting**: No
- **Pacing context**: Well-scoped Section 20 opener. Concrete implementations (ArrayStack, SortedVec) reinforce earlier lessons without requiring embedded hardware.
- **Unresolved from prior reviews**: Exercise format uses unnumbered bullets -- must standardize to "Exercise N -- Title" (flagged since v4)
- **New findings**: None
- **Recommendation**: Fix exercise format when task content is next updated

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 60-75min (Moderate)
- **Needs split**: No
- **Progression**: Well-paced Section 20 opener. Exercises reinforce generics/traits without hardware.
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: None
- **Recommendation**: No changes needed. Well-scoped lesson.

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 55-75min
- **Pacing**: Good
- **Issues**: None
- **Recommendations**: None
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 70-85min
- **Pacing**: Good
- **Issues**: extern crate alloc syntax has not been covered — modern Rust rarely uses extern crate. Add brief explanation of why it is needed in no_std contexts
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 70-85min
- **Pacing**: Good
- **Issues**: extern crate alloc syntax not covered in modern Rust — needs explanation for no_std contexts
- **Changes made**: Added extern crate alloc explanation in Exercise 3, task file updated

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 70-85min. **Pacing**: Good. **Changes**: Standardized exercise title separators from single dash to double-dash for consistency. **Why**: Cosmetic inconsistency with other lessons.
