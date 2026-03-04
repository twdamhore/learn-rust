# Changelog - Lesson 050: Advanced lifetimes - HRTBs, variance, subtyping

## Section 10: Lifetimes

### v1 - Initial creation
- Lesson added to curriculum

### v2 - Review audit (2026-03-03)
- Reviewed task file against CLAUDE.md curriculum
- **Result**: Title, section assignment, and topic all align with curriculum
- **Status**: pending (no content changes needed)

### v3 - Concrete objectives and exercises (2026-03-03)
- Replaced TODO placeholders with concrete objectives and exercises
- **Objectives added**: HRTBs with for<'a> syntax, lifetime variance (covariance/contravariance/invariance), lifetime subtyping ('a: 'b), when HRTBs are needed (closures with references), PhantomData for lifetime relationships
- **Exercises added**: HRTB with closures (apply_to_ref), variance observation (covariance and invariance demo), PhantomData RawSlice with lifetime safety, study real-world HRTBs from std library

### v4 - Comprehensive pacing and content review (2026-03-03)
- Reviewed all 100 tasks for pacing, prerequisites, content density, and exercise formatting
- **Pacing**: Overloaded for 1-hour lesson
- **Issues found**:
  - HRTBs, variance, and subtyping are each individually advanced topics
  - Exercise 3 (RawSlice with raw pointers) touches unsafe territory not covered until Section 16 (lessons 73-76)
  - Exercise 4 (study std library) is open-ended and time-consuming
  - PhantomData coverage duplicates lesson 057 exercise 4
  - **Most conceptually dense lesson in the 041-060 range**
- **Recommendations**:
  - Trim variance to 'conceptual awareness' level rather than requiring deep understanding
  - Make Exercises 3-4 stretch goals
  - Remove PhantomData from either this lesson or lesson 057 to avoid duplication

### v5 - Cross-curriculum review (2026-03-03)
- Full 100-lesson review for pacing realism, prerequisite ordering, and progressive difficulty
- **Pacing**: OVERLOADED (~2-3 hr) for 1-2 hour target
- **Changes noted**: Most conceptually dense lesson in 041-060. HRTBs + variance + subtyping are each individually advanced topics experienced Rustaceans struggle with. Exercise 3 uses raw pointers (not taught until lesson 73 -- unsafe section). PhantomData duplicates lesson 057. Exercise 4 is open-ended research.
- **Why**: Three individually hard topics crammed together; prerequisite violation with unsafe.
- **v4 recommendations status**: Not yet applied -- v4 recommended trimming variance to awareness, making Exercises 3-4 stretch goals, deduplicating PhantomData. Gradual progression: CRITICAL -- hardest lesson so far; should be split or heavily trimmed.

### v6 - Pacing review and split assessment (2026-03-03)
- Full review of all 100 tasks for realistic human pacing (1-2 hr target per lesson)
- **Estimated time**: ~2-3 hours
- **Pacing verdict**: OVERLOADED - split required
- **Split needed**: Yes - split into 050a/050b
- **Key issues**:
  - 3 individually hard topics (HRTBs, variance, subtyping)
  - Exercise 3 uses raw pointers/unsafe (not taught until lesson 73 - PREREQUISITE VIOLATION)
  - PhantomData duplicates lesson 057
  - Exercise 4 is open-ended with no stopping point
- **Action taken**: Split into task-050a (HRTBs) and task-050b (variance/subtyping). Removed raw pointer/unsafe exercise (prerequisite violation). Removed PhantomData exercise (covered in lesson 057). Variance kept at awareness level, not mastery.

## v7 — Relaxed Pacing Review (2026-03-03)
- **Threshold change**: Lessons now OK at 1-2 hours; only split if >2hrs
- **Pacing**: OVERLOADED (~2-3 hr)
- **Status**: Changes noted below
- Already split in v6. **Task files now created** for 050a/050b (were missing).
- Raw pointer exercise removed (prerequisite violation).
- PhantomData removed (covered in 057b).

### v8 - Full curriculum pacing review (2026-03-03)
- Original lesson correctly split into 050a/050b at v6. Original was ~180 min.
- **Changes made**: None (split already done)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~180 min (original)
- **Pacing**: OVERLOADED
- **Needs split**: Yes (already split into 050a/050b)
- **Issues**: None — three individually hard topics. Raw pointer exercise removed. PhantomData moved to 057b.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: SUPERSEDED by 050a/050b
- **Time estimate**: 150-180 minutes original (correctly split)
- **Needs splitting**: Already split at v6; raw pointer exercise removed
- **Pacing context**: Three individually hard topics warranted split; prerequisite violation (unsafe) fixed
- **Unresolved from prior reviews**: None for parent -- see 050a/050b changelogs
- **New findings**: None
- **Recommendation**: No changes to parent; see 050a/050b for sub-part status

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 150-180min original (OVERLOADED)
- **Needs split**: No (SUPERSEDED by 050a/050b)
- **Progression**: Split was correct. Removed raw pointer prerequisite violation and PhantomData duplication.
- **Changelog reconciliation**: All prior findings consistent
- **Genuinely unresolved**: None -- see 050a/050b changelogs
- **Recommendation**: No changes to parent; see 050a/050b for sub-part status

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- SUPERSEDED by 050a/050b. No changes to parent.

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: N/A
- **Pacing**: SUPERSEDED
- **Issues**: SUPERSEDED by 050a/050b
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. Correctly superseded. **Changes**: Changelog only.
