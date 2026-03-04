# Changelog - Lesson 062: PhantomData and Type-Level Markers
## Section 12: Smart Pointers & Interior Mutability

### v1 - Created from split (2026-03-03)
- Split from original lesson 061 which was rated OVERLOADED (~2+ hrs)
- **Reason for split**: Original lesson 061 combined 4 completely unrelated topics (Cow, Weak, Pin, PhantomData) with no coherent throughline. PhantomData is grouped with type-level markers as a focused lesson on using the type system for safety. Pin<T> content moved to lesson 073 (advanced async) where it can be properly motivated with async/await context.
- **Scope**: PhantomData<T> for type-level markers, typed IDs, units systems, and drop checking/variance effects
- **Estimated time**: ~1-1.5 hours

### v2 - Full curriculum pacing review (2026-03-03)
- Reviewed task file and changelog for pacing, progression, and 1-2hr achievability
- **Estimated time**: ~90 min (Heavy, risks exceeding 2hr)
- **Needs split**: No
- **PREREQUISITE VIOLATION**: Exercise 3 uses *const T raw pointers (not taught until lesson 081). This was removed from lesson 053 but reappeared here. Must be fixed -- replace with safe equivalent.
- **Issues**: Exercise 4 (typestate builder) should be marked [STRETCH] -- it previews lesson 088.
- **Changes made**: None (content fix deferred to lesson start -- HIGH PRIORITY)

### v9 - Full curriculum review — pacing, progression, and content audit (2026-03-03)
- Reviewed all 100 tasks for realistic human pacing (1-2 hr target, split if >2 hrs)
- **Estimated time**: ~90 min
- **Pacing**: Heavy (borderline)
- **Needs split**: No
- **Issues**: PREREQUISITE VIOLATION (HIGH PRIORITY) — Exercise 3 uses *const T raw pointers, not taught until lesson 73 (unsafe section). Same issue was removed from lesson 50 but reappeared here. Must replace with safe equivalent. Exercise 4 (typestate builder) previews lesson 79 — mark [STRETCH]. Flagged since v4.
- **Changes made**: Changelog updated only

## v10 - Comprehensive Cross-Curriculum Pacing Review (2026-03-03)
- **Reviewer**: Full curriculum audit (lessons 001-100 reviewed against CLAUDE.md)
- **Alignment**: Well-scoped split from original 057
- **Time estimate**: 90 minutes (Heavy)
- **Needs splitting**: No
- **Pacing context**: Concludes the heavy smart pointers cluster (058-062)
- **Unresolved from prior reviews**: HIGH PRIORITY -- (1) Exercise 3 uses *const T raw pointers (not taught until lesson 081). Must be replaced with safe equivalent. (2) Exercise 4 typestate preview should be marked [STRETCH]. Both flagged since v2.
- **New findings**: None
- **Recommendation**: Replace raw pointer exercise with safe equivalent before lesson start (HIGH PRIORITY)

### v11 - Comprehensive curriculum review with changelog reconciliation (2026-03-03)
- Full review of all 100 tasks: pacing realism, progression, prerequisite audit, and changelog-vs-task-file reconciliation
- **Estimated time**: 90-110min (Heavy)
- **Needs split**: No
- **Progression**: Concludes the heavy smart pointers cluster (058-062)
- **Changelog reconciliation**: "Exercise 3 uses *const T raw pointers" flagged since v2 -- but task file uses `PhantomData<&'a T>` with safe BorrowTracker, no raw pointers. Resolved. Exercise 4 (typestate builder) already [STRETCH].
- **Genuinely unresolved**: None (raw pointer issue was stale; typestate already marked [STRETCH])
- **Recommendation**: No changes needed; prior raw pointer concern is resolved

### v12 - Full curriculum pacing and progression review (2026-03-04)
- Reviewed all active tasks for realistic human pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 90-110min
- **Pacing**: Heavy
- **Issues**: None
- **Recommendations**: None
- **Changes made**: Changelog updated only

### v13 - Full curriculum pacing, progression, and prerequisite review (2026-03-04)
- Reviewed task file for realistic pacing (1-2hr target, split if >2hr), prerequisite ordering, and gradual progression
- **Estimated time**: 75-95min
- **Pacing**: Heavy
- **Issues**: PhantomData is abstract; 3 dense exercises covering typed IDs, type-safe units with operator overloading, and PhantomData with lifetimes. Consider reordering to put lifetime exercise before units exercise
- **Changes made**: Changelog updated only

### v14 - Full curriculum review (2026-03-04)
- Reviewed task file for pacing, prerequisites, progression, and content quality
- **Estimated time**: 75-95min
- **Pacing**: Heavy
- **Issues**: Exercise 2 PhantomData + operator overloading density noted (acceptable)
- **Changes made**: Changelog updated only

### v15 - Full curriculum review (2026-03-04)
- Reviewed. **Time**: 75-95min. **Pacing**: Heavy. **Changes**: Softened Objective 4 — removed explicit PhantomData<*mut T> reference, deferred raw pointer variance details to lesson 081. **Why**: Raw pointers not taught until lesson 081; direct mention could confuse.
