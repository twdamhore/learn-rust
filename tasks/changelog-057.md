# Changelog - Lesson 057: Cow<T>, Weak references, Pin<T>, PhantomData

## Section 12: Smart Pointers & Interior Mutability

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: Cow clone-on-write optimization, Weak references for cycle breaking, Pin for immovable types (conceptual), PhantomData for type-level metadata
- **Exercises added**: normalize_name with Cow<str> and is_borrowed check, breaking reference cycle with Weak::upgrade, Pin<Box<T>> exploration with self-referential struct, PhantomData-based typed Id<T> preventing type confusion

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Overloaded for 1-hour lesson
- **Issues found**:
  - Four completely unrelated advanced topics (Cow, Weak, Pin, PhantomData) in one lesson
  - Pin<T> is hard to motivate without async context (Section 14, lessons 63-67)
  - PhantomData coverage duplicates lesson 050 exercise 3
- **Recommendations**:
  - Make Pin<T> coverage lighter here (conceptual only) and deeper in lesson 067 (advanced async)
  - Remove PhantomData from either this lesson or lesson 050
  - Consider splitting into two lessons if time permits

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: OVERLOADED (~2+ hr) for 1-2 hour target
- **Changes noted**: Four completely unrelated advanced topics (Cow, Weak, Pin, PhantomData). Pin without async context (not until lesson 63) is premature. PhantomData duplicates lesson 050.
- **Why**: Four mini-lessons stapled together with no coherent throughline.
- **v4 recommendations status**: Not yet applied -- v4 recommended moving Pin to lesson 67, deduplicating PhantomData, splitting lesson. Gradual progression: CRITICAL -- follows three heavy lessons; learner burnout risk.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~2+ hours
- **Pacing verdict**: OVERLOADED - split required
- **Split needed**: Yes - split into 057a/057b
- **Key issues**:
  - 4 completely unrelated topics (Cow, Weak, Pin, PhantomData) with no throughline
  - Pin without async context (lesson 63) is premature
  - PhantomData duplicates lesson 050
  - Follows three heavy lessons (054-056) creating burnout risk
- **Action taken**: Split into task-057a (Cow and Weak) and task-057b (PhantomData and type-level markers). Pin<T> content moved to lesson 067 where it belongs (after async context). PhantomData deduplication resolved by removing it from lesson 050 and keeping it in 057b.

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: OVERLOADED (~2+ hr)
- **Status**: Changes noted below
- Already split in v6. **Task files now created** for 057a/057b (were missing).
- Pin<T> moved to 067b. 057a covers Cow+Weak, 057b covers PhantomData and type-level markers.

### v8 - Full curriculum pacing review (2026-03-03)
- Original lesson correctly split into 057a/057b at v6. Original was ~150+ min.
- **Changes made**: None (split already done)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~150+ min
- **Pacing**: OVERLOADED
- **Needs split**: Yes (already split into 057a/057b)
- **Issues**: Four unrelated topics. Pin<T> moved to lesson 067.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: SUPERSEDED by 057a/057b
- **Time estimate**: 150+ minutes (OVERLOADED, original)
- **Needs splitting**: Already split at v6
- **Pacing context**: Original combined Cow, Weak, Pin, PhantomData. Pin moved to lesson 067.
- **Unresolved from prior reviews**: None (resolved via split)
- **New findings**: None
- **Recommendation**: No further changes -- see changelog-057a.md and changelog-057b.md

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 150+min original (OVERLOADED)
- **Needs split**: No (SUPERSEDED by 057a/057b)
- **Progression**: Split was correct. Pin moved to lesson 067.
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: None -- see 057a/057b changelogs
- **Recommendation**: No changes to parent; see 057a/057b for sub-part status

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- SUPERSEDED by 057a/057b. No changes to parent.

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: N/A
- **Pacing**: SUPERSEDED
- **Issues**: SUPERSEDED by 057a/057b
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. Correctly superseded. **Changes**: Changelog only.
