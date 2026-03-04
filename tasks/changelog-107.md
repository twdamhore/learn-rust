# Changelog - Lesson 107: Memory layout - repr, alignment, size optimization

## Section 20: Special Targets

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Default vs repr(C) struct layout, std::mem inspection functions (size_of, align_of, offset_of!), repr(packed/transparent/align), field reordering for size optimization, enum layout and niche optimization
- **Exercises added**: Compare struct sizes with different field orders, repr(C) network packet header with offset verification, enum niche optimization exploration with Option types, cache-line aware struct optimization exercise

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Moderate for 1-hour lesson
- **Issues found**:
  - `std::mem::offset_of!` is relatively recent (Rust 1.77, March 2024)
  - Exercise format uses unnumbered bullets (formatting inconsistency)
- **Recommendations**:
  - Note minimum Rust version for offset_of!
  - Standardize exercise format

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: Moderate (~1 hr) for 1-2 hour target
- **Changes noted**: Exercises are exploratory (print sizes, observe niche) rather than heavy implementation. offset_of! requires Rust 1.77+. Exercise format inconsistency.
- **Why**: Well-structured low-level memory exploration.
- **v4 recommendations status**: Not yet applied -- v4 noted offset_of! version requirement. Gradual progression: Good; reasonable scope.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~1 hour
- **Pacing verdict**: Moderate - OK - under 2hr threshold
- **Split needed**: No
- **Key issues**:
  - Exercise format inconsistent (unnumbered bullets)
  - offset_of! requires Rust 1.77+ (not mentioned in task)
- **Action taken**: No changes needed. Minor issues should be addressed when task content is updated.

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: Moderate (~1 hr)
- **Status**: No changes needed

### v8 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and all prior changelog entries for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~60 min (Moderate)
- **Needs split**: No
- **Issues**: Add note: "std::mem::offset_of! requires Rust 1.77+". Exercise format uses unnumbered bullets.
- **Changes made**: None

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~55-65 min
- **Pacing**: Good
- **Needs split**: No
- **Issues**: Exercise format uses unnumbered bullets — must standardize. std::mem::offset_of! requires Rust 1.77+, should note version requirement. Unresolved since v4.
- **Changes made**: Changelog updated only

### v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Exact match with CLAUDE.md
- **Time estimate**: 55-65 minutes (Moderate)
- **Needs splitting**: No
- **Pacing context**: Exploratory exercises (print sizes, observe niche optimization) keep scope manageable.
- **Unresolved from prior reviews**: (1) offset_of! requires Rust 1.77+ -- add version note (flagged since v4). (2) Exercise format uses unnumbered bullets (flagged since v4).
- **New findings**: None
- **Recommendation**: Add Rust version note for offset_of! and fix exercise format when task content is next updated

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 55-70min (Moderate)
- **Needs split**: No
- **Progression**: Exploratory exercises keep scope manageable. Well-structured low-level memory exploration.
- **Changelog reconciliation**: "offset_of! version note missing" — task file already includes Rust 1.77+ note. Resolved.
- **Genuinely unresolved**: None
- **Recommendation**: No action needed — offset_of! version note already present in task file

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 55-70min
- **Pacing**: Good
- **Issues**: None
- **Recommendations**: None
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 65-80min
- **Pacing**: Good
- **Issues**: NonZeroU64 and std::num::NonZero* types used without introduction. repr(packed) safety implications (UB from unaligned access) should be emphasized
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 65-80min
- **Pacing**: Good
- **Issues**: NonZeroU64 and std::num types used without introduction; repr(packed) safety implications (UB from unaligned access) should be emphasized; `type` is a reserved keyword used as field name
- **Changes made**: Fixed type reserved keyword to msg_type in Exercise 2, added NonZeroU64 note in Exercise 3, added repr(packed) UB warning in Exercise 4, task file updated

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 65-80min. **Pacing**: Good. **Issues**: None — all v14 fixes verified. **Changes**: Changelog only.
